# PRD — P3: WhatsApp Notification + Auto Dashboard Generator

## 1. Problem Statement
Businesses and individuals collect large amounts of data but lack the time or skill to convert it into dashboards and insights. Manual dashboard building is slow, requires expertise, and often gets ignored.

Users need:
- Automated dashboard creation  
- AI-generated insights  
- WhatsApp delivery of reports  
- A simple workflow to get insights instantly  

---

## 2. Target Users

### B2B
- Small businesses  
- Agencies  
- Doctors, salons, clinics  
- Logistics & retail  

### B2C
- Students  
- Fitness/health trackers  
- Personal finance users  

---

## 3. Core Value Proposition
"Your data speaks to you automatically."

Upload a file → dashboard auto-generated → WhatsApp sends insights → user understands data instantly.

---

## 4. Goals
- Upload Excel/CSV  
- Auto dashboard creation using Python & Plotly  
- AI summary (OpenAI/Gemini)  
- WhatsApp report delivery  
- Scheduled recurrent summaries  

---

## 5. Features
- One-click dashboard  
- Auto chart generation  
- KPI cards  
- Trend identification  
- Weekly/daily automated WhatsApp reports  

---

## 6. System Flow
```
User Uploads Data →
AI Analyzes → Creates Charts →
Generates Dashboard Link →
WhatsApp Sends Summary →
Store Analytics History
```

---

## 7. API Endpoints
```
POST /upload-data
GET /dashboard/{id}
POST /send-summary
POST /schedule-report
```

---

## 8. Dashboard Autogen Template
- KPI cards (total, averages, etc.)  
- Line chart  
- Bar chart  
- Pie/Donut chart  
- Trend analysis  
- Forecast (optional)  

---

## 9. Database Schema

### uploads  
| id | user_id | file_path | created_at |

### dashboards  
| id | upload_id | html_path | insights |

---

## 10. KPIs
- Dashboard generation time  
- Report open rate  
- Repeat uploads  
- Weekly active users  

---

## 11. Edge Cases
- Invalid file formatting  
- Too large dataset  
- Missing columns  
- WhatsApp delivery failed  

---

## 12. Tech Stack
Python, FastAPI, Plotly, Pandas, Twilio WhatsApp API, Supabase

---

## 13. Risks
- WhatsApp API rate limits  
- Incorrect AI insights  
- Data privacy concerns  

