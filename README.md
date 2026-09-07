# Catify 🤝 Tranquil Mind Studio — Premium App Center

Hub web phân phối bản build (Dev / Live / AAB) cho các app của đối tác **Catify**.

- **Domain chính**: https://catify-app.tranquilmind.co
- **Mirror**: https://conmangangqua.github.io/catify_app/
- **Trang kiểm tra**: `/check.html`

## Cách app xuất hiện trên hub
CI của mỗi app đẩy artifact lên GitHub Release của repo này; workflow
`.github/workflows/update-apps-json.yml` quét Release rồi cập nhật `apps.json`
(kèm version từ file sidecar `<id>_<env>.version`), sau đó `deploy-pages.yml`
publish GitHub Pages. Vercel tự deploy theo mỗi lần push.

## File dữ liệu
| File | Vai trò |
|---|---|
| `apps.json` | Danh sách app + link tải (CI sinh, không sửa tay) |
| `versions.json` | Version từng env (CI sinh) |
| `stores.json` | Link store công khai (CI sinh) |
| `names.json` | Tên listing ASO (CI sinh) |
| `category_overrides.json` | Ép category thủ công — ưu tiên cao nhất |
