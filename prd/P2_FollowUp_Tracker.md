# PRD — P2: Smart Follow-Up Tracker & Auto Reminder Engine

## 1. Problem Statement
Individuals and businesses frequently miss follow-ups, deadlines, and commitments due to fragmented tools and lack of automated tracking. This results in lost opportunities, poor client experience, and productivity inefficiency.

A system is needed that:
- Tracks all pending tasks and follow-ups
- Sends reminders automatically through WhatsApp, email, or notifications
- Highlights overdue tasks
- Provides a unified dashboard for personal and business use

---

## 2. Target Users

### B2B
- Freelancers handling multiple clients  
- Agencies (marketing, real estate, IT services)  
- Sales professionals and CRM-light businesses  
- Small & medium businesses managing leads or tasks  

### B2C
- Students  
- Working professionals  
- Everyday users needing reminders (bills, renewals, tasks)

---

## 3. Core Value Proposition
“Never forget a follow-up again.”

A smart automation system that:
- Tracks all tasks  
- Sends reminders automatically  
- Provides insights on pending & overdue items  
- Keeps users consistent without manual effort  

---

## 4. Goals
- Simple task creation interface  
- Automated reminder notifications  
- Multi-channel reminder system (WhatsApp, Email)  
- Overdue task detection  
- Daily summary report  
- Analytics & history tracking  

---

## 5. Non-Goals
- Full CRM functionality  
- Complex sales automation  
- Multi-tenant enterprise structure  

---

## 6. User Stories
1. As a user, I want to create tasks with due dates.  
2. As a user, I want automatic reminders before deadlines.  
3. As a freelancer, I want a daily summary of pending tasks.  
4. As a business owner, I want reminders on WhatsApp.  
5. As a user, I want overdue tasks highlighted automatically.  

---

## 7. System Architecture Overview

### Frontend  
- Gradio / Streamlit / React (MVP friendly)

### Backend  
- Python FastAPI

### Automation Engine  
- CRON / Celery worker  
- Daily & hourly checks

### Notifications  
- Twilio WhatsApp API  
- SendGrid Email API

### Database  
- PostgreSQL / Supabase

---

## 8. Automation Flow
```
User Adds Task → Store in DB → Scheduler Checks → 
If Due/Overdue → Send Reminder → Log Notification →  
Send Daily Summary Report
```

---

## 9. API Endpoints
```
POST /task
GET /tasks
PUT /task/{id}
DELETE /task/{id}
GET /daily-summary
```

---

## 10. Database Schema

### tasks  
| Field | Type | Description |
|-------|--------|-------------|
| id | UUID | Unique ID |
| title | text | Task title |
| description | text | Task details |
| due_date | datetime | Follow-up date |
| status | enum | pending/completed |
| created_at | datetime | Timestamp |

### notifications  
| Field | Type |
| id | UUID |
| task_id | UUID |
| notification_type | text |
| sent_at | datetime |

---

## 11. KPIs
- Reminder delivery rate  
- Overdue task reduction  
- Tasks completed  
- Daily active users  
- User retention  

---

## 12. Edge Cases
- Due date set in the past  
- WhatsApp API rate limit  
- Email bounce  
- Duplicate reminders  
- Task deleted before firing reminder  

---

## 13. Tech Stack
Python, FastAPI, Supabase, Twilio, SendGrid, CRON, Gradio

---

## 14. Risks & Mitigation
- WhatsApp API cost → add rate controls  
- Notification spam → implement smart frequency rules  
- User privacy concerns → encrypt sensitive data  

