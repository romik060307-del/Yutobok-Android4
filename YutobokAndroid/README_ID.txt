YUTOBOK ANDROID — PROJECT SOURCE + GITHUB ACTIONS APK BUILD

Struktur repository yang benar:
- .github/workflows/build.yml   (workflow harus berada di root repository)
- YutobokAndroid/               (project Android)

MENGHASILKAN APK TANPA ANDROID STUDIO
1. Unggah/ekstrak isi ZIP ini ke root repository GitHub. Pastikan folder .github dan YutobokAndroid sejajar di root.
2. Buka tab Actions.
3. Pilih workflow "Build Yutobok APK", lalu klik Run workflow.
4. Tunggu sampai run berstatus sukses.
5. Buka run tersebut dan unduh artifact "Yutobok-Android-APK".
6. Ekstrak ZIP artifact untuk mendapatkan app-debug.apk.

CATATAN
- Project sumber ini tidak menyertakan Gradle wrapper (gradlew). Workflow memasang Gradle 8.9 secara otomatis sehingga tidak bergantung pada file wrapper.
- Workflow menggunakan Java 17, Android SDK platform 35, serta build-tools 35.0.0.
- APK debug cocok untuk pengujian/pemasangan pribadi, bukan pengganti APK release bertanda tangan untuk distribusi resmi.
- Halaman memakai beberapa aset web dari CDN, jadi tampilan lengkap membutuhkan internet. Video pihak ketiga masih bergantung pada koneksi, sumber video, format, dan dukungan Android WebView.
- APK baru tersedia setelah GitHub Actions berhasil menyelesaikan proses build.
