# PRD: Mini Kasir Toko Jam Tangan (Web-based)

## 1. Ringkasan Produk
**Nama:** Mini Kasir Toko Jam Tangan
**Platform:** Web-based (PWA)
**Target:** Toko jam tangan skala kecil
**Format:** Mobile-first responsive

Aplikasi kasir sederhana untuk toko jam tangan skala kecil, fitur utama: pemasukan, pengeluaran, kasbon.

---

## 2. Latar Belakang
- Sistem POS kompleks mahal
- Internet terbatas di daerah pedesaan  
- HP lama tidak kuat aplikasi berat
- Kebutuhan pencatatan sederhana

---

## 3. User Stories
1. Pemilik: catat penjualan jam untuk lacak pemasukan harian
2. Kasir: catat pembelian stok dari supplier
3. Pemilik: catat kasbon karyawan/pelanggan
4. Pemilik: lihat laporan keuangan sederhana
5. Pengguna: aplikasi tetap jalan saat internet putus

---

## 4. Kebutuhan Fungsional

### Modul Transaksi
**Penjualan (Pemasukan)**
- Input: nama jam, harga, jumlah, total
- Pembayaran: tunai, transfer, kasbon
- Cetak struk via browser print
- Riwayat transaksi

**Pembelian (Pengeluaran)**
- Input: nama supplier, jumlah, keterangan
- Kategori: stok, operasional
- Riwayat pengeluaran

**Kasbon**
- Input: nama peminjam, jumlah
- Status: belum lunas/lunas
- Pembayaran kasbon

### Modul Laporan
- Laporan harian/bulanan
- Export CSV/PDF

### Master Data
- Produk: nama, harga beli/jual, stok
- Supplier: nama, kontak

---

## 5. Kebutuhan Non-Fungsional
- Bundle < 500KB minified
- Mobile-first, min 320px
- Offline via Service Worker + IndexedDB
- Browser: Chrome 60+, Firefox 55+, Safari 12+
- Bahasa Indonesia

---

## 6. Teknologi
Frontend: Vanilla JS + Tailwind CSS
Database: IndexedDB (local)
PWA: Manifest + Service Worker

---

## 7. Routes
/      -> Dashboard
/penjualan  -> Penjualan
/pembelian  -> Pembelian  
/kasbon     -> Kasbon
/produk     -> Produk
/laporan    -> Laporan
/pengaturan -> Pengaturan

---

## 8. Roadmap (4 minggu)
Minggu 1: Setup, database, dashboard, pemasukan
Minggu 2: Pengeluaran, kasbon, offline, produk
Minggu 3: Laporan, export, testing HP lama
Minggu 4: Optimasi bundle, UI polish, dokumentasi

---

## 9. Kriteria Penerimaan
1. Buka di HP < 3 detik
2. Semua fitur via HP portrait
3. Auto-save ke IndexedDB
4. Form maks 3 langkah
5. Bundle < 500KB

---

## 10. Risiko
- Internet lambat: Local-first
- Perangkat lama: Minify JS
- Data hilang: Auto backup + export
