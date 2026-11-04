# Review OpenAPI Specification - TODO(TH2-1)

## Kết quả kiểm tra các API endpoints:

1. **GET /api/v1/books**
   - Mã thành công: 200
   - Mã lỗi khai báo: 400
   - An toàn (Safe): Có
   - Idempotent: Có

2. **POST /api/v1/books**
   - Mã thành công: 201 + Header `Location` + Header `ETag`
   - Mã lỗi khai báo: 400, 409
   - An toàn (Safe): Không
   - Idempotent: Không

3. **GET /api/v1/books/{isbn}**
   - Mã thành công: 200 + Header `ETag` / 304 (Not Modified)
   - Mã lỗi khai báo: 404
   - An toàn (Safe): Có
   - Idempotent: Có

4. **PUT /api/v1/books/{isbn}**
   - Mã thành công: 200 + Header `ETag` mới
   - Mã lỗi khai báo: 400, 404, 412, 428
   - An toàn (Safe): Không
   - Idempotent: Có

5. **DELETE /api/v1/books/{isbn}**
   - Mã thành công: 204
   - Mã lỗi khai báo: 404
   - An toàn (Safe): Không
   - Idempotent: Có

---
