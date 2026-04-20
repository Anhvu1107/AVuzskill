# So Tay Van Hanh

File nay la manual tong cho `agent-skills-unified`.

Neu can bat dau nhanh, doc `HUONG_DAN_SU_DUNG.md`.
Neu can hieu day du cach bo nay van hanh, duoc mo rong, duoc harden, va duoc bao tri, doc file nay.

## 1. Muc Tieu

Bo nay khong phai chi la mot thu vien skill.

No la mot he van hanh cho AI agent:

- biet nen doc gi truoc
- biet chon skill nao dung
- biet khi nao can ghep nhieu skill
- biet cach verify truoc khi chot
- biet cach nang cap bundle ma khong lam no rot vao tinh trang tap nham, mo ho, hoac kho trigger

## 2. Tu Duy Nen Dung

Hay nhin bundle nay theo 4 lop:

1. `workspace-operating-system`
   - lop dieu phoi trung tam
2. `skills/`
   - tri thuc va workflow theo domain
3. `agents/`
   - prompt chuyen gia theo vai tro
4. `workflows/`
   - diem vao theo kieu command/procedure

Them vao do:

- `rules/`
  - rang buoc toan cuc
- `scripts/`
  - helper va validator
- `.shared/`
  - tai nguyen dung chung

## 3. Cau Truc Chuan

Root repo:

- `README.md`
  - giai thich repo la gi
- `HUONG_DAN_SU_DUNG.md`
  - quick start
- `SO_TAY_VAN_HANH.md`
  - manual tong
- `BAO_CAO_HARDENING.md`
  - lich su va nguyen tac lam sach/hardening

Runtime tree:

- `.agent/skills/`
  - thu vien skill canonical duy nhat
- `.agent/agents/`
  - 20 agent prompts
- `.agent/workflows/`
  - 11 workflow entry points
- `.agent/rules/`
  - 1 global rule file
- `.agent/scripts/`
  - helper/validation scripts
- `.agent/.shared/`
  - shared assets

Tinh trang hien tai:

- `54` skills
- `20` agents
- `11` workflows
- `1` rules file

## 4. Thu Tu AI Nen Doc Khi Vao Repo

Day la trinh tu de mot AI moi vao repo va van hanh dung:

1. Doc `.agent/skills/workspace-operating-system/SKILL.md`
2. Doc:
   - `.agent/skills/workspace-operating-system/references/task-routing.md`
   - `.agent/skills/workspace-operating-system/references/quality-bar.md`
3. Neu task nhieu domain:
   - doc them `composition-patterns.md`
4. Neu chua chac skill nao:
   - doc `skill-catalog.md`
5. Sau do moi doc `SKILL.md` cua skill chinh
6. Chi doc `references/` khi thuc su can
7. Neu task can role chuyen biet:
   - doc agent phu hop trong `.agent/agents/`
8. Neu task theo kieu command/process co san:
   - doc workflow phu hop trong `.agent/workflows/`

Nguyen tac:

- di tu tong quan -> route -> skill chinh -> reference sau
- khong doc lan tung folder mot cach mu quang
- khong load het context neu task khong can

## 5. Entry Point Chuan

Mac dinh, cau mo dau tot nhat la:

```text
Use $workspace-operating-system to decide the right skill stack, sequence the work, and verify the result.
```

Dung entry nay khi:

- task mo ho
- task lon
- task nhieu domain
- task co gia tri cao
- task can quality bar ro rang

## 6. Cach Route Task

### 6.1 Task mo rong ung dung

Dung:

- `app-builder`
- support: `architecture`, `frontend-design`, `api-patterns`, `database-design`, `deployment-procedures`, `closed-loop-delivery`

### 6.2 Task kien truc

Dung:

- `architecture`

Doc them:

- `references/decision-playbook.md`
- `references/adr-checklist.md`

### 6.3 Task API

Dung:

- `api-patterns`

Doc them:

