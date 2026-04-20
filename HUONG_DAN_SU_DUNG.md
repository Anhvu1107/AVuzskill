# Huong Dan Su Dung

File nay la diem vao nhanh de dung bo `agent-skills-unified` ma khong can doc toan bo repo.

## Muc Tieu

Bo nay duoc lam de ca nguoi va AI khac co the vao repo, hieu nen doc gi truoc, chon dung skill, lam dung thu tu, va tu kiem tra chat luong truoc khi ket thuc.

## Cach Dung Nhanh Nhat

Neu khong chac nen dung skill nao, hay bat dau bang:

```text
Use $workspace-operating-system to decide the right skill stack for this task.
```

Day la skill trung tam. No giup:

- phan loai task
- chon skill chinh va skill phu
- quyet dinh thu tu lam viec
- nhac AI phai verify truoc khi chot

## Khi Nao Dung Skill Trung Tam

Hay bat dau bang `$workspace-operating-system` khi:

- task con mo ho
- task lon hoac nhieu buoc
- task dung nhieu domain cung luc
- ban muon AI tu chon quy trinh lam viec tot nhat
- ban muon AI giai thich vi sao no chon skill do

## Khi Nao Goi Thang Skill Chuyen Biet

Goi truc tiep skill khi ban da biet ro viec can lam.

Vi du:

- UI, landing page, component:
```text
Use $frontend-design to redesign this page and keep the UX clear.
```

- test trinh duyet, kiem tra flow web:
```text
Use $webapp-testing to inspect the app and verify the main user flow.
```

- tao MCP server:
```text
Use $mcp-builder to design and implement an MCP server for this API.
```

- thiet ke API:
```text
Use $api-patterns to design this endpoint and response format.
```

- schema database:
```text
Use $database-design to propose the schema and indexing strategy.
```

- debug:
```text
Use $systematic-debugging to find the root cause of this issue.
```

- co san plan va muon AI thi cong theo dung trinh tu:
```text
Use $executing-plans to follow this plan step by step and verify each stage.
```

- muon AI lam den noi den chon, co acceptance criteria ro:
```text
Use $closed-loop-delivery to finish this task end to end and prove the result.
```

- dang xu ly review comments:
```text
Use $receiving-code-review to triage these comments, fix valid issues, and verify them.
```

- review code:
```text
Use $code-review-checklist to review these changes for bugs and risks.
```

## Quy Tac Thuc Chien

1. Khong chac thi bat dau bang `$workspace-operating-system`.
2. Chac domain roi thi goi thang skill chinh.
3. Task lon thi de AI ghep nhieu skill theo thu tu.
4. Task code thi luon yeu cau verify hoac test sau khi sua.
5. Task review thi uu tien bug, regression, missing test truoc phan style.
6. Neu task da co plan, dung `$executing-plans` thay vi de AI vua nghi vua che lai ke hoach.
7. Neu task can "done that su", dung them `$verification-before-completion` hoac goi thang `$closed-loop-delivery`.

## Quy Trinh Khuyen Dung

### 1. Task moi hoac nhieu domain

```text
Use $workspace-operating-system to choose the right skills and execution order for building this feature.
```

### 2. Task UI

```text
Use $frontend-design to define the visual direction, hierarchy, and implementation approach for this interface.
```

### 3. Task bug

```text
Use $workspace-operating-system to route this bug, then use the right debugging and verification skills.
```

### 4. Task review feedback

```text
Use $receiving-code-review to process these review comments, apply valid fixes, and verify them.
```

### 5. Task review

```text
Use $workspace-operating-system to choose the right review stack, then review this code with a risk-first mindset.
```

### 6. Task thi cong theo plan

```text
Use $executing-plans to implement this approved plan without drifting from scope.
```

### 7. Task can chot den noi den chon

```text
Use $closed-loop-delivery to finish this task end to end and only stop when the acceptance criteria are proven.
```

### 8. Task tai lieu, brief, hoac noi dung can trinh bay ro

Goi theo huong viet va dieu phoi noi dung:

- `$doc-coauthoring`
- `$internal-comms`
- Them `$brand-guidelines` neu can chuan hoa giong thuong hieu

## Cau Truc Can Biet

- `.agent/skills/`
  - thu vien skill chinh va la cay skill chuan duy nhat
- `.agent/agents/`
  - chuyen gia theo vai tro
- `.agent/workflows/`
  - workflow dieu phoi
- `.agent/skills/workspace-operating-system/`
  - skill trung tam
- `.agent/skills/workspace-operating-system/references/task-routing.md`
  - map nhanh tu loai task sang skill phu hop
- `.agent/skills/workspace-operating-system/references/composition-patterns.md`
  - cach ghep nhieu skill voi nhau
- `.agent/skills/workspace-operating-system/references/quality-bar.md`
  - chuan toi thieu truoc khi ket thuc task
- `.agent/skills/workspace-operating-system/references/skill-catalog.md`
  - danh sach day du cac skill hien co

## Prompt Mau Co The Copy Ngay

### Prompt tong quat

```text
Use $workspace-operating-system to understand this request, pick the minimum effective skill stack, do the work, and verify the result before finishing.
```

### Prompt build feature

```text
Use $workspace-operating-system to build this feature end-to-end, including planning, implementation, and verification.
```

### Prompt sua bug

```text
Use $workspace-operating-system to route this issue, identify the root cause, patch it, and verify the fix.
```

### Prompt lam UI

```text
Use $frontend-design to improve this UI with a stronger visual direction and better UX clarity.
```

### Prompt kiem tra web

```text
Use $webapp-testing to inspect the app, discover selectors, and verify the key user journeys.
```

## Cach Nang Cap Sau Nay

Neu ban them hoac sua skill:

1. cap nhat `SKILL.md` cua skill do
2. neu skill loi thi them `agents/openai.yaml`
3. chay lai script build catalog:

```text
python .agent/skills/workspace-operating-system/scripts/build_skill_catalog.py
```

## Ghi Chu Quan Trong

- Bo nay da dung duoc ngay.
- Bay gio chi con mot cay skill chuan la `.agent/skills/`.
- Repo nay da duoc gop that su, khong con hai thu vien skill song song nua.
- Mac dinh repo nay la local-first: khong bat san MCP server ben ngoai.
- 4 skill file van phong co license han che da duoc go bo khoi ban public cua bundle.
- Cac workflow moi duoc viet lai theo he Codex hien tai, khong import launcher hay app shell tu bundle la vao cay skill chinh.

## Cau Mo Dau Tot Nhat

Neu chi chon dung mot cau de bat dau, hay dung:

```text
Use $workspace-operating-system to decide what to do first, which skills to load, and how to verify the result.
```
