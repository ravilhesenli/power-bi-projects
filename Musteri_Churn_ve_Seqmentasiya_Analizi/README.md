# 📉 Müştəri Churn (Tərk Etmə) və Seqmentasiya Analizi

Bu layihə, şirkətin müştəri bazasının aktivliyini izləmək, tərk etmə (churn) risklərini analiz etmək və müştəriləri alış davranışlarına görə seqmentasiya etmək üçün hazırlanmış qabaqcıl analitik Power BI dashboard-udur.

## 🖼️ Dashboard-un Vizual Görüntüsü
Layihəni endirmədən öncə hesabatın interaktiv strukturunu aşağıdan baxa bilərsiniz:

![Müştəri Churn Analizi](churn_analizi.png)

## 🎯 Biznes Məntiqi və Müştəri Seqmentasiyası
Layihə çərçivəsində dataya şirkət strukturunun qaydalarına əsasən xüsusi şərtlər tətbiq edilmiş və müştərilər 3 əsas kateqoriyaya ayrılmışdır:
* **🏃‍♂️ Çıxmış Müştəri (Churn):** Sonuncu alış-veriş tarixi üzərindən **120 gündən çox** vaxt keçən və şirkəti tərk etdiyi qəbul edilən müştərilər.
* **✨ Yeni Müştəri:** İlk alış tarihindən etibarən hələ **60 gün** tamam olmamış müştərilər.
* **🔄 Daimi Müştəri:** Şirkətlə müntəzəm işləyən və yuxarıdakı iki şərtə daxil olmayan aktiv müştərilər.

## 🛠️ Görülən İşlər və Analitik Həllər
* **Data Modelləşdirilməsi:** Müştəri məlumatları, satış qeydləri və regional strukturlar arasında relyasion əlaqələr qurulmuşdur.
* **DAX ilə Şərtlərin Hesablanması:** Müştərilərin alış tarixləri arasındakı gün fərqlərini (`DATEDIFF`, `TODAY` və ya son satış tarixləri ilə) dinamik hesablamaq və onları "Çıxmış", "Yeni" və "Daimi" olaraq etiketləmək üçün mürəkkəb DAX formullarından istifadə edilmişdir.

## 📊 Hesabatda Yer Alan Əsas Vizuallar (1 Səhifəlik Dashboard)
* **KPI Kartları:** Ümumi "Çıxmış Müştəri" sayı (155) və "Yeni Müştəri" sayının (33) birbaşa izlənilməsi.
* **Bölgə Müdiri və Təmsilçi üzrə Analiz (Clustered Bar Chart):** Hansı bölgə müdirinin və satış təmsilçisinin nə qədər çıxmış, yeni və daimi müştəriyə sahib olduğunu göstərən performans qrafiki.
* **Regional və Region üzrə Analiz (Clustered Column Chart):** Müştəri seqmentlərinin coğrafi (Bakı və digər regionlar) payını və çıxmış müştərilərin regional konsentrasiyasını göstərən vizual.
* **Kanal üzrə Pay Bölgüsü (Donut Charts):** Yeni və çıxmış müştərilərin hansı satış kanallarına (məsələn: P, R, Y, O, S) aid olduğunu göstərən faiz və say analizi.
* **Müştəri və Mağaza Siyahısı (Tables):** Müştəri və mağaza adlarına görə son 5 aylıq satış həcmlərini göstərən detallı analitik cədvəllər.

## 💾 Data Mənbəyi (Source)
* Layihənin xam Excel dataları qovluq daxilindəki `Data_Sources/` bölməsində yerləşir.
