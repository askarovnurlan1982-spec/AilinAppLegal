AILIN APP STORE PRIVACY AND REVIEW ANSWERS

Версия: 1.0Статус: FINAL — рабочая карта ответов для Ailin iOS v1.0Дата утверждения: 29 июля 2026 годаЯзык документа: русский; готовые ответы для Apple приведены на английскомТип документа: внутренний релизный документ; не публикуется пользователям и не загружается в App Store Connect как файл

1. Назначение документа

Этот документ фиксирует ответы для:

App Privacy в App Store Connect;

App Information;

Age Rating;

Content Rights;

Export Compliance;

App Review Information;

проверки подписок PRO и PRO+;

отдельных обязательных compliance-полей Apple.

Документ основан на фактической модели Ailin iOS v1.0:

аккаунт и вход не требуются;

сервер Ailin и cloud sync отсутствуют;

аналитика, реклама, tracking, attribution и сторонний crash-reporting отсутствуют;

AI-чат и отправка пользовательского текста отсутствуют;

доступ к геолокации, камере, фото, микрофону, контактам, календарю и HealthKit отсутствует;

прогресс, настройки и состояние контента хранятся локально на устройстве;

покупки и подписки обрабатываются Apple через StoreKit;

пользовательские тексты и health-related information не передаются из приложения оператору;

ссылки на Privacy Policy, Terms и Support открывают внешние публичные страницы;

Ailin является образовательным и general-wellness приложением, а не медицинским устройством, лечением или кризисной службой.

Ранее завершённый полный аудит контента повторять не требуется. Перед отправкой проверяются только:

фактическая production-сборка;

поля и URL, отмеченные в этом документе маркерами;

новые или изменённые после 29 июля 2026 года функции, SDK, data flows, подписки и материалы.

Если production-сборка противоречит этому документу, приоритет имеет фактическое поведение сборки: сначала исправляется сборка или ответы Apple, а не скрывается расхождение.

2. Финальная карта основных ответов

Поле Apple

Ответ для текущего Ailin

App Privacy — Data Collection

No, we do not collect data from this app

Data Used to Track You

No

Tracking / ATT permission

No; ATT prompt не требуется

Account / Sign-In Required

No

Demo account

Not applicable

Made for Kids

No

Intended minimum age in Ailin documents

16+

Age Rating questionnaire

Frequent Medical or Treatment Information; остальные чувствительные категории — согласно разделу 5

Expected Apple rating on OS 26+

16+

Possible display on OS earlier than 26

17+ из-за преобразования рейтинга Apple

Regulated Medical Device

No

Content Rights

Yes — third-party content is included and all necessary rights are held

License Agreement

Apple Standard EULA

Custom EULA in App Store Connect

Do not add

Non-exempt encryption

No

Advertising Identifier / IDFA

No

Unrestricted Web Access

No

User-Generated Content

No

Messaging or Chat

No

Remote push notifications

No

App Store Server Notifications URL

Leave blank for the current no-server implementation

EU DSA status for commercial worldwide release

Trader

3. App Privacy

3.1 Главный ответ

В App Store Connect выбрать:

Do you or your third-party partners collect data from this app?

No, we do not collect data from this app.

Ожидаемое отображение на странице App Store:

Data Not Collected
The developer does not collect any data from this app.

3.2 Почему этот ответ корректен

Apple считает данные собранными для App Privacy, когда они передаются с устройства и становятся доступными разработчику или его партнёру дольше, чем необходимо для обслуживания запроса в реальном времени.

Локальные настройки и прогресс Ailin:

не покидают устройство;

не передаются оператору Ailin;

не передаются аналитическому, рекламному или crash-reporting сервису;

не связываются с личностью пользователя;

не используются для tracking.

Поэтому локальные данные Ailin не выбираются как собранные data types в App Privacy.

Apple самостоятельно обрабатывает данные App Store и платежей. Платёжные данные, к которым оператор Ailin не получает доступа, не декларируются как данные, собранные Ailin.

3.3 Data-flow inventory

Data flow

Где возникает

Где хранится / обрабатывается

Покидает устройство в пользу Ailin?

App Privacy answer

Язык приложения

App

Локально

Нет

Not collected

Завершение onboarding

App

Локально

Нет

Not collected

Настройки и предпочтения

App

Локально

Нет

Not collected

Прогресс и completion state

App

Локально

Нет

Not collected

Daily Anchor / состояние дневного контента

App

Локально

Нет

