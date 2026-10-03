# Источники и аналоги

Первичная проверка: 2026-10-03. Документ различает подтверждённую доступность материала и выполненную проверку реализации. В этой редакции реализации нет. Для паспорта эмпирической формулы нужны полное уравнение/коэффициенты, издание, страница и диапазоны, а не только ссылка на продукт.

## Аналоги

| Источник | Что подтверждает | Что не подтверждает |
|---|---|---|
| Siam GeoTest, SiamEngy: https://siamgeotest.com/engy | Структуру продукта: интерактивные расчёты, конвертер, справочник | Точность нашего ядра, право копировать код/дизайн/иллюстрации |
| SiamEngy release: https://siamgeotest.com/blog/siam-engy-release | Принцип расчёта неизвестных и позиционирование | Безусловную применимость обратных решений |
| SiamEngy Google Play: https://play.google.com/store/apps/details?id=com.siam.geotest.siam_engy | Каталог возможностей аналога | Независимый научный источник всех методик |
| SiamEngy App Store: https://apps.apple.com/us/app/siamengy-petroleum-calculator/id1602641707 | Публичное описание продукта/история | Отсутствие ошибок |
| Halliburton cementing software: https://www.halliburton.com/en/well-construction/well-cementing/cementing-software | eRedBook как аналог таблиц и расчётов цементирования | Право распространять Halliburton/API таблицы |
| Halliburton eRedBook: https://apps.apple.com/us/app/halliburton-eredbook-mobile/id507496941 | Объёмные калькуляторы и справочные данные труб | Лицензию на базы труб и готовые изображения |

«Мобильный калькулятор нефтяника» может обозначать SiamEngy либо другой продукт. Отдельный продукт под этим названием не идентифицирован однозначно: нужна ссылка/разработчик. Сравнение здесь ограничено подтверждёнными SiamEngy и eRedBook; доступ к их закрытым формулам/коду не предполагается.

## Научная и метрологическая база

| Источник | Применение/статус |
|---|---|
| BIPM, The International System of Units, 9th edition: https://www.bipm.org/en/publications/si-brochure/ | Основы СИ и обозначений; актуальную ревизию фиксировать в каталоге единиц |
| NIST, Special Publication 811: https://www.nist.gov/pml/special-publication-811 | Применение СИ и коэффициенты; источник старше нового определения СИ, актуальные базовые определения сверять с BIPM |
| OpenStax, University Physics Volume 1, Chapter 14 Key Equations: https://openstax.org/books/university-physics-volume-1/pages/14-key-equations | p=p0+ρgh и непрерывность; учебный физический источник, не полная нефтепромысловая модель |
| OpenStax, §14.5 Fluid Dynamics: https://openstax.org/books/university-physics-volume-1/pages/14-5-fluid-dynamics | Средний расход/скорость, ограничения несжимаемой среды |
| SLB Energy Glossary, Hydrostatic pressure: https://glossary.slb.com/en/terms/h/hydrostatic_pressure | Отраслевой смысл гидростатики, TVD; 0.052 в US единицах округлено и не заменяет точное ядро СИ |
| SLB Energy Glossary, True vertical depth: https://glossary.slb.com/en/terms/t/true_vertical_depth | Различие TVD и MD |
| Hydraulic Institute, Pump Curves: https://datatool.pumps.org/pump-fundamentals/pump-curves.html | Законы подобия с предположениями и соответствующими точками; не фактический дебит скважины |
| Hydraulic Institute, System Operating Point: https://datatool.pumps.org/pump-fundamentals/combined | Рабочая точка совместно с характеристикой системы |

Для объёмной обводнённости, реагентов, электрической мощности всей цепи и специализированных методов ещё требуются отраслевые первичные источники/паспорта. Наличие физического вывода позволяет подготовить кандидат, но не поставить статус производственного допуска.

## Архитектура, безопасность, локализация

- Android Developers, offline-first: https://developer.android.com/topic/architecture/data-layer/offline-first — локальное хранение/синхронизация, не конкретная реализация Flutter.
- Flutter iOS deployment: https://docs.flutter.dev/deployment/ios — сборка и выпуск iOS через macOS/Xcode.
- Flutter supported platforms: https://docs.flutter.dev/reference/supported-platforms — сверять при закреплении SDK/minimum OS.
- OWASP MASVS: https://mas.owasp.org/MASVS/ и MASTG: https://mas.owasp.org/MASTG/ — требования/методы испытаний безопасности; не заявление о завершённом аудите.
- Supabase RLS: https://supabase.com/docs/guides/database/postgres/row-level-security — разграничение доступа; не заменяет E2EE.
- Supabase self-hosting: https://supabase.com/docs/guides/self-hosting — условия самостоятельного управления и обязанности эксплуатации.
- Unicode CLDR: https://cldr.unicode.org/ и Dates: https://unicode.org/reports/tr35/tr35-dates.html — локали, календари/форматы, часовые пояса; нужно проверить библиотеку для выбранного Dart SDK.

## Магазины и платежи

- Google Play personal account testing: https://support.google.com/googleplay/android-developer/answer/14151465?hl=en — подтверждены минимум 12 участников/14 дней для соответствующих новых личных аккаунтов, затем production application/review.
- Google Play Payments: https://support.google.com/googleplay/android-developer/answer/10281818?hl=en — правила цифровых покупок, региональные исключения проверить перед интеграцией.
- Google Play Russia/Belarus billing: https://support.google.com/googleplay/android-developer/answer/11950272?hl=en — доступность бесплатных приложений и ограничения оплаты для пользователей; не окончательная проверка российского merchant account.
- Apple enrollment: https://developer.apple.com/help/account/membership/program-enrollment — стандартная стоимость программы, варианты регистрации.
- Apple Review Guidelines: https://developer.apple.com/app-store/review/guidelines/ — review, покупки, privacy; требования применяются к фактическим функциям.
- Apple In-App Purchase: https://developer.apple.com/in-app-purchase/ — платёжная интеграция последующего этапа.
- RuStore registration: https://www.rustore.ru/help/developers/developer-account/registration-developer — подтверждены регистрация физлица/юрлица; возможности коммерческой монетизации проверяются отдельно.
- Samsung guide: https://developer.samsung.com/galaxy-store/distribution-guide.html — подтверждены требования качества/метаданных и запрет beta для публичной подачи; seller status уточнить.
- Xiaomi global portal: https://global.developer.mi.com/ — подтверждён глобальный канал GetApps; JS-портал, индивидуальные условия/аккаунт ещё не проверены.
- Xiaomi creation/update: https://orig-global.developer.mi.com/document?doc=appManagement.createAndUpdate — официальный поисковый результат инструкции, содержимое консоли перед подачей проверить.
- Huawei AppGallery: https://consumer.huawei.com/en/mobileservices/appgallery/ — подтверждён канал Android; developer documentation при проверке возвращала ошибку, аккаунт/публикация не подтверждены.

## Повторная проверка

Перед каждым допуском методики: точная ревизия источника и поправки/errata. Перед публикацией: SDK/target API, тип аккаунта, региональная доступность, возраст/данные/удаление аккаунта, подпись. Перед платежами/рекламой: правила региона/канала и получателя, договоры/налоги/маркировка. Цифры комиссий и универсальная доступность всех стран намеренно не считаются установленными фактами.
