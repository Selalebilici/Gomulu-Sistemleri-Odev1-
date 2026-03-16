Gomulu-Sistemleri-Odev1
Bu depo, Gömülü Sistemler dersleri kapsamında kapsamlı olarak ilk verilen çalışmayı içermektedir. Proje, STM32F103 (Blue Pill) geliştirme kartı üzerinde temel giriş/çıkış işlemleri ve hata ayıklama (debug) tekniklerinin aralıklarını kapsar.

📋 Proje Özeti
Proje kapsamında STM32F103C8T6 mikrodenetleyicisi üzerinde yer alan kullanıcı LED'i (PC13), 500ms yanık ve 500ms sönük kalacak şekilde (1 saniye periyotla) programlanmıştır. Çalışma; donanım özellikleri, kod geliştirme, sürüm ve donanım üzerindeki hata ayrıntılarının ayrıntılarından oluşur.

🛠️ Kullanılan Teknolojiler ve Araçlar
Donanım: STM32F103C8T6 (Blue Pill), ST-Link V2 Hata Ayıklayıcı.

Geliştirme Ortamı: Visual Studio Code (VS Code).

Derleyici: GNU Arm Embedded Toolchain (arm-none-eabi-gcc).

Yapılandırma: STM32CubeMX (Makefile tabanlı proje yönetimi).

Hata Ayıklayıcı: OpenOCD & Cortex-Debug.

📁 Proje Yapısı
Core/Src/main.c: HAL kütüphanesi aracılığıyla LED Toggle ve Gecikme komutlarının yazıldığı ana uygulama dosyası.

Drivers/: Mikrodenetleyiciye özgü donanım soyutlama katmanı (HAL) kütüphaneleri.

Makefile: Projenin sürümleri ve dosya bağımlılıklarını yönetilen yapı.

.vscode/launch.json: VS Code üzerinde canlı hata ayıklama (Step-by-step Debug) için okunan hata ayıklayıcı ayarları.

💻Uygulama ve Deney Süreci
Pin Yapılandırması: CubeMX üzerinden PC13 pini GPIO_Output olarak atanmış ve sistem saati (Clock) öğretilmiştir.

Derleme (Build): Terminal üzerinden make komut çalıştırılarak build/ dizini altında .elf ve .bin dosyaları oluşturuldu.

Yükleme (Flash): OpenOCD aracı aracılığıyla firmware ST-Link üzerinden MCU flash belleğine kaydedilir.

Hata Ayıklama (Debug): Kodun kritik satırlarına Breakpoint eklenerek program dağılımı durdurulmuş, işlemci kayıtçıları ve pin durumu canlı olarak gözlemlenmiştir.

🎥 Uygulama Videoları
Projenin çalışma sistemleri ve hata ayıklama aşamalarını içeren YouTube videosuna aşağıdaki bağlantıdan ulaşabilirsiniz: 
https://youtu.be/zp7KmKA8OkU
