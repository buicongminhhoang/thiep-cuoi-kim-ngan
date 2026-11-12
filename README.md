# Thiệp cưới Kim Ngân & Minh Hoàng

Trang tĩnh hoàn toàn (không máy chủ, không cơ sở dữ liệu). Mở `index.html` bằng Chrome là xem được ngay.

```
web/
├─ index.html                 thiệp: màn phong bì + thiệp dạng cuộn (HTML + CSS + JS trong một file)
├─ index-phong-bi-cu.html     bản cũ (phong bì đóng, bố cục cũ) để đối chiếu, có thể xoá
├─ js/                        thư viện cuộn mượt (GSAP, Lenis); thiếu vẫn xem được
├─ img/                       30 ảnh (NTDxxxxx.jpg ~1800px, th_NTDxxxxx.jpg thumbnail)
├─ img/flowers/               hoa calla lily đã tách nền (calla-pink.png, calla-white.png)
└─ audio/ngay-dau-tien.mp3    nhạc nền
```

## Tông màu

Mặc định là hồng phấn. Thêm `?theme=dark` vào link để xem bản nền đen như mẫu gốc.
Muốn nền đen làm mặc định: sửa `data-theme="pink"` thành `data-theme="dark"` ở dòng 2 của `index.html`.

## Hoa

Đang dùng `img/flowers/calla-pink.png` (tách nền từ ảnh bạn đưa, khá nhỏ: 433 px).
Có ảnh nét hơn thì lưu đè lên đúng tên file đó (PNG nền trong suốt, cuống hoa ở phía dưới).
`calla-white.png` đã có sẵn nhưng chưa dùng; đổi tên file trong `index.html` nếu muốn dùng hoa trắng.

## Đưa lên mạng để gửi khách

Upload cả thư mục `web/` lên Netlify Drop (netlify.com/drop), Vercel hoặc GitHub Pages.
Trang cần chạy qua `https://` để nút sao chép địa chỉ hoạt động.

## Ghi tên khách lên phong bì

Thêm `?guest=Tên` vào link, ví dụ `https://ten-mien-cua-ban/?guest=Anh%20Tuấn`.
Tên sẽ hiện trên màn phong bì và trong phần lời mời.

## Những gì có thể chỉnh trong `CONFIG` (đầu phần `<script>`)

- `eventISO`: giờ làm lễ dùng cho đếm ngược và file lịch.
- `address`, `mapsUrl`, `mapsEmbed`: địa chỉ, link chỉ đường và bản đồ nhúng.
- `album`: thứ tự ảnh trong album cuối trang.

Ảnh ở các phần khác đổi trực tiếp trong HTML (tìm `img/NTD`).
