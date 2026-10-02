```mermaid
flowchart TD
    A([Mulai]) --> B[/"Cetak judul program"/]
    B --> C[/"Input n (jumlah data)"/]
    C --> D{"n kurang dari atau sama dengan 0 ?"}
    D -- Ya --> E[/"Cetak pesan error"/]
    E --> C
    D -- Tidak --> F["i := 0"]
    F --> G{"i lebih kecil dari n ?"}
    G -- Ya --> H[/"Cetak Data ke-(i+1) dan Input data[i]"/]
    H --> I["i := i + 1"]
    I --> G
    G -- Tidak --> J[["sort(data, data + n)"]]
    J --> K[["mean := hitungMean(data, n)"]]
    K --> L[["median := hitungMedian(data, n)"]]
    L --> M[["modus := hitungModus(data, n)"]]
    M --> N["minimum := data[0]<br>maksimum := data[n-1]<br>range := maksimum - minimum"]
    N --> O[["q1 := hitungQ1(data, n)<br>q3 := hitungQ3(data, n)"]]
    O --> P["iqr := q3 - q1<br>lowerFence := q1 - 1.5 * iqr<br>upperFence := q3 + 1.5 * iqr"]
    P --> Q[["varians := hitungVarians(data, n, mean)"]]
    Q --> R[["standarDeviasi := hitungStandarDeviasi(varians)"]]
    R --> S[["skewness := hitungSkewness(data, n, mean, standarDeviasi)"]]
    S --> T[["tampilkanData(data, n)"]]
    T --> U[/"Cetak judul HASIL ANALISIS<br>Cetak Mean dan Median"/]
    U --> V{"isnan(modus) ?"}
    V -- Ya --> W[/"Tidak ada modus"/]
    V -- Tidak --> X[/"Cetak modus"/]
    W --> Y[/"Cetak Q1, Q3, IQR<br>Cetak Lower Fence, Upper Fence<br>Cetak info batas Z-Score"/]
    X --> Y
    Y --> Z[["analisisOutlier(data, n, ...)"]]
    Z --> AA[/"Cetak Maximum dan Minimum<br>Cetak Range<br>Cetak Varians, Standar Deviasi"/]
    AA --> AB[["analisisEkor(skewness)"]]
    AB --> AC[["tampilkanKurva(data, n)"]]
    AC --> AD([Selesai])
```
