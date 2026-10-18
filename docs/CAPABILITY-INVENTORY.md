# 📦 CAPABILITY-INVENTORY.md

**Project:** KnowledgeStations  
**Phase:** 1 — DISCOVER EXISTING CAPABILITIES  
**Date:** 2026-10-18  
**Status:** Draft (Pending Review)

---

## 1. ĐÃ TỒN TẠI (Có thể tái sử dụng)

### 1.1. File Upload & Storage
- [x] **Browser File API** — Upload file từ client (PDF, DOCX, PPTX, images, video)
- [x] **Browser LocalStorage** — Lưu trữ tạm thời dữ liệu người dùng (MVP)
- [x] **IndexedDB** — Lưu trữ offline cho file lớn (>5MB)
- [x] **GitHub Pages** — Hosting static files (deployment target)

### 1.2. AI & LLM Integration
- [x] **OpenAI API (GPT-4o)** — Text generation, summarization, quiz creation
- [x] **Anthropic API (Claude)** — Alternative LLM for content generation
- [x] **Google Gemini API** — Alternative LLM with multimodal support
- [x] **Hugging Face Inference API** — Self-hosted model access
- [x] **LangChain / LlamaIndex** — Framework for RAG pipeline

### 1.3. Vector Database (RAG)
- [x] **Pinecone** — Managed vector database for semantic search
- [x] **pgvector (PostgreSQL extension)** — Open-source vector similarity search
- [x] **ChromaDB** — Local/embedded vector database (good for MVP)

### 1.4. Document Parsing
- [x] **pdf.js / pdf-parse** — Extract text from PDF
- [x] **mammoth.js** — Convert DOCX to HTML/text
- [x] **pptx-parser** — Extract content from PowerPoint
- [x] **Tesseract.js** — OCR for images (if needed)
- [x] **youtube-transcript-api** — Extract transcript from YouTube videos

### 1.5. UI Framework & Components
- [x] **Next.js / React** — Frontend framework
- [x] **Tailwind CSS** — Utility-first CSS framework
- [x] **Lucide React** — Icon library
- [x] **Framer Motion** — Animation library (for Duolingo-style interactions)
- [x] **React Flow / D3.js** — Graph/tree visualization (for Skill Tree)

### 1.6. Authentication & Backend
- [x] **Supabase Auth** — User authentication (email, OAuth)
- [x] **Firebase Auth** — Alternative authentication provider
- [x] **Supabase Database** — PostgreSQL with real-time sync
- [x] **Firebase Firestore** — NoSQL database with offline support

### 1.7. Testing & Quality
- [x] **Jest / Vitest** — Unit testing framework
- [x] **React Testing Library** — Component testing
- [x] **Playwright / Cypress** — E2E testing

---

## 2. CẦN XÂY MỚI (Core Capabilities for KnowledgeStations)

### 2.1. Document Processing Pipeline
- [ ] **document-upload** — Handle multi-format file upload with validation (max 150MB)
- [ ] **document-parse** — Extract text/content from PDF, DOCX, PPTX, images, video, web links
- [ ] **context-extractor** — Understand document context and structure (AI-powered)
- [ ] **chunk-strategy** — Split document into logical chunks for processing

### 2.2. Knowledge Station Generation
- [ ] **station-recommender** — AI đề xuất số lượng trạm tối ưu (2-50) dựa trên độ dài tài liệu
- [ ] **station-creator** — Tạo cấu trúc trạm kiến thức (5 thành phần: summary, example, quiz, exercise, feedback)
- [ ] **quiz-generator** — Tạo 3-5 câu trắc nghiệm per station (AI-generated hoặc extracted)
- [ ] **exercise-generator** — Tạo 1 bài tập tự luận per station
- [ ] **feedback-engine** — AI chấm điểm và giải thích bài tập tự luận

### 2.3. Skill Tree Management
- [ ] **skill-tree-builder** — Xây dựng cấu trúc cây kỹ năng với nhánh rẽ
- [ ] **station-unlocker** — Logic mở khóa trạm dựa trên tiến độ
- [ ] **progress-tracker** — Theo dõi tiến độ học tập per station
- [ ] **branch-logic** — Quản lý nhánh rẽ và điều kiện mở khóa

### 2.4. Gamification System
- [ ] **xp-system** — Tính toán và cộng điểm XP
- [ ] **streak-tracker** — Theo dõi chuỗi ngày học liên tục
- [ ] **hearts-system** — Quản lý mạng sống (giảm khi làm sai, hồi phục theo thời gian)
- [ ] **badge-manager** — Cấp huy hiệu dựa trên achievements
- [ ] **leaderboard-engine** — Bảng xếp hạng người dùng
- [ ] **quest-manager** — Quản lý daily quests và missions
- [ ] **achievement-unlocker** — Unlock achievements based on milestones
- [ ] **currency-manager** — Quản lý tiền ảo (nếu có)

### 2.5. AI Engine Orchestration
- [ ] **llm-router** — Chuyển đổi linh hoạt giữa GPT-4o, Claude, Gemini, self-hosted
- [ ] **ai-off-mode** — Chế độ chạy offline với dữ liệu pre-generated
- [ ] **rag-pipeline** — Retrieval-Augmented Generation với Vector DB
- [ ] **prompt-builder** — Xây dựng prompt tối ưu cho từng tác vụ
- [ ] **response-validator** — Kiểm tra và validate response từ AI

### 2.6. User Management
- [ ] **user-auth** — Đăng ký, đăng nhập, session management
- [ ] **profile-manager** — Quản lý thông tin người dùng
- [ ] **progress-sync** — Đồng bộ tiến độ từ local lên cloud
- [ ] **json-exporter** — Xuất điểm số/đánh giá dạng JSON

### 2.7. UI/UX Components (Duolingo-style)
- [ ] **skill-tree-visualizer** — Hiển thị cây kỹ năng trực quan
- [ ] **station-card** — Card hiển thị thông tin trạm
- [ ] **quiz-interface** — Giao diện làm bài trắc nghiệm
- [ ] **exercise-interface** — Giao diện làm bài tự luận
- [ ] **feedback-modal** — Modal hiển thị AI feedback
- [ ] **progress-bar** — Thanh tiến độ tổng quan
- [ ] **gamification-hud** — HUD hiển thị XP, streaks, hearts, badges

---

## 3. PRIORITY MATRIX (Ma trận ưu tiên cho MVP)

### 🔴 HIGH PRIORITY (Phase 1 MVP)
1. document-upload
2. document-parse
3. station-recommender
4. station-creator
5. quiz-generator
6. skill-tree-builder
7. progress-tracker
8. llm-router
9. user-auth
10. skill-tree-visualizer

### 🟡 MEDIUM PRIORITY (Phase 2)
1. feedback-engine
2. xp-system
3. streak-tracker
4. hearts-system
5. badge-manager
6. rag-pipeline
7. progress-sync

###  LOW PRIORITY (Phase 3+)
1. leaderboard-engine
2. quest-manager
3. achievement-unlocker
4. currency-manager
5. ai-off-mode (advanced)

---

## 4. NEXT STEPS

✅ **Phase 1 Complete** — Capability Inventory đã được liệt kê  
⏭️ **Phase 2: CAPABILITY DECOMPOSITION** — Phân rã các capability thành sub-capabilities và vẽ Capability Tree  
⏭️ **Phase 3: DEFINE CONTRACTS** — Định nghĩa hợp đồng cho các capability quan trọng

---

**Approval Gate:** Chờ người dùng phê duyệt trước khi chuyển sang Phase 2.