- `references/contract-playbook.md`
- `references/api-review-checklist.md`

### 6.4 Task UI/frontend

Dung:

- `frontend-design`
- support tuy task: `web-design-guidelines`, `tailwind-patterns`, `nextjs-react-expert`, `mobile-design`

### 6.5 Task debug

Dung:

- `systematic-debugging`
- support: domain skill lien quan
- verify them bang `webapp-testing` hoac `testing-patterns`

### 6.6 Task can done-that-su

Dung:

- `closed-loop-delivery`
- support:
  - `verification-before-completion`
  - `receiving-code-review`
  - `webapp-testing`

### 6.7 Task da co plan

Dung:

- `executing-plans`
- support:
  - `using-git-worktrees`
  - `parallel-agents`
  - `verification-before-completion`

### 6.8 Task review feedback

Dung:

- `receiving-code-review`

Khac voi:

- `code-review-checklist`
  - dung khi chinh minh di review code

### 6.9 Task hieu nang React/Next.js

Dung:

- `nextjs-react-expert`

Doc them:

- `references/performance-investigation-playbook.md`
- `references/app-router-checklist.md`

## 7. Nguyen Tac Thiet Ke Skill

Bo nay dang theo mot rule rat quan trong:

- `SKILL.md` phai gon, ro trigger, ro workflow
- tri thuc sau dua xuong `references/`

Ly do:

- `SKILL.md` qua dai se trigger kem
- AI can mot lop dieu phoi gon de load nhanh
- tri thuc senior-grade nen duoc luu thanh playbook/checklist/matrix o `references/`

Mau ly tuong cua mot skill:

- `SKILL.md`
  - khi nao dung
  - quy trinh chinh
  - related skills
- `references/`
  - playbook
  - decision matrix
  - review checklist
  - advanced heuristics
- `agents/openai.yaml`
  - metadata de discover/invoke dep hon

## 8. Catalog Skill Chinh

De xem day du tat ca skill:

- `.agent/skills/workspace-operating-system/references/skill-catalog.md`

Nhom skill quan trong nhat:

- Operating:
  - `workspace-operating-system`
  - `closed-loop-delivery`
  - `executing-plans`
  - `parallel-agents`
  - `plan-writing`
  - `verification-before-completion`
  - `using-git-worktrees`
  - `finishing-a-development-branch`
- Product and architecture:
  - `app-builder`
  - `architecture`
  - `api-patterns`
  - `database-design`
  - `mcp-builder`
- Frontend:
  - `frontend-design`
  - `web-design-guidelines`
  - `tailwind-patterns`
  - `nextjs-react-expert`
  - `mobile-design`
- Quality:
  - `systematic-debugging`
  - `testing-patterns`
  - `tdd-workflow`
  - `webapp-testing`
  - `receiving-code-review`
  - `code-review-checklist`

## 9. Catalog Agent

Day la 20 agent hien co trong `.agent/agents/`:

- `backend-specialist`
  - backend, server, API, auth, database integration
- `code-archaeologist`
  - legacy code, repo analysis, modernization
- `database-architect`
  - schema, migrations, indexing, data modeling
- `debugger`
  - root cause, crash investigation, production issue
- `devops-engineer`
  - deployment, rollback, CI/CD, server operations
- `documentation-writer`
  - docs khi user yeu cau ro rang
- `explorer-agent`
  - deep codebase discovery
- `frontend-specialist`
  - React/Next.js UI architecture
- `game-developer`
  - game logic va engines
- `mobile-developer`
  - React Native, Flutter, mobile patterns
- `orchestrator`
  - dieu phoi nhieu agent
- `penetration-tester`
  - offensive security
- `performance-optimizer`
  - profiling, speed, bundle
- `product-manager`
  - requirements, acceptance criteria
- `product-owner`
  - backlog, MVP, strategic prioritization
- `project-planner`
  - planning va breakdown
- `qa-automation-engineer`
  - e2e, regression, automation infra
