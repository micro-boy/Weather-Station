# RENCANA ANGGARAN BIAYA (RAB)
## SISTEM SENSOR CUACA OTOMATIS

### A. KOMPONEN UTAMA SISTEM

#### 1. Sensor Cluster
| No | Komponen | Spesifikasi | Qty | Harga Satuan | Total |
|----|----------|-------------|-----|--------------|-------|
| 1 | BME680 | Sensor suhu, humidity, barometer | 1 | Rp 450,000 | Rp 450,000 |
| 2 | Anemometer | Sensor kecepatan angin | 1 | Rp 450,000 | Rp 450,000 |
| 3 | Wind Direction Sensor | Sensor arah angin | 1 | Rp 450,000 | Rp 450,000 |
| 4 | Ombrometer | Sensor curah hujan | 1 | Rp 450,000 | Rp 450,000 |
| 5 | Ambient Light Sensor | Sensor intensitas cahaya | 1 | Rp 250,000 | Rp 250,000 |
| 6 | UV Sensor | Sensor UV | 1 | Rp 250,000 | Rp 250,000 |
| 7 | PM2.5 Sensor | Sensor kualitas udara (Optional) | 1 | Rp 1,000,000 | Rp 1,000,000 |
| **Subtotal Sensor** | | | | | **Rp 3,300,000** |

#### 2. Core System Components
| No | Komponen | Spesifikasi | Qty | Harga Satuan | Total |
|----|----------|-------------|-----|--------------|-------|
| 8 | ESP32 WEMOS D1 MINI | Microcontroller utama | 1 | Rp 100,000 | Rp 100,000 |
| 9 | Arduino Nano V3 | Microcontroller slave | 2 | Rp 60,000 | Rp 120,000 |
| 10 | Logic Level Converter | Penghubung antar sistem | 2 | Rp 40,000 | Rp 80,000 |
| 11 | XL6009 DC-DC Step Up | Step-up converter | 1 | Rp 60,000 | Rp 60,000 |
| 12 | Terminal Block | Penghubung komponen | 50 | Rp 2,000 | Rp 100,000 |
| 13 | Kabel Serabut AWG 28 | Penghubung sistem | 50m | Rp 3,000/m | Rp 150,000 |
| 14 | PCB DOT Matrix | Tempat solder komponen | 3 | Rp 33,333 | Rp 100,000 |
| 15 | Pin Header Female 1x40 | Socket core | 1 | Rp 60,000 | Rp 60,000 |
| 16 | Hannochs Driver Adaptor DC 12V | Sumber listrik | 1 | Rp 200,000 | Rp 200,000 |
| 17 | Box Panel | Wadah sistem | 1 | Rp 3,500,000 | Rp 3,500,000 |
| **Subtotal Core** | | | | | **Rp 4,470,000** |

#### 3. Platform & Connectivity
| No | Komponen | Spesifikasi | Qty | Harga Satuan | Total |
|----|----------|-------------|-----|--------------|-------|
| 18 | Antares Platform | IoT platform (1 tahun) | 1 | Rp 1,000,000 | Rp 1,000,000 |
| 19 | Rangka Besi | Tempat semua komponen | 1 | Rp 5,000,000 | Rp 5,000,000 |
| 20 | HKM M23 PRO | Koneksi internet (Optional) | 1 | Rp 900,000 | Rp 900,000 |
| **Subtotal Platform** | | | | | **Rp 6,900,000** |

#### 4. Power System (Optional)
| No | Komponen | Spesifikasi | Qty | Harga Satuan | Total |
|----|----------|-------------|-----|--------------|-------|
| 21 | Solar Panel System | Alternatif sumber listrik | 1 | Rp 8,000,000 | Rp 8,000,000 |
| 22 | Battery Backup 12V 100Ah | Backup power | 2 | Rp 2,500,000 | Rp 5,000,000 |
| 23 | Solar Charge Controller | MPPT 60A | 1 | Rp 1,500,000 | Rp 1,500,000 |
| 24 | Inverter 1000W | DC to AC converter | 1 | Rp 1,200,000 | Rp 1,200,000 |
| **Subtotal Power** | | | | | **Rp 15,700,000** |

### B. BIAYA PENGEMBANGAN & IMPLEMENTASI

