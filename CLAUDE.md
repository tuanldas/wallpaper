# Project Instructions

## Agent Teams Configuration

Dự án này sử dụng **Agent Teams** để khám phá app Android song song trên 3 emulators.

### Env vars (đã cấu hình trong ~/.claude/settings.json)
- `CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1` — bật tính năng Agent Teams
- `CLAUDE_CODE_SUBAGENT_MODEL=claude-opus-4-6` — tất cả sub-agents dùng model Opus

### Phân công teammates

| Teammate | Emulator | Khu vực |
|----------|----------|---------|
| Teammate 1 | emulator-5554 | Home & Wallpaper features |
| Teammate 2 | emulator-5558 | Collage & Editing features |
| Teammate 3 | emulator-5560 | Settings, Export & Monetization |

### Quy tắc phối hợp
- Mỗi teammate tự navigate từ home đến khu vực được giao
- Sử dụng shared task list (`TaskCreate`/`TaskUpdate`) để theo dõi tiến độ
- Nếu phát hiện tính năng thuộc khu vực teammate khác → tạo task nhưng không deep dive
- Output ghi vào thư mục `features/` theo cấu trúc trong `EXPLORATION_RULES.md`