Not collected

Audio playback и выбранный контент

App

Локально

Нет

Not collected

StoreKit entitlement / purchase status

Apple и App

Apple + локальная проверка в App

Не передаётся на сервер Ailin

Not collected by Ailin

Карта, банковские и billing details

App Store

Apple

Ailin не получает доступ

Not collected by Ailin

Добровольное письмо в поддержку

Внешний email-клиент пользователя

Email-провайдер и оператор

Да, только по инициативе пользователя

Не включается в label при соблюдении критериев optional customer-service disclosure; раскрыто в Privacy Policy

Переход на публичный Legal/Support URL

Внешняя веб-страница

Браузер и hosting provider

Не является встроенным data flow Ailin

Не включается в App label; web-практики должны быть описаны на сайте

3.4 Что не выбирать

Для текущей сборки не выбирать:

Contact Info;

Health & Fitness;

Financial Info;

Location;

Sensitive Info;

User Content;

Browsing History;

Search History;

Identifiers;

Purchases;

Usage Data;

Diagnostics;

Other Data;

Data Linked to You;

Data Used to Track You.

3.5 Когда ответ Data Not Collected должен быть пересмотрен

Ответ необходимо обновить до submission или до включения новой функции, если появляется хотя бы одно из следующего:

аккаунт, профиль или sign-in;

сервер Ailin, API, база данных, CloudKit или собственный cloud sync;

analytics SDK;

crash-reporting или performance SDK;

advertising, attribution, IDFA или ATT;

push token, передаваемый на сервер;

AI/LLM, чат или отправка текста пользователя;

remote personalization или recommendations;

in-app feedback/support form;

загрузка аудио или контента с сервера, если оператор или партнёр сохраняет доступные ему логи или identifiers;

HealthKit или иной health-data framework;

передача диагностических, usage или device data;

сторонний SDK, который самостоятельно собирает данные.

Изменение Privacy Policy или сайта без изменения data flow не требует нового полного аудита приложения. Проверяется только изменённая часть.

4. Privacy, Support и Legal URLs

4.1 Обязательные поля

Поле

Значение

Privacy Policy URL — English / primary

[PRIVACY POLICY URL EN]

Privacy Policy URL — Russian localization

[PRIVACY POLICY URL RU]

Support URL

[SUPPORT URL]

Terms of Use URL — English

[TERMS OF USE URL EN]

Terms of Use URL — Russian

[TERMS OF USE URL RU]

Support email

[SUPPORT EMAIL]

Privacy Policy URL должен вести непосредственно на рабочую публичную политику, а не на пустую главную страницу.

Support URL должен содержать реальные способы связи. До submission на странице должны быть:

название оператора;

support email;

business mailing address, если он обязателен для выбранных территорий;

телефон, если он обязателен для выбранных территорий или EU trader disclosure;

ссылки на Privacy Policy и Terms of Use.

4.2 Дополнительные поля

Поле

Решение

Privacy Choices URL

Можно оставить пустым: у Ailin нет аккаунта и удаляемых серверных данных

Marketing URL

Optional; можно оставить пустым до появления полноценного сайта

Custom License Agreement

Не заполнять

License Agreement

Использовать Apple Standard EULA

Публичные Ailin Terms дополняют Apple Standard EULA и доступны в приложении и на сайте, но не вставляются в поле Custom EULA.

5. Age Rating

5.1 Ответы анкеты

Заполнять анкету по фактическому содержанию, а не пытаться вручную получить более низкий рейтинг.

Категория Apple

Ответ для Ailin

Parental Controls

No

Age Assurance

No

Unrestricted Web Access

No

User-Generated Content

No

Social Media

No

Social Media Disabled for Users Under 13

No

Messaging and Chat

No

Advertising

No

Profanity or Crude Humor

None

Horror/Fear Themes

None

Alcohol, Tobacco, or Drug Use or References

None

Medical or Treatment Information

Frequent

Health or Wellness Topics

Present / Yes

Mature or Suggestive Themes

None

Sexual Content or Nudity

None

Graphic Sexual Content or Nudity

None

Cartoon or Fantasy Violence

None

Realistic Violence

None

Prolonged Graphic or Sadistic Realistic Violence

None

Guns or Other Weapons

None

Simulated Gambling

None

Gambling

No

Contests

None

Loot Boxes

No

Обсуждение тревоги, паники, навязчивых мыслей и страха смерти не считается horror content само по себе: Ailin не содержит сцен, сюжетов или изображений, созданных для ужаса или террора.

