# Lets-Defend-Hubungan-SIEM-dan-Analis
Hubungan SIEM dan Analis

Pelajaran ini membahas apa itu SIEM, mengapa SIEM digunakan di SOC, dan bagaimana SIEM berhubungan dengan analis SOC.



Apa itu SIEM?
SIEM adalah solusi keamanan yang menggabungkan manajemen informasi dan peristiwa keamanan, yang melibatkan pencatatan peristiwa secara real-time di suatu lingkungan. Tujuan utama pencatatan peristiwa adalah untuk mendeteksi ancaman keamanan.



Secara keseluruhan, produk SIEM memiliki banyak fitur. Fitur yang paling menarik bagi kami sebagai analis SOC adalah fitur yang mengumpulkan dan menyaring data serta memberikan peringatan untuk kejadian mencurigakan.



Contoh peringatan: Jika seseorang pada sistem operasi Windows mencoba memasukkan 20 kata sandi yang salah dalam 10 detik, ini adalah aktivitas mencurigakan. Tidak mungkin seseorang yang lupa kata sandinya akan mencoba memasukkannya kembali sebanyak itu dalam waktu sesingkat itu. Oleh karena itu, kami membuat aturan/filter SIEM untuk mendeteksi aktivitas yang melebihi ambang batas tersebut. Berdasarkan aturan SIEM ini, peringatan akan dihasilkan ketika situasi seperti itu terjadi.

<img width="540" height="582" alt="image" src="https://github.com/user-attachments/assets/719874bf-40fd-4c97-bb34-bb34815c1056" />

Beberapa solusi SIEM populer: IBM QRadar, ArcSight ESM, FortiSIEM, Splunk, dll. Untuk mendapatkan gambaran yang lebih baik, Anda dapat mengunjungi halaman "Monitoring" di LetsDefend.
<img width="1128" height="424" alt="image" src="https://github.com/user-attachments/assets/4cdb8ec2-ea5a-4ada-b565-1731509849b4" />

Hubungan Antara Analis SOC dan SIEM
Meskipun solusi SIEM memiliki banyak fitur, analis SOC biasanya hanya melacak peringatan. Ada kelompok/orang lain yang bertanggung jawab untuk mengembangkan konfigurasi dan korelasi aturan.

Hubungan Antara Analis SOC dan SIEM
Meskipun solusi SIEM memiliki banyak fitur, analis SOC biasanya hanya melacak peringatan. Ada kelompok/orang lain yang bertanggung jawab untuk mengembangkan konfigurasi dan korelasi aturan.



Seperti yang disebutkan di atas, peringatan dihasilkan dari data yang melewati filter. Peringatan pertama-tama dianalisis oleh seorang analis SOC. Di sinilah pekerjaan seorang analis SOC di pusat operasi keamanan dimulai. Pada intinya, mereka harus menentukan apakah peringatan yang dihasilkan merupakan ancaman nyata atau peringatan palsu.



Untuk pemahaman yang lebih baik, mari kita kembali ke halaman "Pemantauan"; seperti yang Anda lihat di bawah, terdapat berbagai peringatan pada antarmuka SIEM. Seorang analis SOC harus menganalisis detail yang terkait dengan peringatan ini dengan bantuan produk SOC lainnya (seperti EDR, Manajemen Log, Umpan Intelijen Ancaman, dll.) dan pada akhirnya menentukan apakah itu ancaman nyata atau bukan.

<img width="1195" height="703" alt="image" src="https://github.com/user-attachments/assets/f9f29b0c-485d-4362-85af-09caf905ae2c" />

Anda dapat melihat peringatan yang baru dibuat di "Saluran Utama" dan menganggap saluran ini sebagai saluran bersama. Rekan tim Anda tidak terlihat dalam simulasi ini, tetapi dalam skenario kerja nyata, rekan tim Anda akan dapat melihat panel ini. Setelah Anda memilih peringatan yang ingin Anda kerjakan, klik tombol Ambil Kepemilikan di area Tindakan untuk mengambil kepemilikan peringatan tersebut dan mengarahkannya ke Saluran Investigasi. Dengan cara ini, rekan tim Anda dapat melihat peringatan mana yang sedang Anda kerjakan. Pada saat yang sama, ini akan membantu mereka melihat peringatan mana yang sudah Anda kerjakan sehingga mereka dapat memilih peringatan lain. Dengan cara ini, tim Anda dapat dengan cepat meninjau semua peringatan.



Saat Anda mengklik peringatan tersebut, Anda dapat melihat detail peringatan. Ini memungkinkan Anda untuk mengumpulkan informasi (nama host, alamat IP, informasi hash file, dll.) yang diperlukan untuk melakukan investigasi.



Tips Cepat
Perlu dicatat bahwa terkadang, peringatan palsu dapat dihasilkan di SIEM. Seorang analis SOC yang baik akan mampu mengidentifikasi situasi tersebut dan memberikan umpan balik kepada tim, sehingga berkontribusi pada efisiensi tim SOC.



Contoh:
Misalnya, sebuah tim SIEM telah menyusun seperangkat aturan yang menghasilkan peringatan untuk alamat URL yang mengandung kata "union" dan mencoba mendeteksi serangan SQL injection.



Seorang pengguna melakukan pencarian menggunakan "https://www.google.com/search?q=sql+union+usage", dan sebuah peringatan dibuat di SIEM, tampaknya tidak ada ancaman yang jelas. Peringatan tersebut dihasilkan karena kata kunci "union" disertakan dalam URL. Anomali semacam ini dapat dibagikan dengan tim SIEM untuk mengoptimalkan proses peringatan.



Kata Penutup
Sejauh ini, kita telah membahas apa itu SIEM, bagaimana SIEM membantu analis SOC, dan bagaimana seharusnya digunakan. Nanti dalam kursus ini, kita akan membahas cara menganalisis peringatan yang dibuat di SIEM.

Pertanyaan
Benar

Saat Anda menutup peringatan, dari saluran (tab pada halaman pemantauan) mana Anda dapat mengaksesnya?
closed alerts
