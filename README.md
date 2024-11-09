## Quiz Uygulaması

Bu proje, C# dilinde yazılmış temel bir Quiz uygulamasıdır. Kullanıcı, sırasıyla kendisine sunulan soruları yanıtlayarak doğru ve yanlış cevap sayısını görebilir. Uygulama, her soru için dört şıklı bir seçim sunar ve kullanıcı her soruyu cevapladıktan sonra doğru ya da yanlış olduğunu anında görebilir.

### Özellikler

- **Soru Sırası ve İlerleme**: "Sonraki" butonuyla sorular arasında geçiş yapılır. Kullanıcı, soruyu yanıtladıktan sonra bir sonraki soruya geçebilir.
- **Doğru/Yanlış Hesaplama**: Her doğru cevap için puanlama yapılır ve doğru/yanlış sayısı görüntülenir.
- **Görsel Geri Bildirim**: Doğru cevap için bir resim (`pictureBox1`), yanlış cevap için ise başka bir resim (`pictureBox2`) görüntülenir.
- **Sonuç Ekranı**: Son soruya gelindiğinde, kullanıcıya doğru ve yanlış cevap sayısı bir mesaj kutusunda gösterilir.

### Kullanılan Araçlar ve Bileşenler

- **Label (lblSoruNo, lblDoğru, lblYanlış)**: Soru numarası, doğru ve yanlış sayısını göstermek için kullanılır.
- **RichTextBox (richTextBox1)**: Soruların metin olarak gösterildiği alan.
- **Button (btnA, btnB, btnC, btnD)**: Her soru için dört farklı cevap seçeneği.
- **Button (btnSonraki)**: Sonraki soruya geçiş yapmak için kullanılan buton.
- **PictureBox (pictureBox1, pictureBox2)**: Doğru ve yanlış cevap için görsel geri bildirim sağlar.

### Kod Akışı ve Mantık

1. **Form1 Yükleme**: `InitializeComponent()` çağrısı ile form yüklenir.
2. **Soru Yükleme ve Geçiş**:
   - `btnSonraki_Click` event'ı, her tıklamada yeni bir soru yükleyerek seçenekleri günceller.
   - `SoruNo` değişkeni her tıklamada artar ve ilgili soruyu yüklenecek soru metni ve seçeneklerle güncellenir.
3. **Cevap Kontrolü**:
   - Her seçenek butonunun (`btnA`, `btnB`, `btnC`, `btnD`) tıklanması, verilen cevabın doğru olup olmadığını kontrol eder.
   - Doğru ise `pictureBox1` gösterilir ve `Dogru` sayısı artırılır; yanlış ise `pictureBox2` gösterilir ve `Yanlis` sayısı artırılır.

### Kullanım

1. Uygulama başlatıldığında, "Sonraki" butonuna tıklayarak ilk soruya ulaşabilirsiniz.
2. Doğru olduğunu düşündüğünüz seçeneğe tıklayın. Sonraki soruya geçmek için tekrar "Sonraki" butonuna basın.
3. Tüm sorular bittiğinde, sonuçlar bir mesaj kutusunda gösterilecektir.

### Geliştirme Notları

- Daha fazla soru eklemek için `btnSonraki_Click` fonksiyonundaki `SoruNo` kontrol bloklarına yeni sorular eklenebilir.
- Uygulamanın sonundaki sonuç ekranı, bir form üzerinden veya daha detaylı bir sonuç gösterimi için genişletilebilir.
- Proje, Windows Forms üzerine kurulu olduğundan, görsel düzenlemeler için Windows Forms Designer kullanılabilir.
