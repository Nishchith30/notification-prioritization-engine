# Notification Prioritization Engine

## Problem Statement
Users receive too many notifications. Some are repetitive, low-value, or sent at bad times. 
The system must decide whether to send each notification NOW, LATER, or NEVER.

## Solution Overview
This system uses rule-based logic combined with AI scoring to classify notifications.
It prevents duplicates, reduces alert fatigue, and logs every decision for explainability.

## Core Features
- Now / Later / Never classification
- Duplicate detection (exact + near duplicate)
- Alert fatigue control
- Human-configurable rules
- Audit logging
- Safe fallback mechanism

## High-Level Flow
Incoming Event → Duplicate Check → Fatigue Check → Priority Check → AI Score → Final Decision → Logging → Delivery

## Tools & Assumptions
- Rule-based engine
- AI scoring (optional layer)
- Redis (for fast counters)
- PostgreSQL (for logs & storage)