Medical or Treatment Information: Frequent выбирается консервативно и честно, потому что значительная часть приложения содержит guidance around management of anxiety-related and wellness experiences. Неклиническое позиционирование Ailin не означает, что в анкете Apple нужно выбирать None.

5.2 Итоговый рейтинг

На iOS/iPadOS 26 и новее ожидается 16+.

На более ранних версиях ОС Apple может отображать эквивалент 17+.

В Ailin Privacy Policy и Terms сохраняется установленный minimum intended age 16+.

Различие между 16+ и 17+ на старых системах является региональной/системной конвертацией Apple и не требует переписывать Terms.

Не выбирать Made for Kids.

6. Regulated Medical Devices

Для текущего Ailin:

Regulated Medical Device: No

Ailin:

не измеряет медицинские показатели;

не диагностирует;

не назначает и не меняет лечение;

не управляет медикаментами;

не заявляет regulatory clearance;

не является медицинским устройством.

Не загружать regulatory clearance documentation и не описывать Ailin как medical device.

Если Apple задаёт поясняющий вопрос, использовать:

Ailin is a self-guided educational and general-wellness app. It does not diagnose, treat, monitor, prevent, or cure any medical or mental-health condition, and it is not a regulated medical device.

7. Content Rights

Выбрать:

Yes, the app contains, displays, or accesses third-party content, and we have all necessary rights.

Причина:

в Ailin могут использоваться лицензированные nature sounds, ambient audio, voice assets, illustrations, icons или иные сторонние ресурсы;

Apple требует права на такой контент для всех выбранных App Store territories.

До submission документ 07_AILIN_RESOURCE_LICENSE_REGISTER_v1.0.md должен подтвердить для каждого стороннего ресурса:

источник;

правообладателя или лицензиара;

вид лицензии;

commercial app use;

право на modification, conversion и bundling, если применимо;

территории;

срок;

attribution requirement;

сохранённое доказательство лицензии.

Если хотя бы для одного фактически включённого ресурса право не подтверждено, submission блокируется до удаления или замены ресурса.

8. Export Compliance и шифрование

Текущий Ailin:

не реализует собственные криптографические алгоритмы;

не является VPN, secure messenger, password manager или encryption product;

использует только системные сервисы Apple и обычные защищённые соединения, необходимые для App Store/StoreKit или открытия HTTPS-ссылок.

Ответ:

The app does not use non-exempt encryption.

В production-конфигурации проверить:

ITSAppUsesNonExemptEncryption = NO

Это означает отсутствие non-exempt encryption, а не утверждение, что Apple или iOS вообще не используют шифрование.

Если в будущем Ailin добавит собственную криптографию, защищённый backend protocol, VPN, messaging или стороннюю encryption library, export compliance пересматривается до загрузки новой сборки.

9. App Review Information

9.1 Contact Information

Поле

Значение

First name / Last name

Nurlan Askarov

Email

[APP REVIEW CONTACT EMAIL]

Phone

[APP REVIEW CONTACT PHONE]

Контакт должен отвечать на письма и звонки Apple во время review.

9.2 Sign-In Required

Sign-in required: No
Demo username: Not applicable
Demo password: Not applicable

Не создавать фиктивный demo account: в Ailin нет аккаунтов и login.

9.3 Готовая App Review Note на английском

Перед вставкой заменить два маркера точными путями production-сборки.

Ailin is a self-guided educational and general-wellness app for anxiety-related experiences, panic-like sensations, overthinking, intrusive thoughts, grounding, relaxation, and sleep support.

Ailin is not a medical device, diagnostic service, treatment, therapy, emergency service, or crisis hotline. The Ailin SOS feature is an in-app self-support exercise. It does not contact emergency services, assess risk, monitor the user, or alert another person.

No account or sign-in is required. The app does not contain advertising, tracking, analytics, a third-party crash SDK, AI chat, or user-generated content. In-app progress and preferences remain on the device and are not sent to Ailin.

Free content can be accessed without a purchase. Optional PRO and PRO+ auto-renewable subscriptions unlock additional in-app content through Apple StoreKit. The purchase sheet displays the localized price and billing period. Users can restore eligible purchases through the Restore Purchases control.

Review path for subscriptions: [EXACT PAYWALL AND RESTORE PATH].
Legal and safety information: [EXACT SETTINGS / LEGAL PATH].

