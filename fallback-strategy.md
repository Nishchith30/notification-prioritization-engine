# Fallback Strategy

## If AI Engine Fails
Use rule-based decision engine only.

## If Database Is Slow
Send only HIGH priority notifications.
Delay low priority notifications.

## If System Overloaded
Enable strict rate limiting.

Important notifications are never silently dropped.