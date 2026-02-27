# Data Model

## Notifications Table
- event_id
- user_id
- event_type
- message
- priority_hint
- timestamp
- channel
- status (Now/Later/Never)
- decision_reason

## User History Table
- user_id
- notifications_last_1hr
- notifications_last_24hr
- last_notification_time

## Suppression / Defer Table
- event_id
- scheduled_time
- reason

## Audit Log Table
- event_id
- decision
- reason
- timestamp
- confidence_score