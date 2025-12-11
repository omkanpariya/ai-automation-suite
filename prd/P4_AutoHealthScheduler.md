# PRD — P4: Auto Appointment Scheduler + Preventive Health Reminder Engine

## 1. Problem Statement
People miss doctor appointments, checkups, and preventive health scans due to busy schedules and poor reminder systems. Clinics also fail to follow up, causing missed revenue and poor patient care.

Users need:
- Automatic appointment scheduling  
- Recurring health reminders  
- WhatsApp confirmations  
- Smart suggestions for next checkup date  

---

## 2. Target Users

### B2C
- General public  
- Senior citizens  
- Patients with chronic conditions  
- Parents managing kids’ health schedules  

### B2B
- Clinics  
- Dentists  
- Diagnostic labs  
- Wellness centers  

---

## 3. Value Proposition
“Your AI health manager keeps you healthy without effort.”

---

## 4. Features
- Auto scheduling  
- Recurring reminders (weekly, monthly, yearly)  
- WhatsApp reminders  
- Health category-based scheduling  
- Follow-up automation  
- Calendar integration  

---

## 5. User Flow
```
User selects checkup →
AI recommends frequency →
User confirms →
System schedules →
WhatsApp sends confirmation →
Reminders sent →
Next appointment auto-scheduled
```

---

## 6. System Architecture
- FastAPI backend  
- Twilio WhatsApp Bot  
- Scheduler (CRON/Celery)  
- Google Calendar API or custom booking system  

---

## 7. API Endpoints
```
POST /appointment/create
GET /appointment/all
POST /appointment/reschedule
POST /health-scan
```

---

## 8. Database Schema

### appointments  
| id | user_id | type | date | next_due | clinic | status |

### checkup_types  
| id | name | frequency_days |

---

## 9. KPIs
- Appointment completion rate  
- Reminder open rate  
- No-show reduction  
- Monthly active users  

---

## 10. Edge Cases
- Double booking  
- Patient unavailable  
- Clinic API down  
- Invalid phone numbers  

---

## 11. Tech Stack
Python, FastAPI, Google Calendar API, Twilio, Supabase

---

## 12. Risks
- Healthcare privacy  
- Scheduling conflicts  
- API limitations  