#### 5. Software Development
| No | Item | Deskripsi | Qty | Harga | Total |
|----|------|-----------|-----|--------|-------|
| 25 | Embedded Firmware Development | Multi-controller orchestration, sensor fusion, real-time processing | 1 | Rp 15,000,000 | Rp 15,000,000 |
| 26 | IoT Communication Layer | Antares integration, network resilience, data buffering | 1 | Rp 8,000,000 | Rp 8,000,000 |
| 27 | Data Analytics Engine | Real-time analysis, trend detection, anomaly identification | 1 | Rp 12,000,000 | Rp 12,000,000 |
| 28 | Web Dashboard & Visualization | Interactive charts, real-time updates, responsive design | 1 | Rp 10,000,000 | Rp 10,000,000 |
| 29 | Mobile Application (PWA) | Cross-platform app, offline capability, push notifications | 1 | Rp 15,000,000 | Rp 15,000,000 |
| 30 | API & Backend Services | Data processing, user management, integration endpoints | 1 | Rp 8,000,000 | Rp 8,000,000 |
| 31 | Calibration & Maintenance Tools | Sensor calibration interfaces, diagnostic tools | 1 | Rp 7,000,000 | Rp 7,000,000 |
| 32 | Testing & Quality Assurance | Comprehensive testing, load testing, integration testing | 1 | Rp 10,000,000 | Rp 10,000,000 |
| **Subtotal Software** | | | | | **Rp 85,000,000** |

#### 6. Installation & Testing
| No | Item | Deskripsi | Qty | Harga | Total |
|----|------|-----------|-----|--------|-------|
| 29 | Assembly & Testing | Hardware integration | 1 | Rp 2,000,000 | Rp 2,000,000 |
| 30 | Calibration | Sensor calibration | 1 | Rp 1,500,000 | Rp 1,500,000 |
| 31 | Installation | On-site installation | 1 | Rp 2,500,000 | Rp 2,500,000 |
| 32 | Documentation | Manual & training | 1 | Rp 1,000,000 | Rp 1,000,000 |
| **Subtotal Installation** | | | | | **Rp 7,000,000** |

### C. BIAYA OPERASIONAL TAHUNAN

#### 7. Maintenance & Support
| No | Item | Deskripsi | Frequency | Harga/kali | Total/tahun |
|----|------|-----------|-----------|------------|-------------|
| 33 | Kalibrasi Sensor | Maintenance rutin | 4x/tahun | Rp 1,000,000 | Rp 4,000,000 |
| 34 | Technical Support | Remote support | 12 bulan | Rp 500,000 | Rp 6,000,000 |
| 35 | Platform Subscription | Antares renewal | 1x/tahun | Rp 1,000,000 | Rp 1,000,000 |
| 36 | Internet Connection | Data connectivity | 12 bulan | Rp 300,000 | Rp 3,600,000 |
| **Subtotal Maintenance** | | | | | **Rp 14,600,000** |

---

## RINGKASAN BIAYA

| Kategori | Subtotal | Keterangan |
|----------|----------|------------|
| **Komponen Hardware** | **Rp 14,670,000** | Sensor + Core + Platform |
| **Power System** | **Rp 15,700,000** | Optional (solar system) |
| **Software Development** | **Rp 85,000,000** | Complex IoT system development |
| **Installation & Testing** | **Rp 7,000,000** | Implementation |
| **TOTAL INVESTASI AWAL** | **Rp 122,370,000** | Dengan solar system |
| **TOTAL TANPA SOLAR** | **Rp 106,670,000** | Menggunakan PLN |
| | | |
| **Biaya Operasional/Tahun** | **Rp 14,600,000** | Maintenance & support |

### CATATAN PENTING:
1. Harga dapat berubah sesuai kondisi pasar
2. Solar system bersifat optional, bisa menggunakan PLN
3. Biaya maintenance mencakup kalibrasi 4x/tahun sesuai permintaan
4. PWA/Mobile app development sudah termasuk
5. Untuk multiple locations, ada economies of scale untuk software development

### REKOMENDASI PHASING:
- **Phase 1**: Implementasi basic system tanpa solar (Rp 106,670,000)
- **Phase 2**: Upgrade ke solar system jika diperlukan (+ Rp 15,700,000)
- **Phase 3**: Replikasi ke lokasi lain dengan biaya hardware saja
