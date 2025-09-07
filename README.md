# 🚀 AUS Course Swap – Project Timeline  

## 📅 1-Month Plan (5 Members)  

### **Week 1 — Setup & Foundations**  
**Milestone:** Core structure ready (frontend + backend + DB).  

- **Frontend (React + Tailwind)**  
  - Set up project structure with routing for 5 pages.  
  - Build static **Landing Page** (basic intro, CTA buttons).  
  - Build mock versions of **Signup/Login** (UI only, no backend).  

- **Backend (Django REST)**  
  - Initialize Django REST project.  
  - Define DB schema (Users, Courses, Sections, Requests, Matches, Invitations).  
  - Set up Supabase/Postgres connection.  

- **Database**  
  - Finalize ER diagram.  
  - Seed DB with mock course/section data.  

- **Scraper**  
  - Prototype course/section scraper (store into DB).  

- **DevOps**  
  - GitHub repo with branching rules.  
  - Basic CI/CD (Netlify/Vercel for frontend, Railway/Heroku for backend).  

---

### **Week 2 — Core Features (Requests Form + Auth)**  
**Milestone:** Students can create requests.  

- **Frontend**  
  - Connect **Signup/Login Page** to backend (AUS email only, hashed passwords).  
  - Build **Requests Form Page**:  
    - Case 1: Have → Want.  
    - Case 2: Want only.  
    - Case 3: Have → Drop.  
    - Allow multiple Have/Wants.  

- **Backend**  
  - Auth endpoints (signup, login, password reset).  
  - API to create/update/delete requests.  
  - API to fetch course/section data.  

- **Matching Logic (Phase 1)**  
  - Implement exact section-to-section matching.  
  - Return possible matches for a given request.  

- **Testing**  
  - Unit tests for auth + request creation.  
  - Verify scraper inserts courses correctly.  

---

### **Week 3 — My Matches + Dashboard (Swap Flow)**  
**Milestone:** Students can view matches, send/accept swaps.  

- **Frontend**  
  - Build **My Matches Page** → show suggested automatic matches.  
  - Build **Dashboard Page** → show:  
    - Received swap requests.  
    - Sent invitations.  
    - Completed swaps.  
  - Buttons for "Send Invitation", "Accept", "Decline".  

- **Backend**  
  - API for invitations (send, accept, decline).  
  - Swap confirmation logic (mark both requests as completed + remove from active list).  

- **Matching Logic (Phase 2)**  
  - Add fallback matching (same course, different sections).  

- **Integrations**  
  - Mock WhatsApp/email notification when swap is confirmed.  

- **Testing**  
  - End-to-end test: Student A posts → Student B matches → Invitation → Confirmation.  

---

### **Week 4 — Polish, Integrations & Deployment**  
**Milestone:** MVP live + stable.  

- **Frontend**  
  - Polish UI (mobile-first).  
  - Add badges for new matches/invitations.  
  - Improve dashboard navigation.  

- **Backend**  
  - Admin panel: refresh scraper, remove invalid requests.  
  - Optimize DB queries for matching.  

- **Integrations (Final)**  
  - Connect real WhatsApp API (Twilio/Meta).  
  - Add email fallback notifications.  

- **Testing & QA**  
  - Stress test with 500 mock users.  
  - Bug fixes + UX polish.  

- **Deployment**  
  - Finalize hosting (Vercel/Netlify + Railway/Heroku + Supabase).  
  - Write user/admin documentation.  

---

## 👥 Team Roles  

- **Member 1 (Frontend Lead)** → Landing + Signup/Login + routing.  
- **Member 2 (Frontend)** → Requests Form + My Matches UI.  
- **Member 3 (Backend Lead)** → Auth + Requests API + Matches API.  
- **Member 4 (DB & Scraper)** → Schema design, scraper integration, admin panel.  
- **Member 5 (QA & Integrations)** → Testing, WhatsApp/email integration, deployment.  
