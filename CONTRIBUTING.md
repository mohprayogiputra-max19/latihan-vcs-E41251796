# Contributing Guide

Dokumen ini menetapkan standar alur kerja Git untuk proyek pengembangan web berbasis **Laravel, Tailwind CSS, Node.js/Vite, dan MySQL**.

## Branch Convention
Format: `<type>/<short-description>` atau `<type>/<nomor-tiket>-<short-description>`

| Type | Kegunaan | Contoh Benar | Contoh Salah |
| :--- | :--- | :--- | :--- |
| `feature/` | Fitur baru | `feature/123-user-login` | `Feature/Login_Baru` |
| `fix/` | Bug fix | `fix/cart-total` | `fix bug total` |
| `hotfix/` | Darurat production | `hotfix/payment-down` | `hotfix_urgent` |
| `refactor/` | Refactor kode | `refactor/order-service` | `refactorOrder` |
| `docs/` | Dokumentasi | `docs/api-reference` | `update-docs` |
| `test/` | Pengujian otomatis | `test/checkout-flow` | `testing` |
| `chore/` | Maintenance | `chore/update-deps` | `chore` |

**Aturan:**
- Huruf kecil semua (*lowercase*).
- Gunakan hyphen (`-`), bukan spasi atau underscore (`_`).
- Sertakan nomor tiket bila ada, maksimal 50 karakter.

## Commit Convention
Format: `<type>(<scope>): <subject>`

**Type:** `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `build`, `ci`, `chore`, `revert`

**Contoh Benar:**
- `feat(auth): add JWT refresh token`
- `fix(cart): correct total when discount applied`
- `docs(readme): update installation steps`

**Contoh Salah:**
- `update file`
- `fix bug login.`
- `WIP: ngerjain controller`

**Aturan:**
- Subject lowercase, imperative mood, tanpa tanda titik akhir.
- Maksimal 50 karakter untuk subject.
- Body dipisah 1 baris kosong dengan referensi issue (`Closes #123`).

## Pull Request
- Judul PR mengikuti format commit message.
- Ukuran PR disarankan kurang dari 400 baris.
- Wajib minimal 1 reviewer approval dan lolos CI.
- Gunakan metode **Squash and merge**.

## Code Review
Label komentar saat melakukan review:
- `blocking:` harus diperbaiki sebelum merge.
- `nit:` saran kecil, bersifat opsional.
- `question:` butuh klarifikasi.
- `praise:` apresiasi kode yang baik.

## Workflow
1. `git checkout main && git pull origin main`
2. `git checkout -b feature/xxx`
3. Kerjakan perubahan dengan commit atomik.
4. `git push -u origin feature/xxx`
5. Buat Pull Request di GitHub.
6. Tunggu review & CI.
7. Lakukan **Squash and merge**.
8. Hapus branch setelah merge.

## Yang Dilarang
- Push langsung ke `main`.
- Commit message tidak jelas (`wip`, `test`, `asdf`).
- Commit file `.env`, `node_modules/`, maupun credentials.
- Rebase branch yang sudah di-push dan dipakai orang lain.
