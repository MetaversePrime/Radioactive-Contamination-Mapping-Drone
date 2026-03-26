# Radioactive-Contamination-Mapping-Drone
İHA tabanlı, radyoaktif kontaminasyon bölgelerinin otonom tespiti ve çok modlu (Gama, Beta, Nötron) haritalanması için açık kaynak Ar-Ge projesi. Mithras Imaging &amp; Smart Aerospace.

# 🚁 İHA Tabanlı Çok Modlu Radyasyon Tespit ve Haritalama Sistemi 
*(UAV-Based Multi-Modal Radiation Detection and Mapping System)*

Bu depo, radyoaktif kontaminasyon bölgelerinde insan maruziyetini sıfıra indirmeyi hedefleyen, İHA (Drone) tabanlı otonom bir radyasyon tespit, hava örnekleme ve CBS (Coğrafi Bilgi Sistemleri) tabanlı haritalama sisteminin Ar-Ge dokümanlarını, mimari tasarımlarını ve teknik altyapısını içermektedir.

Mithras Imaging Ltd. ve Smart Aerospace Solutions A.Ş. ortaklığında geliştirilen bu proje, nükleer güvenlik, çevresel izleme ve KBRN (Kimyasal, Biyolojik, Radyolojik, Nükleer) savunma ihtiyaçları için tasarlanmıştır.

## 💡 Neden Açık Kaynak?
Bu proje, kapsamlı bir Ar-Ge sistematiği ile ulusal bir fon programı (TÜBİTAK 1507) için hazırlanmıştır. Projenin destek kapsamına alınmamasına rağmen, sunduğu kritik KBRN savunma teknolojisinin raflarda tozlanamayacak kadar hayati olduğuna inanıyoruz. Teknolojinin kapalı kapılar ardında kalması yerine, açık kaynak ekosistemine katkı sağlamak, şeffaf bir mühendislik vizyonu sunmak ve bu alanda çalışan kurumlar/araştırmacılar ile işbirliği yapmak amacıyla projemizin temel mimarisini toplulukla paylaşıyoruz.

## 🚀 Sistemin Temel Yenilikleri ve Özellikleri

Mevcut tek modlu veya insan gücüne dayalı sistemlerin aksine, bu proje aşağıdaki çok disiplinli mühendislik çözümlerini sunar:

* **Çok Modlu Radyasyon Algılama:** Tek bir uçuşta Gama, Beta, X-Işını, Alfa ve Nötron (Bubble dedektör ile) eşzamanlı tespiti.
* **İleri FPGA Sinyal İşleme (Readout Elektroniği):** 144 kanallı SiPM (Silisyum Fotoçoğaltıcı) dizisi. Yüksek radyasyon altında sinyal üst üste binmesini (pile-up) engellemek için FPGA üzerinde gerçek zamanlı *Pulse Shape Analysis (PSA)* ve pikosaniye hassasiyetinde *TDC* mimarisi.
* **Çift Noktalı Stabilize Vinç (Makara) Mekanizması:** Sensörlerin kontamine bölgeye güvenle indirilmesi için salınımı ($<\pm15^{\circ}$) ve kendi ekseninde dönmeyi ($<\pm10^{\circ}$) engelleyen, drone stabilitesini koruyan özgün mekanik tasarım.
* **Atmosferik Partikül Örnekleme:** Havada asılı radyoaktif partiküllerin ve gazların analizi için entegre HEPA filtreli hava örnekleme modülü.
* **Çevrimdışı (Off-line) Yüksek Güvenlikli Haritalama:** Veriler uçuş sırasında GNSS logları ile zaman damgalı olarak cihaza kaydedilir, siber müdahaleye kapalıdır. Uçuş sonrası CBS (GIS) entegrasyonu ile yüksek çözünürlüklü ısı haritaları oluşturulur.

## 🛠️ Sistem Mimarisi

* **Algılama Teknolojisi:** NaI(Tl), CsI(Tl) ve Plastik Sintilatörler + SiPM Array + Nötron Dedektörü + LR-115. *(Bkz: `Hardware/Electronics`)*
* **Mekanik Platform:** 5 kg faydalı yük kapasiteli, minimum 30 dakika uçuş süresine sahip, karbonfiber kompozit döner kanatlı İHA platformu. *(Bkz: `Hardware/Mechanics`)*
* **Veri Kaydı:** Sensör ve uçuş kontrolcüsü arasında elektromanyetik paraziti önlemek amaçlı izole edilmiş, bağımsız enerji yönetimli veri toplama ünitesi (DAQ).

## 📊 Testler ve Doğrulama
Proje kapsamında, sensörlerin laboratuvar ortamında Co-57, Ba-133, Cs-137, Co-60 ve Na-22 gibi referans nokta kaynaklarla yapılan spektrogram analizleri ve SiPM kalibrasyon verilerine `Data_and_Tests` klasöründen ulaşabilirsiniz. *(Not: İlgili laboratuvar sonuçları periyodik olarak depoya eklenecektir.)*

## 🤝 İşbirliği ve İletişim (Call to Action)
Bu teknoloji, nükleer tesis güvenliği, acil durum yönetimi (AFAD, KBRN birimleri) ve çevresel izleme için kullanıma hazırdır. 

Bu alanda çalışan, yatırım yapmak isteyen, teknik donanım/yazılım kısımlarına katkı sunmak isteyen veya sistemin saha testleri için entegrasyon partneri olmak isteyen kişi ve kurumlarla görüşmekten memnuniyet duyarız.

📧 **İletişim:**
* **Radyasyon Algılama ve Elektronik:** Mehmet İrfan Gedik (Mithras Imaging Ltd.) - info@mithras-imaging.com
* **İHA Platformu ve Mekanik Entegrasyon:** Fatih Baykal (Smart Aerospace Solutions A.Ş.) - fatih.baykal@ostimteknik.edu.tr

## 📄 Lisans
Bu depoda paylaşılan teknik dokümanlar, mekanik tasarımlar ve donanım mimarileri **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** lisansı ile korunmaktadır. Projeyi inceleyebilir ve üzerine geliştirmeler yapabilirsiniz; ancak önceden yazılı izin alınmaksızın **ticari bir ürüne dönüştürülemez.**

*Sistemde kullanılan patentli sensör kuplaj mimarisi (TR Patent No: 2022/001086), buluş sahibinin yasal koruması altındadır.*
