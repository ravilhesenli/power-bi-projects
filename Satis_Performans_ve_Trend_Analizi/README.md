# 📊 Satış Performansı və Trend Analizi (2 Səhifəlik Dashboard)

Bu layihə fərqli mənbələrdən toplanmış satış və plan datalarının ETL, Data Modelləşdirmə (Star Schema) və Time Intelligence (Zaman Analizi) funksiyaları tətbiq edilərək hazırlanmış genişmiqyaslı interaktiv hesabatdır.

---

## 🖼️ Dashboard Səhifələri və Vizual Görüntülər

### Səhifə 1: Satış Hesabatı (Plan və Fakt Analizi)
Bu səhifə cari satışların şirkətin təyin etdiyi plan göstəriciləri ilə müqayisəsinə, menecer/kuryer performansına və hədəf icra faizlərinə fokuslanır.
![Satış Hesabatı](satis_hesabati.png)

### Səhifə 2: Satış Müqayisə Hesabatı (Zaman Analizi - YoY)
Bu səhifə cari satışları keçən ilin eyni dövrü ilə (Same Period Last Year) aylıq, rüblük və coğrafi əsasda müqayisə edərək böyümə trendlərini analiz edir.
![Satış Müqayisə Hesabatı](satis_muqayise.png)

---

## 🛠️ Görülən İşlər və ETL (Power Query) Mərhələsi
1. **Məlumatların İnteqrasiyası:** Xam məlumatlar Power BI mühitinə uğurla idxal edilmiş, sütun başlıqları standartlaşdırılmış və məlumat tipləri (Tarix, Rəqəm, Mətn) düzgün təyin edilmişdir.
2. **Birləşdirmə Əməliyyatları:** Data strukturları analiz olunaraq zəruri cədvəllər arasında `Append` və `Merge` transformasiyaları uğurla tətbiq edilmişdir.
3. **Data Modelləşdirilməsi (Model View):** 
   * Fakt və Dimensiya cədvəllərini özündə birləşdirən optimal **Star Schema (Ulduz Sxemi)** qurulmuşdur.
   * `Tarix` (Date), `Hesabat` və müvafiq relyasion cədvəllər arasında **1-to-Many (1:*)** əlaqələri yaradılaraq filtrasiya istiqamətləri optimallaşdırılmışdır.

### Layihənin Data Modeli:
![Data Modeli](data_model.png)

---

## 📐 Yazılmış DAX Metrikaları və Analitik Həllər
Hesabatda mürəkkəb biznes suallarına cavab tapmaq üçün xüsusi DAX formullarından istifadə edilmişdir:
* **Plan İcra %:** Ümumi Satışın Ümumi Plana olan nisbəti hesablanmış və icra faizləri vizuallaşdırılmışdır.
* **Keçən ilin eyni dövrü üzrə Satış (YoY):** `SAMEPERIODLASTYEAR` funksiyası tətbiq edilərək dinamik zaman analizi aparılmışdır.
* **Satışda artım faizi (% YTD / YoY Growth):** Keçən illə müqayisədə faizlə böyümə trendi təyin edilmişdir.

---

## 📊 Hesabatda Yer Alan Əsas Vizual Elementlər

### 1-ci Səhifə (Satış Hesabatı):
* **Gauge (Spidometr) Vizualları:** Azərbaycan, Bakı və Regionlar üzrə ümumi satış və plan göstəricilərinin vizual müqayisəsi və plan icra faizləri.
* **Table (Cədvəl):** Alıcı adlarına görə Ümumi Plan, Ümumi Satış və Plan İcra faizinin sətirbəsətir analizi.
* **Line and Clustered Column Chart:** Menecer və Kuryerlər üzrə plan, satış və plan icra faizlərinin birgə analizi.

### 2-ci Səhifə (Satış Müqayisə Hesabatı):
* **KPI Kartları:** Cari Satış, Keçən ilin eyni dövründəki satış, Keçən aya görə satış, Alıcı sayı və YoY artım faizləri.
* **Matrix (Matris):** Menecer, Kuryer və Aylar üzrə satışların ötən ilin müvafiq dövrü ilə ətraflı müqayisəli cədvəli.
* **Line Chart:** Ən çox satış edilən TOP 10 şəhərin (Sumqayıt, Abşeron, Kürdəmir və s.) satış həcmləri.
* **Line and Clustered Column Chart:** Aylar üzrə Satış, Keçən ilin eyni dövründəki satış və ildən-ilə böyümə faizlərinin dinamik trend xətti.
