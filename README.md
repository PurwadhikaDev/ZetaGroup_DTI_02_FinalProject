# **<big> HOTEL BOOKING CANCELLATION PREDICTION </big>**

Group Contibutors :
1. Ergia Lativolia Putri Subiyantari
2. Diah Purnamaningsih Mulyawan
3. Kezia Patricia Fadli

## [Business Problem Analytics:](https://example.com)
Terdapat sebuah perusahaan yang bergerak dibidang hospitality industry-khususnya perhotelan-dan berlokasi di Portugal. memiliki dataset yang telah diekstrak dari database hotel (Property Management System (PMS) [6], yang mencatat berbagai aspek reservasi, termasuk status pembatalan, harga kamar (ADR), lama menginap, dan lainnya. Industri perhotelan termasuk dalam sektor lodging, yang berperan penting dalam menyediakan akomodasi bagi wisatawan domestik maupun internasional. 

Dari laporan industry Crishty & CO, 2023 [3]. Sebelumnya, lebih dari 28.4 juta wisatawan mengunjungi Portugal, berkontribusi hampir 16% terhadap GDP negara. 
Wilayah seperti Lisbon, Algarve, dan Madeira menjadi pusat wisata utama, dengan lebih dari 70% dari total menginap berasal dari turis internasional. 
Perubahan tren wisata juga terlihat, Portugal telah melampaui Spanyol sebagai sumber utama wisatawan di Lisbon. 
Laporan industry, "Staying Power”  memprediksi Occupancy Rate meningkat pada 2016 dan 2017 di Lisbon, tetapi hasil analisis kami justru menunjukkan penurunan, terutama di City Hotel. 
Ada beberapa kemungkinan penyebabnya:
•	Over-Supply Hotel: Lisbon mengalami lonjakan jumlah hotel baru, yang meningkatkan persaingan dan berdampak pada okupansi hotel tertentu.
•	Perubahan Tren Wisatawan: Faktor event global, keamanan, dan ekonomi menggeser pola perjalanan, dengan preferensi lebih tinggi ke Resort Hotel dibanding City Hotel.

Menurut laporan industry Staying Power, 2015 -2017[2], melaporkan jika, Portugal mengalami pertumbuhan ekonomi 1.6%-1.7%,dengan wisatawan meningkat akibat melemahnya Euro dan meningkatnya konektivitas penerbangan. 
Namun, beberapa faktor global memengaruhi wisatawan, seperti: 
- Ketidakpastian ekonomi seperti Brexit atau serangan teror dapat menyebabkan penurunan perjalanan bisnis, sehingga meningkatkan Cancellation Ratio di City Hotel (0.44) dan menurunkan Occupancy rgrowth (-11% di 2016, -6% di 2017).
  Dalam analisis kami, City Hotel lebih terdampak oleh faktor global karena banyak wisatawannya adalah pebisnis atau peserta event internasional(Group).
  Wisatawan "contract" dan "group" umumnya sudah merencanakan perjalanan jauh-jauh hari,
  sehingga Cancellation Ratio di Resort Hotel lebih rendah (0.31) dan Occupancy rate lebih baik ( 67%-79%) dengan occupancy growth (-5% &  -10%).
  Dalam analysis kami, Resort Hotel lebih stabil karena didukung oleh contract dan group hotel, yang cenderung tidak terlalu bergantung pada faktor ekonomi dan politik. 
-	Fluktuasi mata uang (melemahnya Euro) seharusnya meningkatkan wisatawan dari luar zona Euro, tetapi dalam dataset kami, justru City Hotel mengalami penurunan okupansi.
  Ini bisa terjadi jika wisatawan lebih memilih destinasi resort untuk liburan panjang dibanding perjalanan bisnis ke pusat kota. 

Cancellation Rate di dataset kami mencapai 30% untuk city hotel dan 23.7% untuk resort, lebih RENDAH dibanding rata-rata global yang berkisar 33%-40% (Hospitalitytech, 2019)[3]. 
Resort Hotel lebih stabil dengan Cancellation Ratio 0.31. Cancellation Rate yang tinggi di City Hotel bisa disebabkan oleh segmen wisatawan bisnis yang lebih fleksibel dalam mengubah rencana perjalanan. 
Dan pada dataset kami Custoemr tyoe yang paling memepngaruhi adalah transient (customer flexible).

Untuk Dampak Musiman (Seasonality) terhadap Occupancy Rate, pada;
•	Peak Season (Sep-Nov) = Okupansi tinggi, terutama di Resort Hotel. Salah satu direct booking web Agarve resort Portugal, 
pada awal musim gugur ini diadakan off season promo 15% dengan lead time of staying 5-6 hari [4]. 
Dan september = October adalah waktu yang tepat untuk berlibur ke Agarve karean pergantian dari musim dingin[5].
•	Low Season (Apr-Jun) = Stabil tetapi lebih rendah dibanding puncak wisata.
•	Off-Season (Des & Ags) pada musim dingin dan akhir musim panas = Okupansi turun signifikan, terutama di City Hotel.
•	ADR meningkat di City Hotel dengan perolehan , 32.5 EUR pada 2015, 36.2 EUR dan 2016, dan 38.9EUR pada 2017, kemungkinan karena strategi harga yang terlalu tinggi, sehingga okupansi menurun sekitar -11% & -5%. Sedangkankan pada laporan staying power 2015-2017 [2], ADR Lisbon(jika didataset kami city hotel adalah data dari beberapa atau salah satu hotel di Lisbon)
mengalami peningkatan 95-99 EUR, dikarenakan tahun 2016 terdapat big event seperti s the Web Summit (wrested from Dublin) and Diabetes, as well as new air routes,
should drive demand further putting pressure on ADR and pushing occupancy to record high levels. Accordingly we expect another good year in 2016. 

Target Feature (is_canceled):

1 : Cancel (positif)
0 : No Cancel (negatif)

## [Project Stakeholders:](https://example.com)
Project Stakeholders:
- Marketing & Sales Departement : Departement ini bertanggungjawab untuk memaksimalkan revenue dengan cara melakukan beberapa strategi marketing (ex: promosi/diskon) kepada pelanggan, sehingga dengan model ini Marketing dan Sales Departement bisa mengetahui pelanggan yang tepat untuk diberi promosi/diskon.
- Revenue Management : Salah satu tugas Finance Departement adalah mengatur pemasukan dan pengeluaran keuangan perusahaan yang salah satunya diakibatkan dari promosi/campaign yang diadakan Marketing dan Sales Departement.

Pada dasarnya, kedua departement ini saling berkesinambungan dan memiliki pertanyaan/tujuan yang sama, yaitu bagaimana caranya memaksimalkan revenue perusahaan.

## [Analytic Approach:](https://example.com)
Jadi yang akan kita lakukan adalah menganalisis data untuk menemukan pola yang membedakan pelanggan yang akan membatalkan pesanan atau tidak.

Kemudian kita akan membangun model supervised machine learning klasifikasi yang akan membantu perusahaan untuk dapat memprediksi pelanggan yang akan membatalkan pesanan atau tidak.

## [Metric Evaluation:](https://example.com)
Type I Error: False Positive Kondisi di mana pelanggan terprediksi membatalkan pesanan padahal kenyataannya tidak membatalkan pesanan Konsekuensinya: promosi tidak tepat sasaran, sehingga revenue tidak maksimal. Tanpa mengadakan marketing, pihak hotel bisa mendapatkan 101 EUR.

Type II Error: False Negative Kondisi di mana pelanggan terprediksi tidak membatalkan pesanan padahal kenyataannya membatalkan pesanan Konsekuensinya: pihak hotel kehilangan potential pelanggan dan tentu saja berdampak pada kehilangan revenue. Berdasarkan dataset ini, rata-rata biaya marketing adalah 10.07 - 10.14 EUR. Sehingga, untuk worst case-nya pihak hotel mendapatkan ADR sekitar 113.2EUR tanpa biaya marketing.

## [Sources:](https://example.com)

[1] [Nama Tampil]([https://example.com](https://assets-eu-01.kc-usercontent.com/6bb3df3c-b648-01ae-2357-22fa5c7d5f19/93b732c7-e612-4890-88f4-31d2996a52eb/Portugal%20Hotel%20Market%20Performance%202023))
[2] [Nama Tampil](https://www.pwc.ch/en/publications/2016/european-cities-hotel-forecast-2016-2017.pdf)
[3] [Nama Tampil](https://hospitalitytech.com/global-cancellation-rate-hotel-reservations-reaches-40-average) 
[4] [Nama Tampil](https://algarveresorts.net/en/promocoes/ver/6)
[5] [Nama Tampil](https://myportugalholiday.com/portugal-guides/portugal-september.html#google_vignette)
[6] [Nama Tampil](https://www.sciencedirect.com/science/article/pii/S2352340918315191) 
[7] [Nama Tampil](https://www.bdc.ca/en/articles-tools/marketing-sales-export/marketing/what-average-marketing-budget-for-small-business#:~:text=1.-,Start%20by%20researching%20your%20industry,%E2%80%94between%205%20and%2010%25.)
