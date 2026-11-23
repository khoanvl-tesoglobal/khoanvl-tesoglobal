# Nhật Ký Thay Đổi (Changelog)

Toàn bộ các cập nhật và thay đổi mã nguồn của dự án sẽ được ghi nhận tại đây.

Định dạng dựa trên [Keep a Changelog](https://keepachangelog.com/vi/1.0.0/).

---
## [2026-11-23] - Đồng Bộ Profile GitHub Theo Tên Người Dùng Mới
### Đã thay đổi (Changed)
- **Cập nhật định danh tài khoản trong `README.md`**: Chuyển toàn bộ liên kết cá nhân, badge thống kê (GitHub Stats, Top Languages, Streak Stats), nhãn Arcade Player sang tài khoản mới `@khoanvl-tesoglobal`.
- **Đồng bộ đường dẫn hoạt ảnh đóng góp (Contribution Snake Animation)**: Cập nhật URL nguồn ảnh SVG của con rắn sang repository `khoanvl-tesoglobal/khoanvl-tesoglobal/output/`.
- **Cập nhật URL Remote Git**: Đồng bộ địa chỉ Git origin sang repository `https://github.com/khoanvl-tesoglobal/khoanvl-tesoglobal.git`.


## [2026-09-19] - Tinh Chỉnh Giao Diện Mô Phỏng AI Simulation Window
### Đã thay đổi (Changed)
- **Xóa nút STOP ENGINE**: Loại bỏ nút dừng màu đỏ ở góc trên thanh tiêu đề của cửa sổ mô phỏng, giúp giao diện thoáng đãng và tập trung vào luồng code.
- **Rút ngắn chuỗi Prompt comment**: Tinh chỉnh nội dung chú thích thành `# Prompt: "Tối ưu hóa chu kỳ đèn theo thời gian thực"`, giải quyết dứt điểm việc dòng chữ dài bị tràn lề và đè lên panel Python Runtime bên phải.
- **Thêm Cache Buster URL vào README.md**: Gắn thêm tham số `?v=2` vào đường dẫn ảnh `ai-simulation-window.svg` để ép máy chủ proxy GitHub Camo hủy bản cache cũ và tải lại ảnh mới ngay lập tức.

## [2026-09-10] - Cập Nhật URL Snake Mới Để Xóa Triệt Để Cache Camo GitHub
### Đã thay đổi (Changed)
- **Đổi tên file đầu ra thành `snake-dark.svg` và `snake-light.svg`**: Tránh tình trạng máy chủ GitHub Camo lưu cache cũ của URL trước đó ở chế độ Dark Mode, giúp người dùng thấy ngay giao diện con rắn gradient xanh dương và các ô táo xanh lá mới tinh ngay lập tức.

### Đã thay đổi (Changed)
- **Đổi màu "trái táo" sang xanh lá contributions**: Cập nhật `color_dots` sang hệ màu xanh lá cây đặc trưng của GitHub (`#161b22,#0e4429,#006d32,#26a641,#39d353` cho Dark mode và `#ebedf0,#9be9a8,#40c463,#30a14e,#216e39` cho Light mode) giúp hiển thị chuẩn như graph contribution thực tế.
- **Tạo hiệu ứng gradient xanh dương nhạt dần cho con rắn**: Bổ sung bước xử lý tự động `Enhance Snake Color Gradient` trong GitHub Actions workflow `.github/workflows/snake.yml`, gán dải màu xanh dương chuyển sắc mượt mà từ đầu (`#0284c7` - xanh dương đậm rõ nét) nhạt dần qua thân (`#38bdf8`, `#7dd3fc`) đến đuôi (`#bae6fd`), giúp con rắn nổi bật hoàn toàn và không bị trùng màu với các ô xanh lá.
