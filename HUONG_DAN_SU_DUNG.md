# Hướng Dẫn Sử Dụng

File này là điểm vào nhanh để dùng bộ `agent-skills-unified` mà không cần đọc toàn bộ repo.

## Mục Tiêu

Bộ này được làm để cả người và AI khác có thể vào repo, hiểu nên đọc gì trước, chọn đúng skill, làm đúng thứ tự, và tự kiểm tra chất lượng trước khi kết thúc.

## Cách Dùng Nhanh Nhất

Nếu không chắc nên dùng skill nào, hãy bắt đầu bằng:

```text
Use $workspace-operating-system to decide the right skill stack for this task.
```

Đây là skill trung tâm. Nó giúp:

- phân loại task
- chọn skill chính và skill phụ
- quyết định thứ tự làm việc
- nhắc AI phải verify trước khi chốt

## Khi Nào Dùng Skill Trung Tâm

Hãy bắt đầu bằng `$workspace-operating-system` khi:

- task còn mơ hồ
- task lớn hoặc nhiều bước
- task đụng nhiều domain cùng lúc
- bạn muốn AI tự chọn quy trình làm việc tốt nhất
- bạn muốn AI giải thích vì sao nó chọn skill đó

## Khi Nào Gọi Thẳng Skill Chuyên Biệt

Gọi trực tiếp skill khi bạn đã biết rõ việc cần làm.

Ví dụ:

- UI, landing page, component:
```text
Use $frontend-design to redesign this page and keep the UX clear.
```

- test trình duyệt, kiểm tra flow web:
```text
Use $webapp-testing to inspect the app and verify the main user flow.
```

- tạo MCP server:
```text
Use $mcp-builder to design and implement an MCP server for this API.
```

- thiết kế API:
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

- review code:
```text
Use $code-review-checklist to review these changes for bugs and risks.
```

## Quy Tắc Thực Chiến

1. Không chắc thì bắt đầu bằng `$workspace-operating-system`.
2. Chắc domain rồi thì gọi thẳng skill chính.
3. Task lớn thì để AI ghép nhiều skill theo thứ tự.
4. Task code thì luôn yêu cầu verify hoặc test sau khi sửa.
5. Task review thì ưu tiên bug, regression, missing test trước phần style.

## Quy Trình Khuyên Dùng

### 1. Task mới hoặc nhiều domain

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

### 4. Task review

```text
Use $workspace-operating-system to choose the right review stack, then review this code with a risk-first mindset.
```

### 5. Task tài liệu hoặc file văn phòng

Gọi thẳng skill chuyên loại file:

- `$docx`
- `$pptx`
- `$xlsx`
- `$pdf`

## Cấu Trúc Cần Biết

- `skills/`
  - thư viện skill chính
- `.agent/`
  - phần runtime, workflows, agents và cấu hình hỗ trợ
- `skills/workspace-operating-system/`
  - skill trung tâm
- `skills/workspace-operating-system/references/task-routing.md`
  - map nhanh từ loại task sang skill phù hợp
- `skills/workspace-operating-system/references/composition-patterns.md`
  - cách ghép nhiều skill với nhau
- `skills/workspace-operating-system/references/quality-bar.md`
  - chuẩn tối thiểu trước khi kết thúc task
- `skills/workspace-operating-system/references/skill-catalog.md`
  - danh sách đầy đủ các skill hiện có

## Prompt Mẫu Có Thể Copy Ngay

### Prompt tổng quát

```text
Use $workspace-operating-system to understand this request, pick the minimum effective skill stack, do the work, and verify the result before finishing.
```

### Prompt build feature

```text
Use $workspace-operating-system to build this feature end-to-end, including planning, implementation, and verification.
```

### Prompt sửa bug

```text
Use $workspace-operating-system to route this issue, identify the root cause, patch it, and verify the fix.
```

### Prompt làm UI

```text
Use $frontend-design to improve this UI with a stronger visual direction and better UX clarity.
```

### Prompt kiểm tra web

```text
Use $webapp-testing to inspect the app, discover selectors, and verify the key user journeys.
```

## Cách Nâng Cấp Sau Này

Nếu bạn thêm hoặc sửa skill:

1. cập nhật `SKILL.md` của skill đó
2. nếu skill lõi thì thêm `agents/openai.yaml`
3. chạy lại script build catalog:

```text
python skills/workspace-operating-system/scripts/build_skill_catalog.py
```

## Ghi Chú Quan Trọng

- Bộ này đã dùng được ngay.
- Một số app có thể hiển thị path trùng giữa `.agent/skills` và `skills/` vì `.agent/skills` đang trỏ sang cùng một thư viện.
- Về logic sử dụng thì không ảnh hưởng.

## Câu Mở Đầu Tốt Nhất

Nếu chỉ chọn đúng một câu để bắt đầu, hãy dùng:

```text
Use $workspace-operating-system to decide what to do first, which skills to load, and how to verify the result.
```
