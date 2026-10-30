# 📊 Satış Analizi Dashboard-u

Bu layihə fərqli mənbələrdən daxil olan xam satış məlumatlarının təmizlənməsi, birləşdirilməsi və interaktiv şəkildə vizuallaşdırılması prosesini əhatə edir.

## 🖼️ Dashboard-un Vizual Görüntüsü
![Satış Analizi Dashboardu](dashboard_visual.png)

## 🎯 Layihənin Məqsədi
* Şirkətin ümumi satış göstəricilərini Brend, Məhsul, Kateqoriya və Regionlar üzrə analiz etmək.
* İnteraktiv filtrlər (Slicers) vasitəsilə istifadəçiyə illər, aylar, günlər və spesifik brendlər üzrə dinamik hesabat təqdim etmək.

## 🛠️ Görülən İşlər və ETL (Power Query) Mərhələsi
1. **Datanın Əldə Olunması:** İlkin olaraq fərqli mənbələrdə olan xam data faylları (Tapşırıq data 1 və Tapşırıq data 2) Power BI mühitinə inteqrasiya edilmişdir.
2. **Başlıqların Uyğunlaşdırılması:** Sütun başlıqları standart formaya gətirilmiş və xətalar aradan qaldırılmışdır.
3. **Data Tiplərinin Təyini (Data Types):** Hər bir sütunun məlumat tipi (Mətn, Tarix, Tam/Onluq rəqəmlər) düzgün şəkildə konfiqurasiya edilmişdir.
4. **Append & Merge Transformasiyaları:** Strukturca eyni olan datalar `Append` funksiyası ilə alt-alta birləşdirilmiş, zəruri əlaqəli məlumatlar isə `Merge` vasitəsilə vahid modelə gətirilmişdir.
5. **Unpivot Tətbiqi:** Analizin daha çevik və performanslı işləməsi üçün relyasion modelə uyğun olmayan geniş sütunlar `Unpivot` edilərək sətir strukturuna çevrilmişdir. Heç bir kənar table ilə lazımsız dərəcədə birləşdirilməyərək data modelin optimallığı qorunmuşdur.

## 📊 Hesabatda Yer Alan Vizual Elementlər
* **Dinamik Filtrlər (Slicers):** İl, Ay, Gün, Brend və Məhsul kateqoriyalarına görə sürətli filtrasiya.
* **Brend üzrə satış (Clustered Bar Chart):** Ən çox satılan brendlərin həcm göstəriciləri.
* **Məhsul üzrə satış (Donut Chart):** Məhsulların ümumi satış payındakı faiz nisbəti (Kivi, Alma, Armud, Mandarin, Banan).
* **Kateqoriya üzrə satış (Clustered Column Chart):** Kateqoriyalar üzrə gəlir payının müqayisəsi.
* **Region üzrə satış (Clustered Bar Chart):** Sumqayıt, Şirvan, Sabirabad, Bakı və digər regionlar üzrə satışın coğrafi performansı.
