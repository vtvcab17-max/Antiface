<p align="center">
  <img src="https://raw.githubusercontent.com/vtvcab17-max/Bravinall/main/site/assets/brand/antifact.svg" alt="Antifact" width="72" height="72">
</p>

<h1 align="center">Antifact</h1>

<p align="center"><b>Chỉnh ảnh, thiết kế và làm slide camera ngay trên trình duyệt.</b><br>
Không cần cài, không cần tài khoản. Xong thì gửi sang Bravin, mỗi layer một track.</p>

<p align="center">
  <a href="https://antiface.vtvcab17.workers.dev/"><b>🎨 Mở Antifact</b></a> ·
  <a href="https://bravinall.vtvcab17.workers.dev/antifact.html">Trang giới thiệu</a>
</p>

---

## Làm được gì

- **Layer**: mỗi thứ một layer, chồng lên nhau thành tác phẩm.
- **Công cụ chọn, vẽ, sửa ảnh**: năm loại cọ; làm sáng, làm tối, làm mờ từng vùng.
- **Xoá vật thể**: khoanh vùng, bấm, vật thừa biến mất.
- **Layer điều chỉnh**: chỉnh màu mà không phá ảnh gốc.
- **Chữ tiếng Việt** chuẩn từng dấu, màu chính xác tới từng mã.
- **Trợ lý AI** tự chọn: Claude, OpenAI hoặc Ollama. Gõ yêu cầu thay vì thao tác.
- **Khung có sẵn** cho mọi nơi bạn đăng.
- **Slide camera** 2D / 2.5D / 3D: mỗi layer là một tấm phẳng, camera bay trong không gian.
- **Xuất** PNG, JPG, WebP, hoặc **gửi sang Bravin**.

Dữ liệu nằm trên máy bạn. Cài được như app (PWA) và chạy khi không có mạng.

## Trong repo này có gì

| Tệp | Nội dung |
|---|---|
| `index.html` | Antifact 1.1 gói gọn trong một tệp HTML |
| `antifact-app.zip` | Mã nguồn đầy đủ (giải nén để sửa) |

Bên trong `antifact-app.zip`:

```
public/
  index.html                 giao diện
  css/style.css              kiểu dáng
  js/app.js                  toàn bộ logic: editor, slide, camera, timeline, xuất video / GIF
  sw.js, js/register-sw.js   chạy offline
  manifest.webmanifest       cài như app (PWA)
  _headers                   header cache / bảo mật cho Cloudflare
wrangler.toml                cấu hình Cloudflare Workers
scripts/serve.mjs            chạy thử trên máy
scripts/build-single.mjs     gộp thành một tệp index.html
```

## Chạy thử trên máy

```bash
unzip antifact-app.zip && cd antifact-app
node scripts/serve.mjs        # mở http://localhost:8787
```

> [!NOTE]
> Đừng mở bằng `file://`: service worker và PWA cần http(s).

Đưa lên Cloudflare: chạy `npx wrangler deploy` trong thư mục `antifact-app`.

## Hệ sinh thái Bravinall

| Ứng dụng | Dùng để | Mở ngay |
|---|---|---|
| **Antifact** | Thiết kế, chỉnh ảnh | [antiface.vtvcab17.workers.dev](https://antiface.vtvcab17.workers.dev/) |
| [Bravin](https://github.com/vtvcab17-max/Bravin) | Dựng video | [bravin.vtvcab17.workers.dev](https://bravin.vtvcab17.workers.dev/) |
| [Micron](https://github.com/vtvcab17-max/micron) | Canvas AI, plugin cho Bravin | [micron.vtvcab17.workers.dev](https://micron.vtvcab17.workers.dev/) |
| [Micow](https://github.com/vtvcab17-max/Micow) | Làm nhạc trên máy | [micow.vtvcab17.workers.dev](https://micow.vtvcab17.workers.dev/) |

---

<p align="center">© 2026 Phạm Việt Hà · <a href="https://bravinall.vtvcab17.workers.dev/">Bravinall</a></p>
