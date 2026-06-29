# Hướng dẫn triển khai Qantera Docs lên GitBook

## Trạng thái gói tài liệu

Các thông tin network đã được cấu hình:

- Public Testnet
- Chain ID `974621`
- QTER, 18 decimals
- RPC1, RPC2 và WSS
- Explorer
- Faucet amount `0.1 QTER`

Những thông tin chưa được công bố được ghi rõ là **Coming soon** hoặc **Not yet published**, không dùng thông số giả.

## Đưa lên GitHub

1. Tạo repository, ví dụ `qantera-docs`.
2. Upload toàn bộ nội dung bên trong thư mục `qantera-gitbook` lên root repository.
3. Đảm bảo `.gitbook.yaml`, `README.md` và `SUMMARY.md` nằm ở root.
4. Commit lên branch `main`.

## Kết nối GitBook

1. Tạo Space mới trong GitBook.
2. Chọn **GitHub Sync**.
3. Chọn repository `qantera-docs` và branch `main`.
4. Chọn chiều đồng bộ ban đầu **GitHub → GitBook**.
5. Để Project directory là `/` nếu file nằm ở root.
6. Chạy initial sync.

## Cập nhật sau này

Khi có thông tin mới, cập nhật trước các trang:

- `getting-started/network-details.md`
- `setup/faucet.md`
- `concepts/why-post-quantum.md`
- `security/post-quantum.md`
- `nodes/run-a-node.md`
- `validators/overview.md`
- `CONFIGURATION_CHECKLIST.md`

Sau đó commit lên GitHub để GitBook tự đồng bộ.
