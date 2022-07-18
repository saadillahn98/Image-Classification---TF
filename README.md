# Image-Classification-TensorFlow Hub

Dalam project ini, saya mencoba mengklasifikasikan gambar dengan menggunakan pembelajaran transfer dari jaringan yang telah dilatih sebelumnya.  Intuisi di balik pembelajaran transfer untuk klasifikasi gambar adalah bahwa jika model dilatih pada kumpulan data yang cukup besar dan umum, model ini akan secara efektif berfungsi sebagai model umum dunia visual. Kemudian dapat memanfaatkan peta fitur yang dipelajari ini tanpa harus memulai dari awal dengan melatih model besar pada kumpulan data yang besar.  Kemudian akan mencoba dua cara untuk menyesuaikan model yang sudah dilatih sebelumnya :  Ekstraksi fitur, representasi yang dipelajari oleh jaringan sebelumnya untuk mengekstrak fitur yang berarti dari sampel baru Fine-Tuning, Mencairkan beberapa lapisan atas dari basis model yang dibekukan dan bersama-sama melatih lapisan pengklasifikasi yang baru ditambahkan dan lapisan terakhir dari model dasar

# Kesimpulan

Menggunakan model yang telah dilatih sebelumnya untuk ekstraksi fitur : Saat bekerja dengan kumpulan data kecil, merupakan praktik umum untuk memanfaatkan fitur yang dipelajari oleh model yang dilatih pada kumpulan data yang lebih besar dalam domain yang sama. Ini dilakukan dengan membuat instance model yang telah dilatih sebelumnya dan menambahkan classifier yang terhubung penuh di atasnya. Model pra-pelatihan "dibekukan" dan hanya bobot pengklasifikasi yang diperbarui selama pelatihan. Dalam hal ini, basis konvolusi mengekstrak semua fitur yang terkait dengan setiap gambar dan Kita baru saja melatih pengklasifikasi yang menentukan kelas gambar yang diberikan kumpulan fitur yang diekstraksi.

Menyesuaikan model yang telah dilatih sebelumnya : Untuk lebih meningkatkan kinerja, seseorang mungkin ingin menggunakan kembali lapisan tingkat atas dari model yang telah dilatih sebelumnya ke kumpulan data baru melalui penyetelan halus. Dalam hal ini, Kita menyetel bobot Anda sedemikian rupa sehingga model Anda mempelajari fitur tingkat tinggi khusus untuk kumpulan data. Teknik ini biasanya direkomendasikan ketika dataset pelatihan besar dan sangat mirip dengan dataset asli yang digunakan untuk melatih model pra-pelatihan.
