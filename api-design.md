# API Design

## 1. Submit Notification
POST /notifications/event

Request Body:
{
  user_id,
  event_type,
  message,
  priority_hint,
  timestamp
}

Response:
{
  event_id,
  decision
}

## 2. Get Decision
GET /notifications/{event_id}

## 3. Update Rules
POST /rules/update

## 4. Get Audit Log
GET /audit/{event_id}