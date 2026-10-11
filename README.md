# Từ điển cho trò chơi Đổi Chữ

Hai file JSON dùng để phán quyết từ đúng/sai trong trò chơi.

| File | Số từ hợp lệ | Nội dung |
|---|---|---|
| `dict_vi.json` | 6.113 (+1.076 từ mở rộng) | Từ đơn tiếng Việt một âm tiết |
| `dict_en.json` | 168.551 | Từ tiếng Anh dài 2–15 chữ cái |

## Cấu trúc

- `words`: toàn bộ từ hợp lệ, đã chuẩn hoá.
- `extra`: (chỉ tiếng Việt) các tiếng chỉ xuất hiện trong từ ghép, ví dụ "nhiên", "khuyến". Chỉ được chấp nhận khi phòng bật "Từ điển mở rộng".
- `common`: từ thông dụng, dùng cho máy ở chế độ chơi một mình.
- `start`: từ khởi đầu theo độ dài, đã lọc để có đủ nước đi tiếp theo.
- `startLengths`: các độ dài từ khởi đầu có thể chọn.

## Chuẩn hoá

- Tiếng Việt: Unicode NFC, chữ thường, dấu thanh kiểu mới (`hoà`, `thuý`, `uỷ`). Ứng dụng phải chuẩn hoá chữ người chơi gõ theo cùng cách trước khi tra.
- Tiếng Anh: chữ thường a–z.

## Nguồn và giấy phép

- Tiếng Việt: tổng hợp từ [uiovn/Vietnamese-Dictionary](https://github.com/uiovn/Vietnamese-Dictionary) (nhóm underthesea; gồm danh sách của Hồ Ngọc Đức, tudientv và Wiktionary). Giấy phép GPL-3.0; `dict_vi.json` là sản phẩm phái sinh và được phát hành theo cùng giấy phép.
- Tiếng Anh: danh sách ENABLE (`enable1.txt`, phạm vi công cộng) và `popular.txt` từ [dolph/dictionary](https://github.com/dolph/dictionary).
