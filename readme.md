# ToroCrop Plugin Development

## Nhiệm vụ
Tạo plugin ToroCrop cho Minecraft 1.20-1.21.1 với hỗ trợ Folia - hệ thống vùng trồng cây tự động.

---

## Checklist

### Planning
- [x] Nghiên cứu cấu trúc dự án hiện tại
- [x] Phân tích plugin Autoreplant-master để tham khảo
- [x] Viết implementation plan
- [x] Chờ user phê duyệt kế hoạch

### Implementation
- [x] Tạo cấu trúc thư mục và file cơ bản
  - [x] pom.xml với dependencies (Paper, BStats)
  - [x] plugin.yml
  - [x] config.yml
  - [x] messages.yml
- [x] Tạo main class với logo khởi động
- [x] Hệ thống vùng (Region System)
  - [x] CropRegion class
  - [x] RegionManager class  
  - [x] Selection tool (rìu) với 2 vị trí
  - [x] Lưu/tải vùng từ file YAML
- [x] Commands
  - [x] /torocrop create <tên> - tạo vùng mới
  - [x] /torocrop delete <tên> - xóa vùng
  - [x] /torocrop list - liệt kê vùng
  - [x] /torocrop reload - reload config
  - [x] /torocrop wand - nhận rìu chọn vùng
  - [x] /torocrop info <tên> - thông tin vùng
- [x] CropListener - xử lý sự kiện đập cây trồng
- [x] TrampleListener - ngăn chặn dẫm nát ruộng lúa
- [x] Prevent breaking unripe crops - chặn đập cây chưa chín
- [x] Folia scheduler support

### Verification
- [x] Build plugin không lỗi
- [ ] Test trên server (manual)