- `security-auditor`
  - OWASP, auth, supply chain, security review
- `seo-specialist`
  - SEO va GEO
- `test-engineer`
  - tests, TDD, coverage

Nguyen tac dung agent:

- dung agent khi role thuc su quan trong voi task
- khong thay agent cho skill; agent va skill la 2 lop khac nhau
- skill lo tri thuc/quy trinh
- agent lo goc nhin va vai tro

## 10. Catalog Workflow

11 workflow hien co trong `.agent/workflows/`:

- `brainstorm.md`
  - structured brainstorming
- `create.md`
  - tao ung dung moi
- `debug.md`
  - dieu tra loi co he thong
- `deploy.md`
  - deployment flow
- `enhance.md`
  - nang cap feature hien co
- `orchestrate.md`
  - dieu phoi nhieu agent
- `plan.md`
  - lap ke hoach
- `preview.md`
  - quan ly preview/local server
- `status.md`
  - theo doi trang thai
- `test.md`
  - sinh/chay tests
- `ui-ux-pro-max.md`
  - luong thao tac UI

Luu y:

- workflows la diem vao theo process
- skills van la lop tri thuc canonical
- neu workflow cu/legacy xung dot voi `workspace-operating-system`, uu tien routing tu skill trung tam

## 11. Rules

Hien tai co 1 global rule file:

- `.agent/rules/GEMINI.md`

Vai tro cua no:

- giu compatibility voi mot so he cu
- mo ta framework-style behavior rong

Nhung can hieu ro:

- runtime canonical hien tai van nen bat dau tu `workspace-operating-system`
- `GEMINI.md` la file inherited legacy, khong nen tiep tuc phinh to no
- rule moi nen ngan, ro, va toi gian

Khuyen nghi:

- de `rules/` cho rang buoc that su toan cuc
- de logic route/execution o `skills/workspace-operating-system`
- de domain knowledge o `skills/*`

## 12. Rule Uu Tien

Trong repo nay, nen nghi theo thu tu:

1. user request
2. `workspace-operating-system`
3. skill chinh cua task
4. reference cua skill do
5. agent role neu co dung agent
6. workflow neu task vao theo workflow
7. global rules de giu compatibility

Nguyen tac don gian:

- rule nao cu the hon va gan task hon thi uu tien de lam viec
- rule nao cu/legacy ma mau thuan voi he canonical moi thi phai review can than

## 13. Prompt Mau Cho Human

### Route tong quat

```text
Use $workspace-operating-system to route this task, choose the minimum effective skill stack, and verify the result.
```

### Build app

```text
Use $app-builder to shape this product request, choose the stack, and plan the next implementation steps.
```

### Architecture

```text
Use $architecture to compare realistic system options and recommend the best architecture with tradeoffs.
```

### API

```text
Use $api-patterns to design the API style, response contract, auth, and versioning for this system.
```

### End-to-end delivery

```text
Use $closed-loop-delivery to finish this task end to end and prove the acceptance criteria.
```

### Review feedback

```text
Use $receiving-code-review to process these review comments, apply valid fixes, and verify them.
```

### Performance

```text
Use $nextjs-react-expert to find the main bottleneck and optimize this React or Next.js flow deliberately.
```

## 14. Cac Quy Trinh Vang

### 14.1 Build feature lon

Trinh tu nen dung:

1. `workspace-operating-system`
2. `app-builder` hoac `architecture`
3. `plan-writing`
4. `executing-plans`
5. domain skills
6. `verification-before-completion`
7. `finishing-a-development-branch`

### 14.2 Sua bug kho

1. `workspace-operating-system`
2. `systematic-debugging`
3. domain skill lien quan
4. `testing-patterns` hoac `webapp-testing`
5. `verification-before-completion`

### 14.3 Xu ly review feedback

1. `receiving-code-review`
2. domain skill
3. `verification-before-completion`
4. neu can done-that-su -> `closed-loop-delivery`