The app includes bundled audio. Some audio can continue during background playback when the user intentionally starts a session.

No demo credentials are required. All subscriptions submitted with this version should be available in Apple’s review environment.

9.4 Что проверить перед вставкой Review Note

путь к paywall указан точно;

путь к Restore Purchases указан точно;

путь к Privacy Policy, Terms и safety information указан точно;

все названные подписки добавлены в ту же submission;

Free-контент действительно открывается без покупки;

background audio работает только после осознанного запуска пользователем;

в note нет функции, которой нет в production-build.

10. Подписки PRO и PRO+

10.1 Модель

Для Ailin используются auto-renewable subscriptions через Apple StoreKit:

Tier

Period

Planned U.S. price

Product ID

PRO

Monthly

$9.99

[PRO MONTHLY PRODUCT ID]

PRO

Annual

$59.00

[PRO ANNUAL PRODUCT ID]

PRO+

Monthly

$14.99

[PRO PLUS MONTHLY PRODUCT ID]

PRO+

Annual

$89.00

[PRO PLUS ANNUAL PRODUCT ID]

Фактическая цена и период берутся из App Store Connect / StoreKit. Если значения App Store Connect отличаются от таблицы, paywall и документ обновляются до submission.

10.2 Subscription group

PRO и PRO+ должны находиться в одной subscription group, если пользователь должен свободно upgrade/downgrade между уровнями.

Рекомендуемый порядок уровней:

PRO+ — higher service level;

PRO — lower service level.

Monthly и Annual одного tier должны предоставлять один и тот же уровень контента, отличаясь только billing period и ценой.

Перед submission проверить фактическую структуру в App Store Connect. Не создавать несколько групп без отдельной подтверждённой бизнес-причины.

10.3 Subscription Review Information

Для каждого subscription product:

добавить localization;

указать Display Name и Description, совпадающие с paywall;

установить duration;

установить price и availability;

загрузить App Review Screenshot, ясно показывающий предлагаемый tier;

при необходимости добавить review note с точным путём к paywall;

добавить продукт в submission.

Краткий review note для subscription product:

This auto-renewable subscription unlocks the Ailin PRO or PRO+ content shown on the in-app paywall for the selected billing period. Use the tier name that matches this product. It is available at [EXACT PAYWALL PATH]. Eligible purchases can be restored at [EXACT RESTORE PATH].

10.4 Обязательные правила

первая auto-renewable subscription и первая subscription group отправляются вместе с новой версией приложения;

все четыре продукта, которые видны на paywall, должны существовать и быть доступны App Review;

paywall показывает localized price и billing period из StoreKit;

автоматическое продление указано;

cancellation path доступен;

удаление приложения не описывается как отмена;

Restore Purchases работает;

trial или introductory offer не упоминается, пока он реально не настроен в App Store Connect;

внешняя оплата или license key для открытия цифрового контента не используются;

screenshot для review показывает реальный экран и реальное предложение.

11. Дополнительные ответы App Store Connect

Вопрос / поле

Ответ

Does the app use the Advertising Identifier?

No

Does the app track users?

No

Is ATT permission required?

No

Does the app require an account?

No

Is in-app account deletion required?

Not applicable; no account exists

Does the app include user-generated content?

No

Does the app include chat or messaging?

No

Does the app provide unrestricted web access?

No

Does the app include ads?

No

Does the app use HealthKit?

No

Does the app use location, camera, photos, microphone, contacts, or calendar?

No

Does the app use remote push notifications?

No

Does the app use Apple In-App Purchase for paid digital content?

Yes

Does the app have a restore mechanism?

Yes

App Store Server Notifications URL

Blank for current no-server implementation

Family Sharing

Off unless separately implemented and tested

Made for Kids

No

Regulated Medical Device

No

Standard or Custom EULA

Apple Standard EULA

12. EU Digital Services Act

При worldwide distribution, включающей EU, и коммерческой модели с подписками рабочий ответ:

This is a trader account.

До включения EU territories необходимо заполнить и подтвердить:

Поле

Значение

Legal operator

[LEGAL OPERATOR NAME]

Business address / verified address

[BUSINESS MAILING ADDRESS]

Public trader email

[EU TRADER EMAIL]

Public trader phone

[EU TRADER PHONE]

Payment account details

Complete in App Store Connect

Business verification documents

Upload current valid documents

Для организации Apple обычно отображает адрес, связанный с D-U-N-S, и отдельно требует email и phone. Для individual developer Apple требует address или P.O. Box, email и phone.

