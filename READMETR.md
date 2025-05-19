# 📌 Klinik Yapay Zekâ Değerlendirmesinde Negatif Öngörü Değeri (NPV)

## 🧠 Proje Hakkında

Bu depo, **Negatif Öngörü Değeri (NPV)** kavramının, genel **doğruluk (accuracy)** düşük olsa bile nasıl yüksek kalabildiğini görsel ve kavramsal olarak açıklamaktadır — bu durum, gerçek dünya sağlık uygulamalarında hâlâ güçlü bir klinik değere sahip olabilir.

Görselleştirme **Excel** ile hazırlanmış olup, ikili sınıflandırma için karışıklık matrisi ilişkilerine odaklanmaktadır:
- Gerçek Sınıf (Doğru Etiket)
- Tahmin Edilen Sınıf (Model Çıktısı)

---

## 🎯 Neden Önemli?

Çoğu yapay zekâ ve makine öğrenmesi projesinde **kesinlik (precision)**, **duyarlılık (recall)**, **F1 skoru** ve **doğruluk (accuracy)** gibi metrikler önceliklidir.

Ancak **klinik uygulamalarda** öncelikler farklılaşır.

Çoğu zaman göz ardı edilen fakat **klinik açıdan kritik** olan bir metrik vardır: **Negatif Öngörü Değeri (NPV)**

> 🔎 **NPV**, test sonucu negatif çıkan bir kişinin gerçekten sağlıklı olma olasılığını gösterir.  
> Özellikle **tarama senaryolarında** çok önemlidir — amaç, hastalığı olmayan kişileri güvenle ayırt etmektir.

Bu metrik, bir model *"sağlıklısın"* dediğinde, bu cevabın neredeyse her zaman doğru olmasını sağlar — bu da sağlık hizmetlerinde temel bir gerekliliktir.

---

## 📊 Tablo Ne Gösteriyor?

Bu projede görselleştirilen tablo 2x2’lik bir karışıklık matrisini temsil eder:

|                     | **Tahmin: Pozitif**            | **Tahmin: Negatif**             |
|---------------------|-------------------------------|---------------------------------|
| **Gerçek: Pozitif** | Doğru Pozitif (TP)            | Yanlış Negatif (FN) – Tip II Hata |
| **Gerçek: Negatif** | Yanlış Pozitif (FP) – Tip I Hata | Doğru Negatif (TN)            |

Aşağıda, karışıklık matrisi terimleriyle ifade edilen ilgili metrik formülleri yer alır:

| **Metrik**        | **Formül**                             |
|------------------|-----------------------------------------|
| Duyarlılık       | TP / (TP + FN)                          |
| Özgüllük         | TN / (TN + FP)                          |
| Doğruluk         | (TP + TN) / (TP + TN + FP + FN)         |
| Kesinlik         | TP / (TP + FP)                          |
| NPV              | TN / (TN + FN)                          |

---

## 💬 Gerçek Klinik Verilerden Yansımalar

Tez çalışmam sırasında gerçek klinik veri setleriyle çalışırken önemli bir şey öğrendim:

> Modelin **doğruluğu düşük olsa bile**, **yüksek NPV** modeli **klinik olarak değerli** kılabilir.

Klinik pratikte sıkça duyulan bir ifade şudur:
> **"NPV yüksekse, düşük doğruluk kabul edilebilir."**

Bu şu gerçekleri ortaya koyar:
- **Değerlendirme metrikleri bağlama göre seçilmelidir.**
- **Hastalığı erken tespit etmek için yanlış negatiflerin azaltılması hayati önemdedir.**

Bu yaklaşım sadece istatistiksel doğruluğu değil, aynı zamanda **tahminlerin arkasındaki insan hayatını** da ön planda tutar.

---

<p align="center">
  <span style="font-size:40px;"><strong>Karışıklık Matrisi</strong></span><br/>
</p>

![NPV Confusion Matrix](confusion_matrix_EN.png)  
*Şekil: Gerçek ve tahmin edilen sınıflar arasındaki ilişkiyi gösteren karışıklık matrisi.*

##

Bu depoda yer alan Excel tabanlı görsel şunları içermektedir:
- TP, FP, FN, TN olarak etiketlenmiş karışıklık matrisi hücreleri
- Hata türlerinin açıklamaları ve temel metrik formülleri

_Alternatif Metin (erişilebilirlik için):_  
**İkili sınıflandırma için TP, FP, FN, TN hücreleri ve ilgili metrik formülleri (Duyarlılık, Özgüllük, Kesinlik, NPV, Doğruluk) içeren karışıklık matrisi. Klinik model değerlendirmesi amacıyla tasarlanmıştır.**

---

📩 **İletişim**

Herhangi bir sorunuz, öneriniz veya sorun bildiriminiz olursa, benimle iletişime geçmekten çekinmeyin.  
Bana [LinkedIn](https://www.linkedin.com/in/emirkan-beyaz-07732933b) üzerinden ulaşabilir veya e-posta atabilirsiniz:  
📧 **beyazemirkan01@gmail.com**

---

## 📄 Lisans

Bu çalışma, **[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)** lisansı ile lisanslanmıştır.

Şunları yapmakta özgürsünüz:
- İçeriği paylaşmak, kopyalamak, uyarlamak ve ticari amaçlarla bile yeniden dağıtmak.
- Sadece uygun şekilde atıf yapmanız ve değişiklik yaptıysanız belirtmeniz yeterlidir.
