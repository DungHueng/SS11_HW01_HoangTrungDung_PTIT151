# Bài 1: Phân Tích & Lựa Chọn Phương Án Tạo Mã Nguồn

## Đáp án lựa chọn: B

# Lý do lựa chọn:

Phương án B là phương án tối ưu vì đáp ứng đầy đủ cấu trúc 5 thành phần của một Prompt chất lượng, giúp AI sinh mã nguồn chính xác, đúng yêu cầu của dự án.

## 1. Vai trò (Role)

- Chỉ định AI đóng vai **Senior Java Developer**.
- AI sẽ sử dụng tư duy của một lập trình viên giàu kinh nghiệm.
- Mã nguồn được sinh ra thường tuân thủ chuẩn lập trình tốt hơn.

## 2. Nhiệm vụ (Task)

- Yêu cầu rất rõ:
    - Viết class `PaymentValidator`.
    - Kiểm tra tính hợp lệ của thẻ tín dụng.
    - Sử dụng thuật toán **Luhn**.

- Không gây mơ hồ nên AI khó hiểu sai yêu cầu.

## 3. Ngữ cảnh (Context)

- Nêu rõ hệ thống là **E-commerce**.
- Mục đích:
    - Validate thẻ
    - Trước khi gửi API thanh toán.

Nhờ có ngữ cảnh, AI hiểu đúng vị trí của class trong dự án thay vì viết theo hướng chung chung.

## 4. Ràng buộc (Constraints)

Prompt quy định rất đầy đủ:

- Sử dụng **Java 17**
- Triển khai đúng thuật toán **Luhn**
- Nếu:
    - Thẻ rỗng
    - Hoặc chứa ký tự chữ

→ phải ném ra:

```java
IllegalArgumentException
```

Các ràng buộc này giúp AI giảm khả năng sinh code sai hoặc thiếu chức năng.

## 5. Định dạng đầu ra (Output Format)

Prompt yêu cầu:

- Chỉ trả về mã nguồn Java.
- Đặt trong một code block.
- Không giải thích.

Điều này giúp:

- Dễ copy vào IDE.
- Không có phần văn bản dư thừa.
- Phù hợp quy trình phát triển phần mềm.

---

# Ưu điểm của phương án B

- Đầy đủ ngữ cảnh.
- Có vai trò rõ ràng.
- Có yêu cầu kỹ thuật cụ thể.
- Có xử lý ngoại lệ.
- Có định dạng đầu ra.
- Giảm tối đa khả năng AI hiểu sai.
- Phù hợp môi trường dự án thực tế.

---

# Phân tích phương án A

Prompt:

> "Viết cho tôi một class Java tên là PaymentValidator để kiểm tra số thẻ tín dụng bằng thuật toán Luhn. Code ngắn gọn thôi nhé."

## Hạn chế

- Không chỉ định vai trò AI.
- Không có ngữ cảnh dự án.
- Không yêu cầu phiên bản Java.
- Không yêu cầu xử lý ngoại lệ.
- Không quy định định dạng đầu ra.
- "Code ngắn gọn" có thể khiến AI bỏ qua nhiều bước kiểm tra cần thiết.

## Rủi ro Hallucination

AI có thể:

- Không dùng Java 17.
- Không xử lý dữ liệu rỗng.
- Không kiểm tra ký tự chữ.
- Viết thuật toán Luhn chưa đầy đủ.
- Sinh code thiếu tính thực tế.

---

# Phân tích phương án C

Prompt:

> "Tôi cần một đoạn code kiểm tra thẻ tín dụng. Hãy viết bằng Java và sinh thêm cả database SQL để lưu thông tin thẻ. Nhớ hướng dẫn tôi cách cài đặt database và kết nối JDBC luôn nhé."

## Hạn chế

Prompt yêu cầu quá nhiều nhiệm vụ:

- Viết Java.
- Sinh SQL.
- Thiết kế database.
- Hướng dẫn cài đặt.
- Hướng dẫn JDBC.

Trong khi yêu cầu bài toán chỉ cần:

- Viết class `PaymentValidator`.

## Sai lệch ngữ cảnh

AI sẽ chuyển sang nhiều chủ đề khác:

- Database
- SQL
- JDBC
- Cài đặt môi trường

#### => Những nội dung này không phục vụ trực tiếp việc kiểm tra thẻ tín dụng.
