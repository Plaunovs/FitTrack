# 💪 FitTrack – Fitness & Workout Tracker

Pilna stack web aplikācija lietotāju treniņu plānošanai, sasniegumu reģistrēšanai un progresu vizualizēšanai; ietver diagrammas, kaloriju aprēķinus un paziņojumus.

---

## 🎯 Mērķis
Aplikācija ļauj:
- Reģistrēties un droši ielogoties ar JWT autentifikāciju  
- Plānot treniņus ar datumiem, vingrinājumiem, atkārtojumiem un svaru  
- Reģistrēt sasniegumus un aprēķināt patērētās kalorijas  
- Sekot progresam ar vizualizācijām un diagrammām  
- [Šeit vari vēlāk pievienot informāciju par rikiem vai papildu funkcionalitāti]

---

## ⚙️ Izmantotās tehnoloģijas

**Back-end:**  
- Java 17+  
- Spring Boot  
- MySQL  
- JPA / Hibernate  
- Spring Security + JWT  

**Front-end:**  
- React.js  
- Tailwind CSS  
- Axios  
- Chart.js  
- React Router  

**Papildus:**  
- E-pasta paziņojumi ar Spring Mail  
- Docker izvietošana  

---

## 🗃️ Datubāzes shēma (vienkāršota)

| Tabula        | Kolonnas |
|---------------|----------|
| `users`       | id, name, email, password, role |
| `workouts`    | id, user_id (FK), date, title, notes |
| `exercises`   | id, workout_id (FK), name, sets, reps, weight |
| `achievements`| id, user_id (FK), workout_id (FK), calories_burned, notes |

---

## 🔌 API (REST) piemēri

| Metode | Endpoint | Apraksts |
|--------|----------|----------|
| POST   | `/api/auth/register` | Reģistrē jaunu lietotāju |
| POST   | `/api/auth/login` | Ielogojas un saņem JWT |
| GET    | `/api/workouts` | Saņem lietotāja treniņus |
| POST   | `/api/workouts` | Pievieno jaunu treniņu |
| PUT    | `/api/workouts/{id}` | Rediģē treniņu |
| DELETE | `/api/workouts/{id}` | Dzēš treniņu |
| GET    | `/api/workouts/{id}/exercises` | Saņem vingrinājumus |
| POST   | `/api/workouts/{id}/exercises` | Pievieno vingrinājumu |
| GET    | `/api/achievements` | Saņem lietotāja progresu |
| POST   | `/api/achievements` | Pievieno jaunu sasniegumu |

---

## 🖥️ Front-end funkcionalitāte

- **Login/Register** – lietotāju autentifikācija  
- **Dashboard** – pārskats par treniņiem, kalorijām, progresu  
- **Workout Planner** – treniņu pievienošana un rediģēšana  
- **Exercise Manager** – vingrinājumu pievienošana treniņiem  
- **Progress Charts** – diagrammas ar progresu (Chart.js)  

---
