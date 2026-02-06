# ToroCrop 🌾

**ToroCrop** tự trồng lại hạt giống , yêu cầu của chế ngân

## 🎮 Hướng dẫn sử dụng

### 1. Nhận công cụ chọn vùng
Sử dụng lệnh sau để nhận công cụ (mặc định là **Rìu Kim Cương**):
```bash
/torocrop wand
```

### 2. Tạo vùng trồng trọt
1. **Click chuột trái** vào góc đầu tiên của vùng.
2. **Click chuột phải** vào góc đối diện (tạo thành hình hộp chữ nhật bao quanh khu ruộng).
3. Gõ lệnh để tạo vùng:
```bash
/torocrop create <tên_vùng>
```
*Ví dụ: `/torocrop create luanep`*

### 3. Xong!
Bây giờ bất kỳ cây trồng nào trong vùng `luanep` khi chín sẽ tự động được trồng lại khi thu hoạch.

## 📜 Danh sách lệnh (Commands)

| Lệnh | Mô tả | Quyền (Permission) |
|---|---|---|
| `/torocrop wand` | Nhận công cụ chọn vùng | `torocrop.admin` |
| `/torocrop create <tên>` | Tạo vùng mới từ 2 điểm đã chọn | `torocrop.admin` |
| `/torocrop delete <tên>` | Xóa một vùng | `torocrop.admin` |
| `/torocrop list` | Xem danh sách các vùng đang có | `torocrop.admin` |
| `/torocrop info <tên>` | Xem thông tin chi tiết của vùng | `torocrop.admin` |
| `/torocrop reload` | Tải lại cấu hình config.yml | `torocrop.admin` |

## 🛡️ Permissions

- `torocrop.admin`: Quyền sử dụng tất cả các lệnh Admin.
- `torocrop.bypass.break-unripe`: Cho phép đập cây chưa chín (khi đang bật chế độ bảo vệ).

## ⚙️ Cấu hình (config.yml)

```yaml
# Công cụ dùng để chọn vùng (Mặc định: DIAMOND_AXE)
selection-tool: DIAMOND_AXE

# Các loại cây hỗ trợ
supported-crops:
  - WHEAT
  - CARROTS
  - POTATOES
  - BEETROOTS
  - NETHER_WART

# Thời gian trễ trước khi trồng lại (ticks)
replant-delay-ticks: 2

# Có rớt hạt giống dư thừa không?
drop-extra-seeds: true

# Chống dẫm nát ruộng trong vùng (True = Bật)
prevent-trampling: true

# Chặn đập cây chưa chín (True = Bật)
prevent-breaking-unripe-crops: true
```
