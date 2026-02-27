# Decision Logic Design

The system classifies notifications into NOW, LATER, or NEVER.

## Step 1: Expiry Check
If expires_at < current_time → NEVER

## Step 2: Exact Duplicate Check
If dedupe_key matches recent event → NEVER

## Step 3: Near Duplicate Check
If same user + same event_type + similar message within 5 minutes → NEVER

## Step 4: High Priority Check
If event_type = security_alert OR priority_hint = HIGH → NOW

## Step 5: Alert Fatigue Check
If user exceeded notification limit → LATER

## Step 6: AI Scoring
If score > 0.8 → NOW  
If 0.4–0.8 → LATER  
If < 0.4 → NEVER