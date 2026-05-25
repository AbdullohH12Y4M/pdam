# UI Overview for PDAM Project

Dokumen ini mencantumkan semua file, folder, dan konfigurasi yang mempengaruhi antarmuka pengguna (UI) di proyek ini.

## 1. Konfigurasi Styling dan UI Global

- `tailwind.config.ts`
  - Menentukan konten Tailwind CSS yang dipindai (`app/**/*` dan `components/**/*`).
- `postcss.config.mjs`
  - Mengaktifkan plugin PostCSS untuk Tailwind CSS.
- `app/globals.css`
  - Import Tailwind CSS dan plugin animasi.
  - Mendefinisikan variabel tema global untuk warna, radius, dan mode `.dark`.
- `app/layout.tsx`
  - Layout root Next.js yang memuat font Google dan file CSS global.
  - Mempengaruhi seluruh aplikasi karena menjadi root layout.

## 2. Dependensi UI Penting

- `package.json`
  - `tailwindcss`, `@tailwindcss/postcss`, `tailwind-merge`, `tailwindcss-animate`, `tw-animate-css`
  - `@radix-ui/react-dialog`, `@radix-ui/react-slot`
  - `lucide-react`
  - `react-toastify`
  - `recharts`

## 3. Komponen UI Dasar (Design System)

Folder utama komponen UI atomik dan reusable.

- `app/components/ui/alert-dialog.tsx`
- `app/components/ui/badge.tsx`
- `app/components/ui/button.tsx`
- `app/components/ui/card.tsx`
- `app/components/ui/combobox.tsx`
- `app/components/ui/dialog.tsx`
- `app/components/ui/dropdown-menu.tsx`
- `app/components/ui/field.tsx`
- `app/components/ui/input.tsx`
- `app/components/ui/input-group.tsx`
- `app/components/ui/label.tsx`
- `app/components/ui/pagination.tsx`
- `app/components/ui/select.tsx`
- `app/components/ui/separator.tsx`
- `app/components/ui/sheet.tsx`
- `app/components/ui/sidebar.tsx`
- `app/components/ui/skeleton.tsx`
- `app/components/ui/table.tsx`
- `app/components/ui/textarea.tsx`
- `app/components/ui/tooltip.tsx`

## 4. Komponen UI Tambahan

- `app/components/Search/index.tsx`
  - Komponen pencarian yang digunakan di UI.
- `app/components/Pagination/index.tsx`
  - Komponen paginasi khusus.

## 5. Layout dan Template Global untuk Admin dan Customer

### Layout Root
- `app/admin/layout.tsx`
- `app/cust/layout.tsx`

### Template Admin
- `app/components/admin-template/app-header.tsx`
- `app/components/admin-template/app-sidebar.tsx`

### Template Customer
- `app/components/cust-template/app-sidebar.tsx`
- `app/cust/components/cust-template/app-sidebar.tsx`

## 6. Halaman Utama dan Autentikasi

- `app/page.tsx`
- `app/sign-in/page.tsx`
- `app/sign-up/page.tsx`

## 7. Halaman Admin

- `app/admin/dashboard/page.tsx`
- `app/admin/dashboard/dashboard-chart.tsx`
- `app/admin/dashboard/admin-profile-content.tsx`
- `app/admin/admin-data/page.tsx`
- `app/admin/bill/page.tsx`
- `app/admin/bill/add.tsx`
- `app/admin/bill/edit.tsx`
- `app/admin/bill/delete.tsx`
- `app/admin/customer/page.tsx`
- `app/admin/customer/add.tsx`
- `app/admin/customer/edit.tsx`
- `app/admin/customer/delete.tsx`
- `app/admin/customer/reset-password.tsx`
- `app/admin/services/page.tsx`
- `app/admin/services/add.tsx`
- `app/admin/services/edit.tsx`
- `app/admin/services/delete.tsx`
- `app/admin/profile/page.tsx`
- `app/admin/profile/form.tsx`
- `app/admin/payments/page.tsx`

## 8. Halaman Customer

- `app/cust/dashboard/page.tsx`
- `app/cust/dashboard/customer-dashboard-content.tsx`
- `app/cust/dashboard/chart.tsx`
- `app/cust/profile/page.tsx`
- `app/cust/payments/page.tsx`
- `app/cust/payments/action.ts`
- `app/cust/bills/page.tsx`
- `app/cust/bills/[id]/page.tsx`
- `app/cust/bills/delete.tsx`
- `app/cust/bills/filters.tsx`
- `app/cust/bills/payment.tsx`
- `app/cust/bills/proof.tsx`

## 9. Hook dan Utilitas UI

- `app/hooks/use-mobile.ts`
  - Membantu deteksi tampilan mobile / responsive.

## 10. File UI Tambahan di Root

- `components/ui/button.tsx`
  - Komponen button tambahan yang berada di luar folder `app/components/ui`.

## 11. File yang Berpotensi Mempengaruhi UI Secara Tidak Langsung

- `next.config.ts`
  - Mempengaruhi routing, config Next.js, dan potensi behavior aplikasi.
- `app/types.ts`
  - Tipe data yang digunakan oleh UI, meski bukan komponen visual langsung.

---

> Catatan: Dokumen ini disusun berdasarkan struktur file saat ini. Jika ada file UI baru ditambahkan nanti, maka `UI-Overview.md` perlu diperbarui kembali.
