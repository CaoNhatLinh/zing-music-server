# 🎵 Trang Chủ API Âm Nhạc Việt Nam 🇻🇳 (MP3 clone)

Đây là hướng dẫn sử dụng cho API cung cấp dữ liệu âm nhạc.

-----

## 🛠️ Cài Đặt và Khởi Chạy

Bạn có thể cài đặt các gói cần thiết và khởi chạy ứng dụng bằng cách sử dụng `yarn` hoặc `npm`.

### 📦 Cài Đặt Gói

Mở terminal và chạy một trong các lệnh sau:

```bash
$ yarn install # Hoặc dùng: npm install
```

### ▶️ Khởi Chạy Ứng Dụng

Sau khi cài đặt, chạy ứng dụng:

```bash
$ yarn start # Hoặc dùng: npm run start
```

> [!NOTE] 
> API này **chỉ được phép sử dụng** với **server Việt Nam**.

-----

## 🚀 Sử Dụng API

Sau khi khởi chạy ứng dụng, API sẽ có sẵn tại **http://localhost:3000**. Dưới đây là danh sách các endpoint và cách sử dụng:

### 🌐 Mở Trình Duyệt

Truy cập địa chỉ sau để kiểm tra ứng dụng:

**[http://localhost:3000](http://localhost:3000)**

-----

### 📝 Danh Sách Endpoint

| Mô Tả | Endpoint | Tham Số (Params) | Ví dụ tham số |
| :--- | :--- | :--- | :--- |
| **Lấy Bài Hát** | `/api/song` | `id` (ID bài hát) | `id=ZWZDZ0C9` |
| **Lấy Thông Tin Bài Hát** | `/api/infosong` | `id` (ID bài hát) | `id=ZWZDZ0C9` |
| **Lấy Lời Bài Hát** | `/api/lyric` | `id` (ID bài hát) | `id=ZWZDZ0C9` |
| **Tìm Kiếm** | `/api/search` | `keyword` (Từ khóa tìm kiếm) | `keyword=hoa+nở+không+màu` |
| **Trang Chủ** | `/api/home` | `page` (Số trang) | `page=1` |
| **Chi Tiết Playlist** | `/api/detailplaylist` | `id` (ID playlist) | `id=ZO68AC72` |
| **Top 100** | `/api/top100` | (Không có) | |
| **Bảng Xếp Hạng (Home)** | `/api/charthome` | (Không có) | |
| **Bảng Xếp Hạng Mới Phát Hành** | `/api/newreleasechart` | (Không có) | |
| **Thông Tin Nghệ Sĩ** | `/api/artist` | `name` (Tên nghệ sĩ) | `name=sơn+tùng+m-tp` |
| **Bài Hát của Nghệ Sĩ** | `/api/artistsong` | `id`, `page`, `count` | `id=IWZ9Z08I`, `page=1`, `count=10` |
| **Danh Sách MV** | `/api/listmv` | `id`, `page`, `count` | `id=IWZ9Z08O`, `page=1`, `count=10` |
| **Danh Mục MV** | `/api/categorymv` | `id` (ID video) | `id=ZO6O68IW` |
| **Thông Tin Video/MV** | `/api/video` | `id` (ID video) | `id=ZO6O68IW` |

### 💡 Cấu Trúc Yêu Cầu

Tất cả các yêu cầu được gửi đến **http://localhost:3000** theo cấu trúc sau:

```
http://localhost:3000{endpoint}?{tham-số-và-giá-trị}
```

**Ví dụ:**

Để **Lấy Bài Hát** với ID `ZWZDZ0C9`:

`http://localhost:3000/api/song?id=ZWZDZ0C9`
