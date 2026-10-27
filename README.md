# astec-marketplace

Marketplace nội bộ của ASTEC cho Claude Code, dành cho các team Dev và Research.
Repo này chứa danh mục plugin (`.claude-plugin/marketplace.json`) và mã nguồn
của từng plugin trong thư mục `plugins/`.

## Cấu trúc

```
demo_marketplace/
├── .claude-plugin/
│   └── marketplace.json     # Danh sách plugin
├── plugins/
│   └── hello-world/         # Plugin mẫu: 1 skill, 1 agent, 1 hook
└── README.md
```

## Plugin hiện có

| Plugin | Mô tả |
|--------|-------|
| `hello-world` | Plugin mẫu để thử quy trình cài đặt và chạy plugin |

## Cài đặt

Thêm marketplace từ repo GitHub `lointfujinet/demo_marketplace`:

```
/plugin marketplace add lointfujinet/demo_marketplace
```

Sau đó cài plugin:

```
/plugin install hello-world@astec-marketplace
```

Lưu ý hai tên khác nhau: `demo_marketplace` là tên **repo** (dùng khi thêm marketplace),
còn `astec-marketplace` là tên **marketplace** khai báo trong `marketplace.json`
(dùng sau dấu `@` khi cài plugin).

Nếu repo là private, tài khoản git trên máy của bạn phải có quyền truy cập repo.

## Cập nhật

Khi plugin có phiên bản mới, chạy `/plugin marketplace update` để lấy bản mới.

## Thêm plugin mới

1. Tạo thư mục `plugins/<tên-plugin>/` với `.claude-plugin/plugin.json`.
2. Thêm một mục vào `plugins` trong `.claude-plugin/marketplace.json`.
3. Chạy `claude plugin validate .` ở thư mục gốc, rồi tăng `version` và push.
