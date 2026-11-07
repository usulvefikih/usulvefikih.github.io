# باب المحرمات

```mermaid
flowchart TD
    classDef root fill:#1b2631,stroke:#34495e,color:#fff,stroke-width:2px,font-weight:bold
    classDef duration fill:#117a65,stroke:#0b5345,color:#fff,stroke-width:2px,font-weight:bold
    classDef illet fill:#2e4053,stroke:#5d6d7e,color:#fff,stroke-width:2px
    classDef term fill:#7d3c98,stroke:#512e5f,color:#fff,stroke-width:1px,font-style:italic
    classDef furu fill:#ebedef,stroke:#aeb6bf,color:#2c3e50,stroke-width:1px
    classDef serh fill:#fdf2e9,stroke:#e59866,color:#873600,stroke-dasharray: 5 5

    R["المحرمات"]:::root

    %% Ana Taksim: Müebbed ve Muvakkat
    D1["المحرمات المؤبدة"]:::duration
    D2["المحرمات المؤقتة"]:::duration

    R --> D1
    R --> D2

    %% Müebbed İlletleri
    D1 --> I1["١. التحريم بالنسب"]:::illet
    D1 --> I2["٢. التحريم بالمصاهرة"]:::illet
    D1 --> I3["٣. التحريم بالرضاع"]:::illet

    %% Neseb Alt Başlıkları (Fıkhî Istılahlar)
    I1 --> T1["الأصول"]:::term
    I1 --> T2["الفروع"]:::term
    I1 --> T3["أجزاء الأبوين"]:::term
    I1 --> T4["أجزاء الأجداد"]:::term

    T1 --> F1_1["الأمهات والجدات وإن علون"]:::furu
    T2 --> F1_2["البنات وبنات الأولاد وإن سفلن"]:::furu
    T3 --> F1_3["الأخوات وبناتهن وبنات الإخوة"]:::furu
    T4 --> F1_4["العمات والخالات"]:::furu

    %% Musâhara Alt Başlıkları (Fıkhî Istılahlar)
    I2 --> TM1["أصول الزوجة"]:::term
    I2 --> TM2["فروع الزوجة"]:::term
    I2 --> TM3["أصول الزوج"]:::term
    I2 --> TM4["فروع الزوج"]:::term
    
    TM1 --> F2_1["أمهات الزوجات والجدات"]:::furu
    TM2 --> F2_2["بنات الزوجات (الربائب)"]:::furu
    TM3 --> F2_3["زوجات الآباء والأجداد (حليلة الأصل)"]:::furu
    TM4 --> F2_4["زوجات الأبناء (حليلة الفرع)"]:::furu
    
    F2_2 -.-> S1["شرط: الدخول بالأم<br/>(فتح القدير: العقد على البنات يحرم الأمهات،<br/> والدخول بالأمهات يحرم البنات)"]:::serh
    F2_1 -.-> S1

    %% Muvakkat İlletleri
    D2 --> I4["٤. التحريم بالجمع"]:::illet
    D2 --> I5["٥. التحريم لعارض"]:::illet

    %% Cem' Bahsi ve İmam Züfer İhtilafı
    I4 --> F4_1["الجمع بين ذواتي محرم<br/>(كل امرأتين لو فرضت إحداهما ذكراً حرم نكاح الأخرى)"]:::furu
    F4_1 -.-> S2["خلاف الإمام زفر:<br/>يشترط ثبوت التحريم من الجانبين<br/>(فإن حرم من جانب واحد جاز الجمع)"]:::serh
    
    %% Ârızî Haller
    I5 --> F5_1["المنكوحة للغير أو المعتدة"]:::furu
    I5 --> F5_2["المشركة والمجوسية"]:::furu
    I5 --> F5_3["المطلقة ثلاثاً"]:::furu