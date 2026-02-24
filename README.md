#**Case Study 2: Differential Gene Expression Profiling in Tuberculosis Using GEO2R**
**Background:** Studi kasus ini merupakan implementasi analisis Differentially Expressed Genes (DEG) menggunakan dataset publik GSE62525 dari database Gene Expression Omnibus (GEO). Dataset ini berisi data transcriptomics berbasis microarray dari peripheral blood mononuclear cells (PBMC) individu dengan tuberkulosis aktif, infeksi laten, serta individu sehat. Analisis dilakukan menggunakan GEO2R sebagai web-based tool untuk membandingkan profil ekspresi gen antara kelompok terinfeksi dan kelompok kontrol.

**Project Purpose:**
1. Mengeksplorasi dataset transcriptomics publik dari GEO
2. Melakukan analisis Differential Expression berbasis web menggunakan GEO2R
3. Mengidentifikasi gen yang mengalami upregulation dan downregulation pada infeksi TB
4. Memahami keterkaitan perubahan ekspresi gen dengan respons imun terhadap infeksi
5. Melatih interpretasi hasil statistik transcriptomics
Studi ini juga berfungsi sebagai latihan dalam memahami alur analisis DEG secara sistematis dan reproducible.

**Dataset and Experimental Design**
Dataset: GSE62525
*Platform: Phalanx Human OneArray Ver. 6 (Microarray)
*Sampel:
- Active TB
- Latent TB
- Healthy controls
*Dalam analisis ini:
- Group 1 (Infected): Active TB + Latent TB
- Group 2 (Healthy): Individu sehat

**Analytical Parameters (GEO2R)**
  Analisis dilakukan menggunakan metode statistik limma (Linear Models for Microarray Data) yang terintegrasi dalam GEO2R, dengan parameter:
  - Multiple testing correction: Benjamini–Hochberg (False Discovery Rate)
  - Kriteria signifikan: adjusted p-value < 0.05
  - Interpretasi arah perubahan berdasarkan nilai log2 fold change
  Untuk memastikan konsistensi hasil, analisis direplikasi sebanyak tiga kali dengan parameter yang sama. Hasil antar replikasi menunjukkan pola yang konsisten dalam jumlah gen signifikan dan arah perubahan ekspresi.

**Key Findings:**
Hasil analisis menunjukkan adanya sejumlah gen yang mengalami perubahan ekspresi signifikan antara kelompok terinfeksi dan sehat.
- Gen dengan log2FC positif → dikategorikan sebagai up-regulated pada kelompok terinfeksi
- Gen dengan log2FC negatif → dikategorikan sebagai down-regulated
Visualisasi volcano plot menunjukkan dominasi gen yang mengalami peningkatan ekspresi pada kelompok terinfeksi, mengindikasikan aktivasi transkripsional yang luas sebagai respons terhadap infeksi Mycobacterium tuberculosis. Pola ini konsisten dengan mekanisme biologis tuberkulosis yang melibatkan aktivasi sistem imun bawaan dan adaptif, termasuk jalur inflamasi dan regulasi sitokin pada sel mononuklear darah perifer.

**Biological Interpretation**
  Infeksi Mycobacterium tuberculosis memicu respons imun kompleks yang tercermin dalam perubahan ekspresi gen pada PBMC. Peningkatan ekspresi gen pada kelompok terinfeksi kemungkinan berkaitan dengan:
  - Aktivasi respons inflamasi
  - Produksi sitokin proinflamasi
  - Regulasi pertahanan terhadap patogen intraseluler
  Sementara itu, gen yang mengalami downregulation dapat mencerminkan perubahan homeostasis seluler atau mekanisme regulasi negatif sistem imun. Temuan ini menunjukkan bahwa pendekatan transcriptomics berbasis microarray dapat mengidentifikasi kandidat biomarker molekuler yang membedakan individu terinfeksi dan sehat.

**Skills Developed**
  Melalui studi ini, kemampuan yang dikembangkan meliputi:
  - Navigasi dan eksplorasi database GEO
  - Evaluasi dan pemilihan dataset transcriptomics
  - Implementasi analisis DEG menggunakan GEO2R
  - Interpretasi volcano plot dan hasil statistik
  - Evaluasi reproducibility hasil analisis
