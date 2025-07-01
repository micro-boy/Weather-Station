# Sistem Weather Station IoT
### Sistem Monitoring Cuaca Otomatis dengan Platform IoT Terintegrasi

![Weather Station](https://img.shields.io/badge/Status-In%20Development-yellow) ![IoT](https://img.shields.io/badge/IoT-Antares%20Platform-blue) ![Hardware](https://img.shields.io/badge/Hardware-ESP32%20%2B%20Arduino-green)

## 📋 Deskripsi Proyek


![Weather Sensor drawio](https://github.com/user-attachments/assets/7ff6aedd-2f7f-4b03-bce3-bd9dc619bef2)

> **⚠️ CATATAN PENTING**: Spesifikasi teknis dan harga hardware yang tercantum dalam dokumentasi ini dapat berubah sewaktu-waktu tergantung ketersediaan komponen di pasaran Indonesia. Fluktuasi harga dan availability stock komponen elektronik, terutama sensor dan microcontroller, sangat dipengaruhi oleh kondisi supply chain global. Disarankan untuk melakukan survey harga terkini dan konfirmasi availability sebelum procurement.

Proyek ini mengembangkan sistem monitoring cuaca otomatis yang komprehensif, dirancang khusus untuk deployment di lokasi remote dengan kebutuhan data meteorologi yang akurat dan real-time. Sistem ini mengintegrasikan multiple sensor lingkungan dengan platform IoT untuk memberikan solusi monitoring cuaca yang robust dan scalable.

Weather station ini tidak hanya mengumpulkan data cuaca, tetapi juga melakukan real-time analytics, predictive analysis, dan menyediakan interface yang user-friendly untuk monitoring dan pengambilan keputusan. Sistem dirancang dengan arsitektur distributed embedded system yang memungkinkan reliability tinggi dan maintenance yang mudah.

## 🎯 Tujuan dan Manfaat

Sistem ini dikembangkan untuk memenuhi kebutuhan spesifik monitoring cuaca di lokasi operasional yang memerlukan data meteorologi akurat untuk optimasi proses bisnis. Beberapa manfaat utama yang diharapkan meliputi:

- Meningkatkan akurasi dalam prediksi cuaca untuk perencanaan operasional
- Mengurangi downtime akibat cuaca ekstrem melalui early warning system
- Menyediakan data historis cuaca untuk analisis dan pelaporan
- Memberikan dasar pengambilan keputusan berdasarkan data cuaca real-time
- Meningkatkan protokol keselamatan berdasarkan kondisi cuaca aktual
- Mengoptimalkan alokasi sumber daya berdasarkan pola cuaca yang terprediksi

## 🏗️ Arsitektur Sistem

### Gambaran Umum Arsitektur

Sistem menggunakan arsitektur three-tier yang terdiri dari sensor layer, processing layer, dan communication layer. Sensor layer menggunakan multiple sensor khusus untuk mengukur berbagai parameter meteorologi. Processing layer menggunakan arsitektur distributed microcontroller dengan ESP32 sebagai master controller dan dual Arduino Nano sebagai slave controller. Communication layer mengelola transmisi data ke cloud platform dan user interface.

Desain arsitektur ini dipilih untuk memberikan redundancy dan reliability tinggi. Jika salah satu komponen mengalami gangguan, sistem masih dapat beroperasi dengan degraded performance daripada complete failure. Hal ini sangat penting untuk aplikasi mission-critical seperti monitoring cuaca.

### Komponen Hardware Utama

**Cluster Sensor:**
- **BME680**: Sensor komprehensif untuk temperature, humidity, barometric pressure, dan gas resistance
- **Anemometer**: Sensor kecepatan angin dengan akurasi tinggi
- **Wind Direction Sensor**: Sensor arah angin dengan resolusi 16 arah
- **Ombrometer**: Sensor curah hujan dengan precision measurement
- **Ambient Light Sensor**: Monitoring intensitas cahaya lingkungan
- **UV Sensor**: Pengukuran radiasi ultraviolet
- **PM2.5 Sensor (Optional)**: Monitor kualitas udara untuk assessment atmosfer lengkap

**Processing Core:**
- **ESP32 WEMOS D1 MINI**: Master controller dengan built-in WiFi untuk konektivitas IoT
- **Arduino Nano V3 (2 unit)**: Slave controller untuk mengelola input sensor dan mengurangi beban processing
- **Logic Level Converter**: Memastikan komunikasi proper antara sistem dengan voltage level berbeda
- **XL6009 DC-DC Step Up**: Power regulation dan voltage conversion

**Power Management:**
- **Hannochs Driver Adaptor DC 12V**: Power supply stabil dari AC mains
- **Solar Power System (Optional)**: Untuk deployment off-grid scenarios

## 📊 Spesifikasi Teknis

> **📝 DISCLAIMER TEKNIS**: Spesifikasi dan model komponen yang tercantum merupakan referensi berdasarkan ketersediaan pada saat penyusunan dokumentasi. Implementasi aktual dapat menggunakan komponen equivalent atau generasi terbaru dengan spesifikasi yang setara atau lebih baik, tergantung availability di distributor lokal dan pertimbangan cost-effectiveness.

### Sensor Specifications dan Communication Protocol

**BME680 (I2C Protocol):**
- Temperature accuracy: ±1°C
- Humidity accuracy: ±3% RH  
- Pressure accuracy: ±1 hPa
- Gas resistance measurement untuk air quality indication

**Anemometer (Interrupt-based):**
- Wind speed measurement dengan pulse counting
- Resolution: 0.1 m/s
- Range: 0-60 m/s

**Wind Direction Sensor (UART):**
- 16-direction resolution
- Accuracy: ±5°
- Output: Digital compass bearing

**Ombrometer (Interrupt Pin):**
- Rainfall detection dengan tipping bucket mechanism
- Resolution: 0.2mm per tip
- Measurement range: 0-999mm/hour

**Ambient Light Sensor (I2C):**
- Measurement range: 0.01 lux sampai 83,000 lux
- Dynamic range: 20-bit resolution

**UV Sensor (I2C):**
- UV index measurement: 0-15
- Accuracy: ±1 UV index unit

**PM2.5 Sensor (I2C, Optional):**
- Laser scattering principle
- Range: 0-1000 μg/m³
- Particle size: 0.3-10 μm

### Processing dan Communication Capabilities

**ESP32 Master Controller:**
- Processor: Dual-core 240MHz
- Memory: 520KB SRAM, 4MB Flash
- Connectivity: WiFi 802.11 b/g/n
- Communication: UART, I2C, SPI
- Operating voltage: 3.3V

**Arduino Nano Slave Controllers:**
- Processor: ATmega328P 16MHz
- Memory: 32KB Flash, 2KB SRAM
- Communication: UART to ESP32
- Operating voltage: 5V

**Inter-Controller Communication:**
- Protocol: UART dengan error detection
- Baud rate: 115200 bps
- Data format: JSON structured messages

**Cloud Integration:**
- Platform: Antares IoT Indonesia
- Protocol: HTTPS POST requests
- Data format: JSON payload
- Features: Data buffering, automatic retry mechanism

## 💰 Rencana Anggaran Biaya (RAB)

> **💵 DISCLAIMER HARGA**: Harga yang tercantum dalam RAB ini bersifat estimasi berdasarkan survey pasar pada periode penyusunan (Juli 2025) dan dapat berubah sewaktu-waktu. Faktor-faktor yang mempengaruhi fluktuasi harga meliputi:
> - **Kondisi Supply Chain Global**: Gangguan rantai pasok komponen elektronik
> - **Nilai Tukar Rupiah**: Sebagian besar komponen merupakan import
> - **Ketersediaan Stock**: Limited availability dapat meningkatkan harga drastis
> - **Seasonality**: Periode tertentu (Chinese New Year, pandemic) mempengaruhi supply
> - **Technology Updates**: Rilisnya generasi baru dapat mempengaruhi harga generasi sebelumnya
> 
> **REKOMENDASI**: Lakukan survey harga aktual dan request quotation dari multiple supplier sebelum final procurement. Buffer 15-25% dari total estimasi untuk mengantisipasi fluktuasi harga.

### Breakdown Biaya Hardware

**Komponen Sensor (Rp 3.300.000):**
Investasi terbesar pada cluster sensor yang menyediakan complete weather monitoring capabilities. BME680 sebagai flagship sensor environmental memberikan multiple parameter measurement dalam single package yang cost-effective. Sensor monitoring angin (anemometer dan wind direction) menyediakan data critical untuk analisis cuaca. PM2.5 sensor optional menambahkan capabilities monitoring kualitas udara yang valuable untuk deployment urban.

**Komponen Core System (Rp 4.470.000):**
Kombinasi ESP32 dan Arduino Nano memberikan arsitektur distributed processing yang robust dan scalable. Logic level converter dan komponen power management memastikan operasi reliable dalam berbagai kondisi lingkungan. Box panel berkualitas tinggi (Rp 3.500.000) memberikan proteksi weatherproof yang essential untuk deployment outdoor.

> **🔄 ALTERNATIF KOMPONEN**: Jika komponen spesifik tidak tersedia, dapat dilakukan substitusi dengan komponen equivalent:
> - ESP32 WEMOS D1 MINI → ESP32 DevKit, NodeMCU ESP32, atau variant ESP32 lainnya
> - Arduino Nano V3 → Arduino Nano Every, Arduino Pro Mini, atau compatible clone
> - BME680 → BME280 + gas sensor terpisah (dengan adjustment firmware)
> - Logic Level Converter → Voltage divider circuit atau bidirectional level shifter
> 
> Substitusi komponen memerlukan review dan possibly firmware modification untuk memastikan compatibility.

**Platform dan Konektivitas (Rp 6.900.000):**
Subscription Antares IoT platform menyediakan cloud-based data storage, API services, dan dashboard capabilities. Framework besi robust memastikan mounting stabil untuk semua komponen sistem. Modul konektivitas internet optional memberikan fleksibilitas untuk deployment di lokasi tanpa infrastructure network existing.

### Investasi Software Development

**Complex IoT System Development (Rp 85.000.000):**
Investasi ini mencakup comprehensive software development meliputi:
- Embedded firmware development untuk multi-controller orchestration
- IoT communication layer dengan network resilience capabilities  
- Real-time data analytics engine
- Interactive web dashboard
- Cross-platform mobile application
- Complete API backend services
- Calibration dan maintenance tools
- Comprehensive testing dan quality assurance

Software development cost yang signifikan ini justified oleh kompleksitas distributed embedded system yang harus mengelola multiple sensor, perform real-time data processing, handle network communication, dan provide user-friendly interface. Investasi ini merupakan one-time cost yang akan memberikan long-term value melalui operasi reliable dan scalability mudah.

### Total Investment Analysis

**Complete System Investment:**
- Total dengan solar system: Rp 122.370.000
- Total tanpa solar system: Rp 106.670.000
- Biaya operasional per tahun: Rp 14.600.000

**Cost per Year Analysis:**
Jika dihitung over 10-year system lifetime, annual cost menjadi approximately Rp 10.667.000 per tahun untuk complete system tanpa solar. Ini competitive dibandingkan commercial weather station solution yang typically cost $15,000-50,000 USD dengan limited customization capabilities.

### Strategi Procurement dan Risk Mitigation

**Recommended Procurement Approach:**
- **Phase Procurement**: Beli komponen dalam fase untuk mengurangi risk obsolescence
- **Multiple Supplier**: Maintain relationship dengan 2-3 supplier berbeda
- **Local vs Import**: Prioritas komponen yang tersedia dari distributor lokal untuk faster delivery
- **Buffer Stock**: Procure 10-15% extra untuk komponen critical (sensor, microcontroller)

**Cost Control Strategy:**
- Monitor harga secara berkala menggunakan price tracking tool
- Negotiate volume discount untuk multiple unit deployment
- Consider refurbished atau previous generation component untuk non-critical function
- Build relationship dengan supplier untuk priority access saat stock limited

## 🛠️ Instalasi dan Setup

### Persiapan Hardware Assembly

Hardware assembly dimulai dengan preparation main enclosure (box panel) dan installation mounting framework. Positioning sensor harus memperhatikan requirement untuk measurement akurat:
- Anemometer dan wind direction sensor memerlukan unobstructed airflow
- Rain gauge harus level dan stable
- Temperature/humidity sensor harus protected dari direct sunlight dengan adequate ventilation

Power system installation mencakup connection DC power adapter, optional solar panel system setup, dan battery backup configuration. Proper grounding sangat important untuk protection terhadap lightning dan electromagnetic interference. Cable management harus weatherproof dan organized untuk easy maintenance access.

### Software Configuration dan Programming

> **⚙️ ADAPTASI FIRMWARE**: Jika terjadi substitusi komponen hardware, firmware perlu disesuaikan untuk memastikan compatibility. Modification yang mungkin diperlukan meliputi:
> - Pin mapping adjustment untuk different microcontroller board
> - Library update untuk sensor variant yang berbeda
> - Communication protocol adjustment
> - Calibration parameter modification
> 
> Disarankan untuk melakukan testing comprehensive setelah component substitution.

Firmware programming dimulai dengan setup development environment menggunakan Arduino IDE atau PlatformIO. Programming ESP32 master controller mencakup:
- WiFi configuration untuk network connectivity
- Antares platform integration
- Sensor data collection routine
- Inter-controller communication protocol

Programming Arduino Nano slave controller fokus pada:
- Specific sensor interfacing
- Data preprocessing dan filtering
- Communication dengan master controller

Configuration parameter harus disesuaikan dengan deployment environment termasuk network credential, sensor calibration value, data transmission interval, dan alert threshold.

### Deployment dan Commissioning

Site preparation mencakup assessment mounting location, power availability, network connectivity, dan environmental factor. Installation framework dan enclosure harus memperhatikan local building code dan safety regulation.

Initial system commissioning meliputi:
- Sensor calibration dengan reference standard
- Communication testing antara semua komponen
- Data validation dan accuracy verification
- Network connectivity testing
- Alert system testing

Performance validation harus dilakukan over several days untuk memastikan system stability dan data accuracy. Comparison dengan reference weather data dapat digunakan untuk validate sensor reading dan identify potential calibration issue.

## 📱 Penggunaan dan Monitoring

### Dashboard Interface dan Data Visualization

Web dashboard menyediakan real-time visualization dari all sensor reading dengan interactive chart dan graph. User dapat view current condition, historical trend, dan customizable time-range analysis. Dashboard dirancang responsive untuk access dari desktop, tablet, dan mobile device dengan consistent user experience.

Advanced feature mencakup:
- Configurable alert untuk threshold violation
- Data export capability untuk analysis
- Integration dengan external system melalui API endpoint
- System health monitoring untuk early detection hardware issue
- Maintenance requirement notification

### Mobile Application Feature

Mobile PWA (Progressive Web App) memberikan full dashboard functionality dengan additional feature:
- Push notification untuk weather alert
- Offline data viewing capability
- Location-based service
- Real-time alert untuk significant weather event
- Personalized alert criteria configuration

Application dirancang untuk work seamlessly across different mobile platform tanpa requiring separate native app.

### Data Analysis dan Reporting

Sistem menyediakan comprehensive data analytics capability termasuk:
- Trend analysis untuk pattern identification
- Correlation study antara different parameter
- Predictive modeling untuk weather forecasting
- Historical data analysis untuk seasonal variation identification
- Long-term climate trend analysis

Automated reporting feature dapat generate daily, weekly, atau monthly weather summary dengan customizable format. Data export capability mendukung integration dengan external analysis tool atau database system untuk advanced analytics application.

## 🔧 Maintenance dan Kalibrasi

### Routine Maintenance Schedule

**Quarterly Maintenance:**
- Sensor cleaning untuk maintain accuracy
- Calibration verification
- System performance assessment
- Electrical connection inspection
- Weather protection integrity check

**Annual Comprehensive Maintenance:**
- Complete system calibration dengan certified reference
- Firmware update dan security patch
- Hardware component replacement jika necessary
- Performance optimization
- Documentation update

### Calibration Procedure dan Quality Assurance

Sensor calibration menggunakan reference standard atau comparison dengan certified weather instrument:

**BME680 Calibration:**
- Temperature reference menggunakan precision thermometer
- Humidity calibration menggunakan saturated salt solution
- Pressure calibration menggunakan barometric reference

**Wind Sensor Calibration:**
- Controlled airflow testing
- Comparison dengan certified anemometer
- Wind tunnel validation jika available

**Rain Gauge Calibration:**
- Volume measurement verification
- Tipping mechanism accuracy testing
- Flow rate calibration

Documentation calibration result sangat important untuk maintaining data quality record dan identifying sensor drift over time. Calibration certificate harus maintained untuk regulatory compliance atau quality assurance requirement.

Documentation calibration result sangat important untuk maintaining data quality record dan identifying sensor drift over time. Calibration certificate harus maintained untuk regulatory compliance atau quality assurance requirement.

---

**Status Proyek**: Dalam tahap development dan testing. Deployment pertama direncanakan untuk Q3 2025 di lokasi Samarinda.
