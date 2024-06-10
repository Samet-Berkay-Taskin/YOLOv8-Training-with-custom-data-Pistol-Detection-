# Pistol-Detection-Train-YoloV8

 Bu proje, YOLOv8 kullanarak tabanca tespiti yapabilen bir model oluşturmayı içerir. Kendi veri setimizle eğiteceğimiz bu model ile tespitler gerçekleştirebilirsiniz.
 
 ## Veri Seti Oluşturma
Resimleri MakeSense kullanarak etiketledim ve veri setini oluşturduktan sonra, eğitim (train) ve doğrulama (validation) olarak ikiye böldüm. Detaylı bilgi için [MakeSense'ye gitmek için buraya tıklayın](https://www.makesense.ai/).

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
   - Eğitim sürecini başlatın ve istediğiniz epoch değerini belirleyin (önerilen: 40 veya 50 epoch). Eğitim tamamlandıktan sonra model, runs/detect/train/weights/best.pt yoluna kaydedilecektir.

6. **Test Verilerini Yükleyin:**
   - Bu repositoryden indirdiğiniz test dosyasına ek video ve fotoğraf ekleyebilir veya mevcut verileri kullanabilirsiniz.
   - ![](User_guide/c.png)

7. **Dosyaları Düzenleyin:**
   - Yüklenen fotoğraf ve videoları yeni bir klasöre taşıyın.
   - ![](User_guide/d.png)

8. **Modeli Kullanarak Tespit Yapın:**
   - Aşağıdaki adımları takip ederek tespitleri gerçekleştirin:
     - /content/oluşturduğunuz_klasör_adı ve /runs/detect/train/weights/best.pt yollarını belirleyin.
     - Kodu çalıştırdıktan sonra veriler runs/detect/predict dizinine kaydedilir.

9. **Sonuçları Görüntüleyin:**
   - runs/detect/predict dizininde yer alan videoları veya fotoğrafları sağ tıklayarak yolunu kopyalayın ve kodu çalıştırın.
   - ![](User_guide/e.png)
   - Eğer video ise, her seferinde "result_compressed.mp4" dosyasını silerek yeni videoyu görüntüleyin.

##### Hepsi bu kadar

### Önceden Eğitilmiş Model ile Tespit

1. **Notebook'u Yükleyin:**
   - YOLOv8_tabanca_tespiti.ipynb dosyasını Google Drive'ınıza yükleyin ve açın. Eğitim kısmındaki (yukarıda) 3. adımdaki kodları çalıştırın.

2. **Veri ve Model Dosyalarını Yükleyin:**
   - Bu repositoryden indirdiğiniz best.pt dosyasını ve test dosyasındaki tüm fotoğraf ve videoları yükleyin. İsterseniz ek video ve fotoğraf da ekleyebilirsiniz.
   - ![](User_guide/c.png)

3. **Modeli Kullanarak Tespit Yapın:**
   - Eğitim kısmındaki (yukarıda) 8. adımı ve 9. adımda sadece kırmızı ile seçilen yeri değiştirin (lacivert kısım sabit kalsın) ve kodu çalıştırın.

4. **Sonuçları Görüntüleyin:**
   - Eğitim kısmındaki (yukarıda) 10. adımı takip edin. Bu şekilde, eğitim yapmadan önceden eğitilmiş model ile tespitleri gerçekleştirebilirsiniz.