### 14.4 Performance pass

1. `nextjs-react-expert`
2. `performance-profiling`
3. `frontend-design` neu co tac dong UX
4. `verification-before-completion`

## 15. Cach Them Skill Moi

Khi them skill moi:

1. Tao folder trong `.agent/skills/<skill-name>/`
2. Tao `SKILL.md`
3. Neu can tri thuc sau:
   - tao `references/`
4. Neu can metadata dep:
   - tao `agents/openai.yaml`
5. Neu can helper repeatable:
   - tao `scripts/`
6. Chay lai:

```text
python .agent/skills/workspace-operating-system/scripts/build_skill_catalog.py
```

Checklist truoc khi commit:

- ten folder va `name:` trong frontmatter phai khop
- `description:` phai noi ro khi nao dung
- tat ca reference trong `SKILL.md` phai ton tai
- khong nhac file/duong dan he cu sai context
- khong import launcher/app shell la vao cay runtime

## 16. Cach Nang Cap Skill Cu

Khi mot skill cu qua rong, mo ho, hoac mang dau vet inherited source:

1. Rut gon `SKILL.md`
2. Lam ro:
   - khi nao dung
   - quy trinh chinh
   - related skills
3. Chuyen tri thuc sau xuong `references/`
4. Them checklist/playbook senior-grade
5. Them `agents/openai.yaml` neu skill quan trong
6. Rebuild catalog

Day la cach bundle nay da duoc nang cap.

## 17. Cach Bao Tri Agent

Khi sua `agents/*.md`:

- mo ta ro role
- giai thich khi nao nen dung
- khong de agent tro thanh ban sao cua skill
- de skill cung cap tri thuc
- de agent cung cap goc nhin, tone, va vung trach nhiem

Agent tot nen:

- co description ro trigger
- biet no dung skill nao
- khong noi qua nhieu ve framework cu neu runtime da doi

## 18. Cach Bao Tri Workflow

Khi sua `workflows/*.md`:

- xem no la entry procedure, khong phai skill thay the
- giu command flow ro
- neu logic da duoc skill trung tam quan ly tot hon, workflow nen don gian hoa
- tranh de workflow override triet ly canonical moi ma khong co ly do

## 19. Hardening Va Ownership

Nguyen tac dang dung:

- local-first
- khong bat san MCP ngoai
- khong ship file nhay cam
- khong import raw launcher/app shell tu bundle ngoai vao `.agent`
- khi go bundle ngoai vao:
  - audit
  - loc
  - viet lai/cherry-pick
  - khong merge nguyen cay runtime cua no vao canonical tree

Xem them:

- `BAO_CAO_HARDENING.md`

## 20. Release Checklist

Truoc khi push:

1. cap nhat file can thiet
2. rebuild catalog neu inventory/description doi
3. kiem tra reference link khong gay
4. chay:

```text
git diff --check
```

5. doc lai:
   - `README.md`
   - `HUONG_DAN_SU_DUNG.md`
   - `SO_TAY_VAN_HANH.md`
   neu thay doi tac dong den cach dung
6. commit ro nghia
7. push `main`

## 21. Dau Hieu He Dang Xau Di

Can canh giac neu thay:

- skill ten mot dang, folder mot nẻo
- `SKILL.md` phinh to va lap y
- trieu skill trigger trung nhau
- reference khong ton tai
- inherited wording cu xuat hien o core skill
- workflow/agent/rule noi nguoc voi canonical flow
- catalog khong rebuild sau khi sua frontmatter

## 22. Quy Tac Vang Cuoi Cung

Bo nay huong toi chuan:

- ro trigger
- giau tri thuc
- it mo ho
- quality bar ro
- verification truoc khi chot
- phong cach senior dev thuc thu

Neu phai chon giua:

- dai nhung mo ho
- va
- gon nhung ro + co reference sau

thi chon ve sau.
