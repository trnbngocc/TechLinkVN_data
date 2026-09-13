# TechLink

Dự án phát triển web

## Mô tả

Script này thực hiện:
1. Cào (crawl) 50 hồ sơ bài báo khoa học từ [OpenAlex API](https://openalex.org/), lọc lấy các bài có đầy đủ thông tin: tiêu đề, DOI, tác giả kèm mã ORCID, năm xuất bản, tạp chí, lĩnh vực, từ khóa, tóm tắt (abstract), và link PDF.
2. Xuất dữ liệu ra file Excel (`research_profiles.xlsx`) với định dạng đã căn chỉnh (in đậm tiêu đề, tự động dãn cột, ngắt dòng).
3. Nạp dữ liệu vào database SQLite (`techlinkvn.db`), bảng `papers`.
4. Truy vấn dữ liệu bằng SQL để kiểm tra và hiển thị kết quả.

## Yêu cầu

- Python 3.10 trở lên
- Các thư viện trong `requirements.txt`

## Cài đặt

```bash
pip install -r requirements.txt
```

## Cách chạy

Mở file `task1.ipynb` bằng Jupyter Notebook (hoặc VS Code có cài extension Jupyter), chạy lần lượt từng cell theo thứ tự.

Hoặc chạy trực tiếp bằng file `.py`:

```bash
python task1.py
```

## Cấu trúc file

- `task1.py` — code chính (bản script thuần)
- `task1.ipynb` — code chính (bản notebook, có hiển thị kết quả trực quan)
- `requirements.txt` — danh sách thư viện cần cài

## Ghi chú

File `research_profiles.xlsx` và `techlinkvn.db` được tự động tạo ra khi chạy code, không được lưu trong repository này (xem `.gitignore`).