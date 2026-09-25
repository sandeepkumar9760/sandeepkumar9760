<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=26&duration=3000&pause=1200&color=0E75B6&center=true&vCenter=true&width=650&lines=Hi%2C+I'm+Sandeep+Kumar;AI%2FML+Engineer+in+Progress;Backend+Developer;Problem+Solver" alt="Typing SVG" />

**AI/ML-focused software engineer building real products across machine learning, backend engineering, and intelligent applications.**

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/sandeepkumar9760)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sandeep-kumar-ds/)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:sandeepkumar270724@gmail.com)
[![X](https://img.shields.io/badge/X-000000?style=flat-square&logo=x&logoColor=white)](https://x.com/KumarSande73051)

</div>

<br>

## About Me

I'm a B.Tech Computer Science student at Lovely Professional University, specializing in Decision Science and Machine Learning. Most of my time splits between DSA practice, ML experimentation, and backend engineering — I'm more interested in what happens *after* a model works than in getting it to work in the first place.

My projects sit at the intersection of predictive analytics and production engineering: a churn-scoring pipeline served through FastAPI, a Chrome extension that routes LeetCode problems through a local LLM, a Django-based food-ordering platform for my campus, and a face-recognition attendance system backed by PostgreSQL. I care about the API contract and the schema as much as the model — a prediction that never gets served isn't a product.

---

## Currently Building & Learning

- Deepening backend engineering with **Django** and **FastAPI** — API design, database modeling, deployment
- Strengthening **ML engineering** fundamentals: production-oriented pipelines, model serving, experiment tracking with MLflow
- Working through **Trees, Graphs, and Dynamic Programming** after clearing the core DSA pattern set
- Reading into **system design fundamentals** — the layer above individual services
- Applying **PostgreSQL** more deliberately for schema design and query performance

---

## Tech Stack

<div align="center">

| Category | Stack |
|---|---|
| **Languages** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black) ![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=mysql&logoColor=white) |
| **Backend** | ![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![REST APIs](https://img.shields.io/badge/REST_APIs-000000?style=flat-square) |
| **Machine Learning & Data** | ![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white) ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white) ![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white) ![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat-square) ![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat-square) |
| **Databases** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) |
| **Frontend** | ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white) ![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=three.js&logoColor=white) |
| **DevOps & Tools** | ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white) ![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white) ![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black) |
| **AI / LLM** | ![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white) ![OpenAI](https://img.shields.io/badge/OpenAI_API-412991?style=flat-square&logo=openai&logoColor=white) |

</div>

---

## Featured Projects

### ChurnGuard — Customer Churn Intelligence Pipeline
An end-to-end churn workflow — from raw telecom data to a served prediction, not just a notebook metric.

**What it does**
- Predicts customer churn on the Telco dataset using an XGBoost classifier
- Handles class imbalance with SMOTE, applied only on training data to avoid leakage
- Explains individual predictions with SHAP so risk scores aren't a black box
- Serves predictions through a FastAPI REST API with single and batch scoring

**Technical Highlights**
- ~0.85 ROC-AUC on held-out test data
- `/predict` and `/predict/batch` endpoints with a live Swagger UI at `/docs`
- Feature preprocessing decoupled into a reusable module, separate from the API layer
- Streamlit dashboard for non-technical stakeholders to explore risk scores

**Stack:** `Python` `XGBoost` `SHAP` `FastAPI` `Streamlit` `Pandas`

🔗 [View Repository](https://github.com/sandeepkumar9760/Customer-Churn-Model)

---

### LeetCoach AI
A Chrome extension that turns any LeetCode problem into an interactive DSA coach, powered by a local LLM.

**What it does**
- Reads the current LeetCode problem directly off the page via a content script
- Sends it to a locally running Ollama model for explanation, approach, and complexity analysis
- Generates a ready-to-paste C++ solution in LeetCode's class format
- Runs entirely on-device — no problem data leaves the machine

**Technical Highlights**
- Manifest V3 Chrome extension talking to a FastAPI backend over a strict JSON contract
- Two dedicated endpoints (`/analyze`, `/generate-code`) with explicit handling for malformed model output
- Side-panel UI built in vanilla JS with no framework overhead

**Stack:** `JavaScript` `Chrome Extension (MV3)` `FastAPI` `Ollama` `Python`

🔗 [View Repository](https://github.com/sandeepkumar9760/LeetCoach-AI)

---

### AI Smart Attendance System
Camera-based attendance for classrooms — face detection and matching in place of the roll call.

**What it does**
- Captures a classroom image and detects every face in frame
- Matches detected faces against stored student encodings
- Marks present/absent automatically and logs it to the database
- Gives faculty a dashboard for class-wise and subject-wise attendance

**Technical Highlights**
- Face detection and encoding via OpenCV, `face_recognition`, and `dlib`
- Django backend with PostgreSQL for relational attendance records
- Single-session lock to prevent duplicate attendance entries

**Stack:** `Python` `Django` `OpenCV` `face_recognition` `PostgreSQL`

🔗 [View Repository](https://github.com/sandeepkumar9760/REAL-AI-BASED-SMART-ATTENDANCE-SYSTEM)

---

### BlockBites-LPU
A block-based food ordering platform built for LPU's campus food courts.

**What it does**
- Organizes food stalls by campus block so students order from the right queue
- Lets students browse menus, add items to a cart, and place orders
- Tracks order status in real time from placement to fulfillment
- Gives stall owners a dashboard for menu management and demand trends

**Technical Highlights**
- Django + PostgreSQL backend with a relational schema for blocks, stalls, menus, and orders
- Role-based access for students, stall owners, and admins
- Architecture left open for a future ML-based demand-forecasting layer

**Stack:** `Python` `Django` `PostgreSQL` `HTML` `CSS`

🔗 [View Repository](https://github.com/sandeepkumar9760/BlockBites-LPU)

---

## Engineering Mindset

```
Read the data  →  Build the smallest working version  →  Break it on purpose
       →  Measure what actually matters  →  Fix the real bottleneck  →  Ship it behind an API
```

---

## GitHub Analytics

<div align="center">
  <img src="https://github-readme-stats-black-six-62.vercel.app/api?username=sandeepkumar9760&show_icons=true&theme=tokyonight&hide_border=true&cache_seconds=1800" width="48%" />
  <img src="https://github-readme-stats-black-six-62.vercel.app/api/top-langs/?username=sandeepkumar9760&layout=compact&theme=tokyonight&hide_border=true&cache_seconds=1800" width="48%" />
</div>

<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=sandeepkumar9760&theme=tokyonight&hide_border=true" />
</div>

<div align="center">
  <img src="https://raw.githubusercontent.com/sandeepkumar9760/sandeepkumar9760/output/github-contribution-grid-snake.svg" alt="Contribution Snake" />
</div>

---

## DSA / Problem Solving

| Area | Patterns Practiced |
|---|---|
| **Arrays & Strings** | Two Pointers, Sliding Window, Prefix Sum, Kadane's Algorithm |
| **Linked Lists** | Fast & Slow Pointers, In-place Reversal |
| **Searching** | Binary Search |
| **Data Structures** | HashMap, Stack, Heap |
| **Intervals** | Merge Intervals |
| **Advanced** | Recursion, Backtracking, Trees, Graphs, Dynamic Programming *(in progress)* |

---

## Connect

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/sandeepkumar9760)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sandeep-kumar-ds/)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:sandeepkumar270724@gmail.com)
[![X](https://img.shields.io/badge/X-000000?style=flat-square&logo=x&logoColor=white)](https://x.com/KumarSande73051)

</div>

<div align="center">
<sub>Open to Software Engineer, ML Engineer, and Data Scientist roles — happy to talk through any project above.</sub>
</div>
