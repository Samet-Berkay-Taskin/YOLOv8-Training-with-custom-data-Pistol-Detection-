# Pistol-Detection-Train-YoloV8
Bu proje, YOLOv8 kullanarak tabanca tespiti yapabilen bir model oluşturmayı içerir. Kendi veri setimizle eğiteceğimiz bu model ile tespitler gerçekleştirebilirsiniz.


## Veri Seti Oluşturma
Resimleri MakeSense kullanarak etiketledim ve veri setini oluşturduktan sonra, eğitim (train) ve doğrulama (validation) olarak ikiye böldüm. Detaylı bilgi için [MakeSense'ye gitmek için buraya tıklayın](https://www.makesense.ai/).

# Yolov8 kullanarak kendi verisetimizle eğitebileceğimiz tabanca tespiti yapabilen model oluşturma.
- Yolov8'de kendi verisetimiz ile eğitebilir ve tespitlerde kendi eğittiğiniz modeli kullanabilirsiniz.
- Aynı verisetiyle önceden eğitilmiş model ile tespitleri yapabilirsiniz.

## Eğitim kısmı
1. **Veri Setini Hazırlayın:**
   - Pistol_Datasets dosyasını zipleyin.
   - YOLOv8_tabanca_tespiti.ipynb, customized.yaml ve Pistol_Datasets.zip dosyalarını Google Drive'ınıza yükleyin.
 
2. **Kodları Çalıştırın:**
   - Google Drive'da YOLOv8_tabanca_tespiti.ipynb dosyasını açın ve aşağıdaki fotoğraftaki kodları sırayla çalıştırın.
   - ![](User_guide/a.png)

3. **YAML Dosyasını Yükleyin:**
   - YAML dosyasını (ultralytics>ultralytics>yolo>data>datasets) yoluna bu repositoryden indirerek atın.
   - ![](User_guide/b.png)
     
4. **Google Drive'ı Bağlayın ve Verileri Yükleyin:**
   - Drive'ı bağlama ve veri yükleme kodlarını çalıştırın.
  
5. **Modeli Eğitin:**
- Eğitim sürecini başlatın ve istediğiniz epoch değerini belirleyin (önerilen: 40 veya 50 epoch).Bu kısım biraz uzun sürecektir bilginiz olsun. Eğitim tamamlandıktan sonra model,DOSYALAR'da runs/detect/train/weights/best.pt yoluna kaydedilecektir (best.pt) modelimizdir.
     
6. **Test Verilerini Yükleyin:**
 - Bu repositoryden indirdiğiniz test dosyasına ek video ve fotoğraf ekleyebilir veya mevcut verileri kullanabilirsiniz.Test dosyasındaki tüm fotoğraf ve videoları tutup dosyalar kısmındaki boşluğa atın ve tamamiyle yüklenmesini bekleyin.
 - ![](User_guide/c.png)

7. **Dosyaları Düzenleyin:**
   - Fotoğraflar ve videolar yüklendikten sonra dosyalar kısmında boşluğa gelip sağ tıkla yeni klasör oluşturun ve yüklenen fotoğraf ve videoları bu klasöre atın.
   - ![](User_guide/d.png)
     
8. **Modeli Kullanarak Tespit Yapın:**
   - Yukarıdaki kırmızı alana /content/oluşturduğunuz_klasör_adı ve lacivert alana /runs/detect/train/weights/best.pt yazın ardından kodu çalıştırın.Kod çalışması bittikten sonra veriler runs/detect/predict kısmına kayıt olur.
   - runs/detect/predict kısmına girip istediğiniz videoya veya fotoğrafa gelip sağ tıklayın ve yolunu kopyalayın.Aşağıdaki resimde gördüğünüz üzere kopyaladığınız yolu yapıştırın ve kodu çalıştırın.(Eğer video ise her video kodunu çalıştırdığınızda bir sonraki videoyu görmek için dosyalar kısmındaki "result_compressed.mp4"ü silin ve video kodunu çalıştırın.)
   - ![](User_guide/e.png) 

##### Hepsi bu kadar


### Verisetiyle önceden eğitilmiş model ile tespit
1. YOLOv8_tabanca_tespiti.ipynb Google Drive'nize yükleyin ve YOLOv8_tabanca_tespiti.ipynb'i açın.Eğitim kısmındaki (yukarıda) 2. kısımdaki fotoğrafta gösterilen kodları çalıştırın.
2. Bu repositoryden indirdiğiniz best.pt vtest dosyasındaki tüm fotoğraf ve videoları tutup dosyalar kısmındaki boşluğa atın ve tamamiyle yüklenmesini bekleyin.(indirilen test dosyasına isterseniz ek video ve fotoğraf ekleyip veya direkt sadece bu verileri kullanarak tespiti yapabilirsiniz)

![](User_guide/c.png)

2. Eğitim kısmındaki (yukarıda) 7. kısmı ve 8. kısımdaki sadece kırmızı ile seçilen yeri değiştirin lacivert kalsın ve kodu çalıştırın.
3. Eğitim kısmındaki (yukarıda) 8. kısmı yapın ve bu kadar.Eğitim yapmadan, eğitilmiş model ile tespitleri gerçekleştirebildiniz.