Не выбирать not a trader только ради сокрытия контактных данных, если Ailin выпускается как коммерческий продукт с платными подписками.

13. Production-build verification перед submission

Это не новый полный аудит контента. Проверяется только соответствие фактической сборки ответам документа.

13.1 Privacy и SDK

В production target нет analytics, ads, attribution и third-party crash SDK.

В production target нет собственных API endpoints или cloud sync.

Package dependencies и embedded frameworks проверены.

Privacy manifests всех включённых SDK присутствуют, если требуются.

PrivacyInfo.xcprivacy корректно описывает используемые required-reason APIs, включая локальное использование UserDefaults, если оно требует декларации.

Xcode privacy report / archive не показывает неожиданные data collection declarations.

Нет IDFA access и ATT prompt.

13.2 Permissions и capabilities

Нет лишних purpose strings для location, camera, photos, microphone, contacts, calendar или HealthKit.

Нет remote push entitlement, если push не реализован.

Background audio capability соответствует реальному audio behavior.

External links не дают unrestricted in-app web browsing.

13.3 Legal links

Privacy Policy EN открывается.

Privacy Policy RU открывается.

Terms EN открываются.

Terms RU открываются.

Support URL открывается и содержит актуальные контакты.

В приложении нет placeholder URL, email, operator name или effective date.

13.4 Purchases

Все product IDs совпадают между кодом и App Store Connect.

PRO/PRO+ entitlement mapping проверен.

Monthly/Annual periods и цены отображаются из StoreKit.

Purchase протестирован.

Upgrade/downgrade протестирован.

Cancel/manage-subscription path открывается.

Restore Purchases протестирован.

Expired/cancelled entitlement обработан правильно.

Все subscription products и group добавлены в submission.

Review screenshots загружены.

13.5 App Review

Review contact email и phone работают.

В App Review Note заменены оба path markers.

Sign-in Required = No.

Reviewer может открыть Free-контент.

Reviewer может найти paywall и Restore Purchases.

App Review Note не превышает лимит поля.

Build number записан: [APP STORE BUILD NUMBER].

14. Маркеры, которые необходимо заменить

Перед submission в этом документе и App Store Connect заменить или подтвердить:

[LEGAL OPERATOR NAME]
[BUSINESS MAILING ADDRESS]
[PRIVACY POLICY URL EN]
[PRIVACY POLICY URL RU]
[TERMS OF USE URL EN]
[TERMS OF USE URL RU]
[SUPPORT URL]
[SUPPORT EMAIL]
[APP REVIEW CONTACT EMAIL]
[APP REVIEW CONTACT PHONE]
[EU TRADER EMAIL]
[EU TRADER PHONE]
[EXACT PAYWALL AND RESTORE PATH]
[EXACT SETTINGS / LEGAL PATH]
[EXACT PAYWALL PATH]
[EXACT RESTORE PATH]
[PRO MONTHLY PRODUCT ID]
[PRO ANNUAL PRODUCT ID]
[PRO PLUS MONTHLY PRODUCT ID]
[PRO PLUS ANNUAL PRODUCT ID]
[APP STORE BUILD NUMBER]

Наличие любого незаменённого маркера в App Store metadata, production-build, public legal pages или App Review Note блокирует submission.

15. Правило будущих обновлений

Полный повторный аудит не проводится, если фактическая privacy-модель Ailin не изменилась.

Проверяются только изменения:

новый SDK;

новый data flow;

новый permission или entitlement;

аккаунт, сервер, cloud sync или AI;

изменения StoreKit;

новый paid tier или offer;

изменение медицинского позиционирования;

новый вид контента, влияющий на age rating;

новая территория с отдельными требованиями;

изменение оператора, email, address, phone или public URL.

Если ничего из перечисленного не изменилось, для следующей версии достаточно подтвердить актуальность ответов и заменить version/build-specific данные.

16. Официальные источники Apple

App Privacy Details

App Review Guidelines

App Information

Platform Version Information and App Review Information

Age Rating Values and Definitions

Required, Localizable, and Editable Properties

Overview of Export Compliance

Offer Auto-Renewable Subscriptions

Submit an In-App Purchase

EU Digital Services Act Trader Requirements

17. История версий

Версия

Дата

Изменение

Статус

1.0

29 июля 2026

Финальная карта App Privacy, Age Rating, Content Rights, Export Compliance, App Review и subscription review answers для Ailin iOS v1.0

FINAL