# Trigger

Nguồn: http://www.postgresqltutorial.com/creating-first-trigger-postgresql/

**Tóm lược**: Trong hướng dẫn này, chúng tối sẽ giới thiệu cho bạn từng bước một làm thế nào để 
tạo ra trigger đầu tiên trong PostgreSQL sử dụng câu lệnh `CREATE TRIGGER`.

Để tạo một trigger mới trong PostgreSQL, bạn cần:

- Tạo một hàm trigger sử dụng câu lệnh `CREATE [OR REPLACE] FUNCTION`.

- Liên kết hàm trigger này đến bảng, sử dụng câu lệnh `CREATE TRIGGER`.

Nếu bạn không quen với tạo hàm do người dùng tự định nghĩa, bạn có thể xem tại [PostgreSQL stored procedure section.](http://www.postgresqltutorial.com/postgresql-stored-procedures/)

### Tạo một hàm trigger

Một hàm trigger giống như một hàm bình thường, ngoại trừ nó không có bất kỳ đối số nào và có trả 
về giá trị kiểu `trigger` như sau: 

```sql
CREATE FUNCTION trigger_function() RETURN trigger AS
```

lưu ý bạn có thể tạo