# Bao Cao Hardening

Ngay audit: 2026-04-20

## Muc Tieu

Lam bundle nay an toan hon de public, de AI khac co the dung ngay, va de giam toi da cac diem co the gay mo ho ve quyen so huu, ket noi ben ngoai, hoac side-effect tren may.

## Da Xu Ly

- Go 4 skill co license han che khoi bundle public:
  - `.agent/skills/docx`
  - `.agent/skills/pdf`
  - `.agent/skills/pptx`
  - `.agent/skills/xlsx`
- Lam sach `.agent/mcp_config.json` thanh cau hinh rong, khong bat san dich vu MCP ben ngoai.
- Chuan hoa `.claude-plugin/marketplace.json`:
  - bo thong tin chu so huu ca nhan
  - bo path cu `./skills/...` da sai voi cau truc merged
  - doi metadata sang ten bundle hien tai
- Harden `.agent/scripts/auto_preview.py`:
  - bo `shell=True`
  - resolve lenh npm/yarn/pnpm/bun tren Windows theo cach ro rang hon
- Mo rong `.gitignore` de bo qua file runtime va log tao ra trong luc preview.
- Cap nhat lai routing, quality bar, va huong dan su dung theo huong local-first.

## Ket Qua Audit

- Khong tim thay hidden file la ngoai `.git`.
- Khong tim thay junction hay reparse point con sot lai.
- Khong tim thay executable binary dang ngo trong repo.
- Cac skill con lai khong tu dong ket noi ra ngoai; nhung skill dung provider ben ngoai van la opt-in va can duoc goi ro rang.
- Da chay custom scan bang Windows Defender tren `D:\\skill\\skill\\agent-skills-unified` va khong co threat nao duoc bao cao.

## Tinh Trang Sau Hardening

- Thu vien skill con lai: 48 skill.
- Cau hinh mac dinh: local-first, khong co MCP server ben ngoai duoc bat san.
- Metadata/plugin market da duoc lam sach de phu hop voi bundle merged hien tai.

## Ghi Chu Van Hanh

- Neu muon dung MCP server ben ngoai, hay tu them cau hinh sau khi review thu cong.
- Neu muon them lai skill xu ly file van phong, chi nen them tu nguon ma ban chac chan co quyen su dung va phan phoi.
- Script trong repo van co the doc file du an hoac chay subprocess khi ban chu dong goi no, nhung bundle hien tai khong ship cau hinh nao tu dong lay du lieu may.
