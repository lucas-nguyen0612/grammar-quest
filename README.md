# Grammar Quest

Chinh phục ngữ pháp: khóa tự học ngữ pháp tiếng Anh cho người mất gốc. Mỗi chương là một trang HTML tự chứa: bài học 25 phút với sơ đồ (mind map, sơ đồ quyết định, bảng), bài tập tự chấm, bài nghiệm thu cho từng chủ đề, bài trộn và flashcard ôn cách quãng (xuất được sang Anki).

Nội dung bám theo sách *Giải thích ngữ pháp tiếng Anh* (Mai Lan Hương & Hà Thanh Uyên). Quy tắc được tóm tắt, diễn giải lại và ghi số trang; phần lớn ví dụ và bài tập là tự soạn.

## Cấu trúc

```
index.html              trang thư viện, liệt kê các chương
site.json               tên và mô tả trang thư viện
chuong-1-tu-loai/       Chương 1 · Từ loại
  index.html            khóa học
  flashcards.txt        file nhập vào Anki
  course-meta.json      thông tin chương cho trang thư viện
```

## Thêm một chương

Trang được tạo bằng skill `english-grammar-course` (Claude Code):

```bash
python3 build_course.py <thư-mục-dữ-liệu-chương> --out ./chuong-2-<ten>
python3 build_library.py .
```

Tiến độ học được lưu trong trình duyệt (localStorage), dùng chung cho mọi chương trên cùng một tên miền.

## Deploy

Trang tĩnh, không cần build. Trên Vercel: Import repo → Framework preset **Other** → để trống Build Command và Output Directory → Deploy.
