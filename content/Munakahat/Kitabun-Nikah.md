# Kitâbü'n-Nikâh

Bu sayfa el-Hidâye merkezli nikâh bahislerinin ana haritasıdır. Alt başlıklara tıklayarak detaylı illet tahlillerine ulaşabilirsiniz.

```mermaid
flowchart TD
    %% Modern Pastel Renk Paleti
    classDef ana fill:#dce4f2,stroke:#869ab8,color:#2c3e50,stroke-width:2px
    classDef fasil fill:#e8f4e5,stroke:#93b88b,color:#2c3e50,stroke-width:2px

    A["كتاب النكاح<br/>(الخريطة الكلية)"]:::ana

    A --> B["١. ماهية النكاح وانعقاده<br/>(شروط الصيغة والشهادة)"]:::fasil
    A --> C["٢. المحرمات<br/>(أسباب التحريم)"]:::fasil
    A --> D["٣. الولاية في النكاح<br/>(ثبوتها وشروطها)"]:::fasil
    A --> E["٤. الكفاءة<br/>(الاعتبار والخصال)"]:::fasil
    A --> F["٥. المهر<br/>(المسمى ومهر المثل)"]:::fasil
    A --> G["٦. نكاح الرقيق وأهل الذمة<br/>(أحكام مخصوصة)"]:::fasil

    %% Tıklanabilir Bağlantılar (Quartz Altyapısı İçin)
    click B "Inikad" "İn'ikad detaylarına git"
    click C "Muharremat" "Muharremât detaylarına git"
    click D "Velayet" "Velâyet detaylarına git"
    click E "Kefaet" "Kefâet detaylarına git"
    click F "Mehir" "Mehir detaylarına git"
    click G "Zimmi" "Zımmî detaylarına git"
 
