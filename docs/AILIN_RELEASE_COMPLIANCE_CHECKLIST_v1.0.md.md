AILIN RELEASE COMPLIANCE CHECKLIST

Версия: 1.0Дата: 29 июля 2026 годаТип: короткий внутренний чек-лист перед отправкой Ailin iOS v1.0 в App ReviewНе публикуется: этот Markdown-файл не загружается в App Store Connect

1. Назначение

Этот файл является последней проверкой перед нажатием Submit for Review.

Он не повторяет тексты Privacy Policy, Terms of Use или инструкции документа №06. Если пункт требует подробного ответа для App Store Connect, используется:

06_AILIN_APP_STORE_PRIVACY_AND_REVIEW_ANSWERS_v1.0.md

Статусы:

[x] — завершено;

[ ] — необходимо завершить;

[N/A] — неприменимо к текущему релизу.

2. Пакет документов

№01 — Product Safety and Claims Standard.

№02 — Privacy Policy EN.

№03 — Privacy Policy RU.

№04 — Terms of Use EN.

№05 — Terms of Use RU.

№06 — App Store Privacy and Review Answers.

№07 — Resource License Register.

№08 — Release Compliance Checklist.

Отдельные Subscription Terms, Medical Disclaimer, Crisis Policy или Custom Apple EULA для текущей модели Ailin не требуются: необходимые условия уже включены в документы №01 и №04–05.

3. Обязательные действия до submission

3.1 Оператор, контакты и публичные страницы

Выбран фактический оператор релиза: Nurlan Askarov как физическое лицо либо уже зарегистрированная Ailin LLC.

Во всех публичных документах заменены маркеры оператора, даты, email, адреса и URL.

Privacy Policy EN и RU опубликованы по рабочим публичным HTTPS-ссылкам.

Terms of Use EN и RU опубликованы по рабочим публичным HTTPS-ссылкам.

Support URL открывается без входа и содержит рабочий способ связи.

Privacy Policy и Terms доступны внутри приложения.

Support email принимает входящие сообщения.

3.2 App Store Connect

Загружены финальные название, subtitle, description, keywords, screenshots и app icon.

Указаны Support URL и Privacy Policy URL.

App Privacy заполнено по документу №06: Data Not Collected.

Age Rating заполнен по фактическому содержанию Ailin.

Regulated Medical Device: No.

Content Rights: Yes.

Export Compliance заполнен по документу №06.

App Review contact name, email и phone действительны.

В App Review Notes вставлен и обновлён готовый текст из документа №06.

Выбраны страны/регионы доступности и способ выпуска версии.

Если релиз включает EU: подтверждён статус Trader и проверены email, phone, имя и адрес.

Если EU не включён: EU storefronts не выбраны для этой версии.

3.3 Подписки PRO и PRO+

Paid Apps Agreement активен.

Banking и tax information приняты Apple настолько, насколько это требуется для платных продаж и выплат.

Созданы четыре согласованных продукта: PRO monthly, PRO annual, PRO+ monthly, PRO+ annual.

Product IDs в коде и App Store Connect совпадают.

Для каждого продукта заполнены цена, период, localization и review information.

Все продукты добавлены в правильную subscription group и имеют корректный уровень доступа.

Paywall до покупки показывает название тарифа, период, локализованную цену, автопродление и ссылки на Privacy Policy и Terms.

Purchase, Restore Purchases, cancel/expiration и переходы между PRO/PRO+ проверены в Sandbox или TestFlight.

Первая auto-renewable subscription и её subscription group добавлены в submission вместе с новой версией приложения.

3.4 Production build и содержание

Финальная production-сборка успешно собирается без release-blocking ошибок.

Выполнен полный RU/EN tap-through основных flows: onboarding, Home, Understanding, Cards, Practices, Sleep, SOS, Settings и Paywall.

Free, PRO и PRO+ открывают только положенный контент.

Все обязательные локальные аудио воспроизводятся; background playback, пауза, перемотка и loop работают по утверждённой логике.

Restore Purchases доступен и работает.

Privacy/Terms/Support links открывают правильные страницы.

Нет аккаунта, аналитики, рекламы, tracking, удалённого сбора данных или неизвестного SDK, которые противоречат ответу Data Not Collected.

Нет новых медицинских обещаний, гарантий результата или представления Ailin как лечения, диагностики, медицинского устройства либо кризисной службы.

Crisis/safety wording и внешние действия работают так, как описано в документах и App Review Notes.

В production build нет случайных, тестовых или неизвестных media-файлов и зависимостей.

Version и build number совпадают с выбранной сборкой в App Store Connect.

Финальная сборка проверена минимум на одном реальном iPhone.

4. Что не является блокером Apple submission

Для текущего MVP само по себе не блокирует отправку:

отсутствие LLC, если оператором честно указан Nurlan Askarov;

отсутствие зарегистрированной торговой марки Ailin;

отсутствие отдельного большого сайта при наличии рабочих Privacy, Terms и Support pages;

отсутствие старых Pixabay URL, имён авторов и точных дат скачивания, учитывая подтверждения документа №07;

отсутствие отдельного Android/Google Play compliance package;

отсутствие отдельного Markdown-файла для каждой юридической оговорки;

отсутствие внешнего юридического заключения; консультация адвоката остаётся разумной дополнительной защитой, особенно перед широким международным релизом.

5. Финальное решение

Отправка разрешена только когда все применимые пункты раздела 3 отмечены [x] либо обоснованно [N/A].

App version / build: [VERSION / BUILD]
Legal operator: [LEGAL OPERATOR NAME]
Submission countries/regions: [COUNTRIES / REGIONS]
EU included: [YES / NO]
Final check date: [DATE]
Checked by: Nurlan Askarov
Release decision: [CLEARED FOR SUBMISSION / HOLD]

Если после этой проверки в приложение добавятся аккаунты, analytics, crash-reporting SDK, реклама, tracking, облачная синхронизация, удалённый AI/API, новые permissions или новые сторонние ресурсы, перед следующим релизом необходимо повторно проверить документы №01–08 и ответы App Privacy.

6. После одобрения

Проверить публичную App Store product page и legal links.

Проверить реальную покупку, доступ PRO/PRO+ и Restore Purchases.

Убедиться, что support email продолжает работать.

Сохранить утверждённые version/build, дату выпуска и финальный статус.

Исправлять подтверждённые проблемы через новый build/version; не менять опубликованные обещания без проверки документов и metadata.

7. Официальные источники Apple

App Review Guidelines: https://developer.apple.com/app-store/review/guidelines/

App Privacy: https://developer.apple.com/help/app-store-connect/manage-app-information/manage-app-privacy/

App Review submissions: https://developer.apple.com/help/app-store-connect/manage-submissions-to-app-review/overview-of-submitting-for-review/

First subscription submission: https://developer.apple.com/help/app-store-connect/manage-submissions-to-app-review/submit-an-in-app-purchase/

App Review information: https://developer.apple.com/help/app-store-connect/reference/app-information/platform-version-information/

App availability: https://developer.apple.com/help/app-store-connect/manage-your-apps-availability/manage-availability-for-your-app-on-the-app-store/

EU DSA trader requirements: https://developer.apple.com/help/app-store-connect/manage-compliance-information/manage-european-union-digital-services-act-trader-requirements/