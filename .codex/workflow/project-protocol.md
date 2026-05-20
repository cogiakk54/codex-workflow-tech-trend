# .codex/workflow/project-protocol.md — Giao thức quy trình (Ưu tiên cao nhất)

## Nhận dạng dự án

- **Tên dự án**: Tech Trend
- **Project root**: D:\work\ai-learning\codex-workflow\tech-trend
- **Workflow version**: snmb-webapp v1.0.0
- **Workflow docs path**: C:\Users\cogia\.codex\plugins\cache\local-workflows\snmb-workflow\1.0.0\references\workflow-docs
- **Khởi tạo**: 2026-05-20T14:28:04.0552700+07:00

## Quy tắc cốt lõi — KHÔNG ĐƯỢC VI PHẠM

1. Đầu mỗi session: READ `.codex/workflow/workflow-state.md` trước khi làm bất cứ điều gì.
2. Cuối mỗi bước: UPDATE `.codex/workflow/workflow-state.md` và APPEND `.codex/workflow/audit-trail.md`.
3. No TBD: Không báo hoàn thành khi còn placeholder `{...}` hoặc "TBD".
4. No Tech Hardcoding trước Bước 03: Không ghi tên framework hoặc DB cụ thể trong docs discovery.
5. Human First: Không tự giả định khi thiếu thông tin — phải hỏi human.
6. QA Signs Off: Developer không tự mark task done. Chỉ qa-engineer sign off.
7. Gate thứ tự: Kiểm tra prerequisite artifacts trước khi bắt đầu bước mới.

## Context Compaction Recovery

Khi context bị compact, PHẢI chạy ngay:

R1: `cat .codex/workflow/workflow-state.md`
R2: Verify 3 artifact gần nhất tồn tại trên filesystem
R3: Output: "Context recovered. Đang ở Bước {N}. Tiếp tục."
R4: Resume từ đúng điểm đã dừng — KHÔNG restart từ Bước 01

## Human Checkpoints bắt buộc

- CP-1: Sau Bước 03 — approve product brief + 4 ADR
- CP-2: Sau Bước 04 — approve architecture + task list
- CP-M: Sau M02 mỗi maintenance cycle — approve impact assessment

## CSF Escalation (Development Loop)

Human CHỈ được gọi khi có Critical Structural Failure (CSF-1 đến CSF-5).
Chi tiết: xem skill `$snmb-dev`.

## Agent Roster

- `analyst` -> `.codex/agents/analyst.toml`
- `architect` -> `.codex/agents/architect.toml`
- `fe-developer` -> `.codex/agents/fe-developer.toml`
- `be-developer` -> `.codex/agents/be-developer.toml`
- `qa-engineer` -> `.codex/agents/qa-engineer.toml`
- `reviewer` -> `.codex/agents/reviewer.toml`

## Bốn ADR bắt buộc

Phải chốt tại **Bước 03** trước khi build. Không bắt đầu Bước 04 khi thiếu bất kỳ ADR nào.

| File | Quyết định |
|---|---|
| `docs/decisions/ADR-001-frontend-framework.md` | Framework FE |
| `docs/decisions/ADR-002-backend-framework.md` | Framework BE |
| `docs/decisions/ADR-003-database.md` | DB engine cụ thể |
| `docs/decisions/ADR-004-deployment-platform.md` | Platform deploy |

## Lệnh nhanh

`$snmb-status`  -> Hiển thị trạng thái hiện tại
`$snmb-next`    -> Hướng dẫn bước tiếp theo
`$snmb-init`    -> Chạy lại bootstrap (nếu cần)
`$snmb-clarify` -> Bắt đầu phỏng vấn yêu cầu (Bước 02)
`$snmb-brief`   -> Tạo product brief + ADR (Bước 03)
`$snmb-plan`    -> Architecture & task breakdown (Bước 04)
`$snmb-setup`   -> Scaffold codebase + QA gate (Bước 05)
`$snmb-dev`     -> Chạy development loop (Bước 06)
`$snmb-review`  -> Code review (Bước 07)
`$snmb-test`    -> Testing (Bước 08)
`$snmb-deploy`  -> Deploy (Bước 09)
`$snmb-verify`  -> Verify production + CHANGELOG (Bước 10)
`$snmb-maintain` -> Bắt đầu maintenance cycle (M01)
