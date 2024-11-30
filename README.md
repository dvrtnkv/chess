# Клуб “Четырёх коней”

## Тестовое задание Yandex crowd

### Чек лист из анкеты для участия в отборе

- [x] Сверстайте адаптивный лендинг по макету в [Figma](https://www.figma.com/file/mbUi7prsyinFITFz5Rmzy8/%D0%94%D0%B8%D0%B7%D0%B0%D0%B9%D0%BD-%D0%B4%D0%BB%D1%8F-%D0%B2%D0%B5%D1%80%D1%81%D1%82%D0%BA%D0%B8-%7C-%D0%A2%D0%B5%D1%81%D1%82%D0%BE%D0%B2%D1%8B%D0%B9-%D0%BB%D0%B5%D0%BD%D0%B4%D0%B8%D0%BD%D0%B3?type=design&node-id=69-1068&mode=design&t=7OOmQFDjnTFNN3Lv-0), используя стек **html + css + чистый js** (без библиотек и фреймворков).
- [x] Придерживайтесь принципа Pixel Perfect.
- [x] Избегайте дублирования текстового контента в мобильной и десктопной версиях.
- [x] Добавьте бегущую строку и другую анимацию по своему усмотрению.
- [x] Кнопки на стартовом экране являются якорями и ведут к соответствующим блокам.
- [x] Карусель с карточками участников должна быть зацикленной и меняться автоматически через каждые 4 секунды.
- [x] Карусель с этапами не должна быть зацикленной и не должна автоматически менять слайды.

---

### Чек лист [@dvrtnkv](https://github.com/dvrtnkv)

#### Общие требования к лендингу

- [x] Изображения: размеры mobile/desktop, формат webp, сжатие, preload, svg в base64
- [x] Набор иконок разных размеров, 150x150, 180x180, 192x192, 512x512 +maskable, favicon 32x32, 16x16, .ico 48x48,
- [x] manifest.json
- [x] Стиль и скрипт учитывают ширину viewport
- [x] Минимальное разрешение где ничего не ломается 375px без учета вертикальной полосы прокрутки
- [x] Анимация вне viewport на паузе
- [x] Стили для отключенного Javascript
- [x] Стили для @media print
- [x] Стили для @media (prefers-reduce-motion: reduce)
- [x] Проверка орфографии
- [x] Meta тэги описания и ключевые слова

#### Шапка сайта

##### Логотип

- [x] Иконка коня cжатый svg в data:image/svg+xml;base64

##### Фон

- [x] Бесшовный повторяющийся фон из оригинального изображения имитирующий текстуру старой бумаги (сделано с GIMP)
- [x] Предзагрузка фоновых изображений шапки rel=”preload” as=”image” в head
- [x] Позиционирование в соответствии с дизайном на ключевых разрешениях экрана =375px, >=1366px

##### Кнопки

- [x] Состояния default, hover, active
- [x] Контейнер кнопок column на мобильной версии, в строку на desktop
- [x] Якорные ссылки плавно скролят к соответствующим блокам на странице

#### Бегущая строка

- [x] Бесконечная плавная анимация без скачков
- [x] Пауза при :hover
- [x] Пауза анимации если элемент вне поля видимости viewport(используется Intersection Observer API) с учетом :hover состояния
- [x] размер шрифта mobile/desktop с использованием clamp()
- [x] высота строки mobile/desktop с использованием clamp()
- [x] При печати страницы не отображается

#### Карусель этапов

- [x] Три адаптивных layout - mobile, tablet, desktop
- [x] Прокрутка одного слайда вправо
- [x] Прокрутка одного слайда влево
- [x] Отключение кнопки если дальше нет слайдов
- [x] Пересчитывает координаты при window.resize для отображения того слайда на котором были до resize
- [x] Переключение слайдов при нажатии на точки индикаторы позиции

#### "Бесконечная" карусель участников

##### Кнопки

- [x] Состояние hover, active, disabled
- [x] Неактивны во время переходов между слайдами
- [x] Автопрокрутка остонавливается если навести на блок кнопок или счетчика
- [x] Всплывающее уведомление о состоянии анимации
- [x] Уведомление сверху/снизу на разной ширине экрана
- [x] Анимированый таймер прогресса автоматического переключения 4с
- [x] Таймер сбрасывается при hover на блок кнопок
- [x] Изменение количества просмотренных элементов при переходах

##### Список

- [x] Определение начального смещения в зависимости от ширины контейнера
- [x] Прокрутка одного слайда вправо
- [x] Прокрутка одного слайда влево
- [x] Проброс на дубликат влево при движение вправо (имитация бесконечной прокрутки)
- [x] Проброс на дубликат вправо при движении влево (-//-)
- [x] Пересчитывает координаты при window.resize, сбрасывает на первый слайд
- [x] Стили определяют оптимальное количество и размер видимых элементов
- [ ] Свайп для мобильных устройств

#### Тесты и оптимизация сервера (за кадром)

- [x] Минимизация CSS, HTML, JS
- [x] Кэширование файлов на долгий срок
- [x] Поддержка протоколов [HTTP/2](https://www.ipvoid.com/http2-test/), [HTTP/3, QUIC](https://http3check.net/?host=collarslab.com)
- [x] Test TLS Checker [Excellent](https://www.ipvoid.com/tls-checker/) (TLSv1.2 TLSv1.3) другие отключены
- [x] HTTPS [Let’s Encrypt](https://letsencrypt.org/ru/)
- [x] Тест SSL сертификата A+ (ssllabs.com)
- [x] Тест безопасности заголовков [Probely](https://securityheaders.com/?q=https%3A%2F%2Fcollarslab.com%2Fchess%2F&hide=on&followRedirects=on) A+
- [x] Поддержка сжатия **[gzip](https://www.ipvoid.com/gzip-test/), [br](https://www.ipvoid.com/brotli-test/)**
- [x] Перенаправление www на **non-www** и http на **https**
- [x] Mozilla Observatory [Test](https://observatory.mozilla.org/analyze/collarslab.com): A+ очков: 125
- [x] ImmuniWeb A+
- [x] HSTS домен добавлен в список Preload на 1 год https://hstspreload.org
- [x] Lighthouse Navigation test [desktop](https://pagespeed.web.dev/analysis/https-collarslab-com-chess/pbw5j8u0mj?form_factor=desktop)/[mobile](https://pagespeed.web.dev/analysis/https-collarslab-com-chess/pbw5j8u0mj?form_factor=mobile)
