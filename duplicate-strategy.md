# Duplicate Prevention Strategy

## Exact Duplicate
If dedupe_key exists and matches a recent event → Suppress (NEVER)

## Near Duplicate
Check:
- Same user_id
- Same event_type
- Similar message
- Within 5 minutes

If matched → Suppress

## Implementation
- Hash comparison for exact match
- Text similarity scoring for near duplicate
- Time-window filtering