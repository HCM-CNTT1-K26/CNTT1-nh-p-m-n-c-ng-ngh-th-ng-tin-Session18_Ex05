# CNTT1-nh-p-m-n-c-ng-ngh-th-ng-tin-Session18_Ex05
### Phần 1. Phân tích: Vai trò của JSON Viewer khi gỡ lỗi API

Lúc hệ thống điều phối gọi dữ liệu GPS, máy chủ thường trả về một mớ chuỗi JSON thô (raw text) nhìn rất nhức mắt và cực kỳ khó dò lỗi bằng mắt thường. Lúc này, extension **JSON Viewer** đóng vai trò cứu cánh: nó tự động parse, phân cấp dữ liệu thành dạng cây (tree view) có thụt lề và tô màu cú pháp rõ ràng. Nhờ vậy, kỹ sư nhìn vào là tra cứu ngay được tọa độ vĩ độ/kinh độ, trạng thái xe hoặc phát hiện lỗi dữ liệu bất thường từ server trong một nốt nhạc.

---

### Phần 2. Triển khai: 5 Tiện ích cốt lõi, Ghim Toolbar và Site Access

1. **Chọn lọc 5 Extensions thiết yếu (tối ưu hóa RAM):**
* *Nhóm Dev:* **JSON Viewer** (đọc hiểu cấu trúc API) và **Talend API Tester** (kiểm tra nhanh các HTTP request).
* *Nhóm Productivity:* **ColorZilla** (hút mã màu giao diện bản đồ) và **Dimensions** (đo khoảng cách pixel chuẩn layout).
* *Nhóm Security:* **uBlock Origin** (chặn quảng cáo thần thánh, dung lượng cực nhẹ, không làm nặng máy).


2. **Ghim nhanh ra thanh công cụ & Cấu hình Site Access:**
* Nhấp vào biểu tượng hình mảnh ghép (Extensions) ở góc trên bên phải trình duyệt, bấm nút **Ghim (Pin)** để đưa các tiện ích trên ra ngoài thao tác cho lẹ.
* Để bảo mật dữ liệu GPS, vào phần quyền của extension đổi thiết lập thành **On click** (Chỉ chạy khi nhấp vào). Việc này giúp tiện ích không tự ý đọc thông tin nhạy cảm hay ngốn ngầm RAM trong lúc trình duyệt đang gồng mình load biểu đồ Waterfall.



---

### Phần 3. Kiểm thử hiệu năng (Xử lý khi trình duyệt bị lag)

Đang soi biểu đồ Waterfall mà thấy máy có hiện tượng giật cục, khả năng cao là có extension đang chạy ngầm hút tài nguyên. Quy trình kiểm tra trực tiếp:

1. Nhấn nhanh tổ hợp phím **Shift + Esc** để mở bảng Task Manager riêng của trình duyệt.
2. Kiểm tra cột **Memory footprint** xem tiện ích mở rộng nào đang tốn nhiều RAM bất thường.
3. Hoặc gõ  chrome://extensions  vào thanh địa chỉ, tìm đúng con gây nghẽn cổ chai rồi bấm gạt tắt tạm thời (hoặc bấm End Process trong Task Manager) để trả lại sự mượt mà cho trình duyệt.
