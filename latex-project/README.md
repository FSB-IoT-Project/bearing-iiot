# LaTeX Project Setup

## Yêu cầu

1. **TeX Distribution** - Bạn cần cài đặt một trong các bản phân phối LaTeX sau:
   - **Windows**: [MiKTeX](https://miktex.org/download) hoặc [TeX Live](https://www.tug.org/texlive/)
   - **macOS**: [MacTeX](https://www.tug.org/mactex/)
   - **Linux**: TeX Live (thường có sẵn trong package manager)

2. **VS Code Extension**: [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)

## Cài đặt

### Bước 1: Cài đặt TeX Distribution

#### Windows - MiKTeX (Khuyến nghị cho người mới bắt đầu)
1. Download MiKTeX từ: https://miktex.org/download
2. Chạy installer và chọn "Install missing packages on-the-fly: Yes"
3. Sau khi cài đặt, mở MiKTeX Console và update tất cả packages

#### Windows - TeX Live (Đầy đủ hơn)
1. Download TeX Live từ: https://www.tug.org/texlive/
2. Chạy installer (có thể mất 30-60 phút)
3. Thêm TeX Live vào PATH nếu chưa có

### Bước 2: Cài đặt LaTeX Workshop Extension

1. Mở VS Code
2. Nhấn `Ctrl+Shift+X` để mở Extensions
3. Tìm "LaTeX Workshop" của James Yu
4. Click Install

### Bước 3: Kiểm tra cài đặt

Mở terminal và chạy:
```bash
pdflatex --version
```

Nếu hiển thị version của pdflatex, bạn đã cài đặt thành công!

## Cách sử dụng

1. **Mở file LaTeX**: Mở file `main.tex` trong VS Code
2. **Compile tự động**: File sẽ tự động compile khi bạn save (Ctrl+S)
3. **Xem PDF**: Click vào icon "View LaTeX PDF" ở góc trên bên phải hoặc nhấn `Ctrl+Alt+V`
4. **Build thủ công**: Nhấn `Ctrl+Alt+B` để build
5. **Clean auxiliary files**: Nhấn `Ctrl+Alt+C`

## Cấu trúc Project

```
latex-project/
├── .vscode/
│   └── settings.json    # Cấu hình LaTeX Workshop
├── output/              # Folder chứa PDF và file tạm (tự động tạo)
├── main.tex            # File LaTeX chính
└── README.md           # File hướng dẫn này
```

## Build Recipes

Project này đã được cấu hình với các recipes sau:

1. **pdfLaTeX**: Build cơ bản với pdflatex (1 lần)
2. **pdfLaTeX x2**: Build 2 lần (cho references và table of contents)
3. **pdfLaTeX + BibTeX**: Build với bibliography
4. **XeLaTeX**: Build với XeLaTeX (hỗ trợ Unicode tốt hơn)

## Tính năng đã cấu hình

- ✅ Auto-build khi save file
- ✅ PDF viewer tích hợp trong VS Code
- ✅ Output files được lưu trong folder `output/`
- ✅ Tự động clean auxiliary files sau khi build
- ✅ Hỗ trợ tiếng Việt
- ✅ SyncTeX (click vào PDF để jump đến code)

## Troubleshooting

### Lỗi "pdflatex not found"
- Đảm bảo bạn đã cài đặt MiKTeX hoặc TeX Live
- Restart VS Code sau khi cài đặt
- Kiểm tra PATH environment variable

### Lỗi "Missing packages"
- Nếu dùng MiKTeX: Mở MiKTeX Console → Updates → Update now
- Nếu dùng TeX Live: Chạy `tlmgr update --all`

### PDF không hiển thị tiếng Việt
- Đảm bảo file `main.tex` có dòng: `\usepackage[vietnamese]{babel}`
- Hoặc sử dụng XeLaTeX recipe thay vì pdfLaTeX

## Tài liệu tham khảo

- [LaTeX Workshop Documentation](https://github.com/James-Yu/LaTeX-Workshop/wiki)
- [Overleaf Learn LaTeX](https://www.overleaf.com/learn)
- [LaTeX Wikibook](https://en.wikibooks.org/wiki/LaTeX)

## Tips

- Sử dụng `Ctrl+Space` để auto-complete commands
- Sử dụng `Ctrl+Click` trên `\ref{}` để jump đến label
- Sử dụng snippet: gõ `beg` rồi `Tab` để tạo environment
