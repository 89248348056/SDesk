﻿**Программа 1С:**** Service Desk**

**ТЭО**

1. **Цели и задачи 1С:**** Service Desk**

Основными целями внедрения программы 1С:Service Desk являются:

1. Осуществление «первой линии поддержки» пользователей информационных систем для дальнейшей обработки данных и возможной передачи на следующие уровни поддержки другим подразделениям.
2. Прием, регистрация и обработка обращений пользователей.
3. Проведение анализа и оценки поступивших обращений для планирования дальнейших работ.
4. Повышение скорости обработки заявок.
5. Выявление потребностей в доработке информационных систем.

 Для реализации поставленных целей система должна решать следующие задачи:

- Прием и регистрация обращений в одной единой точке;
- Возможность описать проблему в теле «Обращения», прикрепить фото, картинку или скриншот.
- Изменение статусов обращений, в зависимости от этапа, на котором находится обращение (Зарегистрировано, В уточнении, Отклонено, Отозвано, Выполнено, Принято пользователем);
- Возможность анализировать количество обращений, время выполнение обращений
- Обеспечение одновременного доступа множества пользователей;
- Защита данных от несанкционированного доступа, искажения и уничтожения.

1. **Перечень выполняемых системой функций**

Система должна выполнять следующие функции:

- вход пользователей в систему с дальнейшей аутентификацией и авторизацией;
- регистрация и учет обращений;
- возможность отклонять обращения (администратор);
- возможность отозвать обращение (пользователь);
- возможность выбрать вид обращений (консультация, запрос на обслуживание, инцидент) из выпадающего списка (пользователь);
- от вида обращений зависят сроки исполнения обращений;
- возможность изменять вид обращений (администратор);
- формирование отчетности в разрезах измерений, скомбинированных пользователем;
- возможность типизировать обращения;
- анализ типовых обращений;

1. **Анализ аналогов системы**

На сегодняшний день существует множество вариантов программного обеспечения – аналогов предложенной системы управления инцидентами, проблемами и изменениями. Каждое из решений поддерживает определенный круг функционала. Но тем не менее, не существует единого решения для любого предприятия.

| **CMS** | **Достоинства** | **Недостатки** |
| --- | --- | --- |
| Freshservice  | Управление инцидентами.Управление проблемами.Управление изменениями.Управление релизами.Управление активами.Отслеживание проблем.Система заявок.База знаний.Портал самообслуживания.Автоматизация стола обслуживания.Несколько языков.Несколько Часовых поясов.Обзор степени удовлетворенности.Игрофикация.Автоматическое присвоение заявок.Каталог услуг.REST API.Отчётность «из коробки».Каталог продукции.  | - Нет экспорта данных / бэкапа- Дорогой сервис- неуклюж и медленен в своих интерфейсах |
| ManageEngine ServiceDesk Plus  | - бесплатная демо-версияИнтеграция с Active Directory.Система закупок.Бизнес-правила для управления запросами.Группировка похожих запросов.Назначение очередей.Пользовательские отчёты.Доски объявлений.Выставление счетов по времени.Редакторы HTML для решений и уведомлений.Управление инцидентами.Управление проблемами.База знаний.Портал самообслуживания с автосбросом пароля.Планировщик.Удалённое управление. | - не удобный интерфейс для пользователя, так как много лишних полей, назначение которых не очень понятно.- интерфейс не меняли довольно давно (выглядит не современно).  |
| Freshdesk  | Простая, быстрая установка.Многоканальная поддержка — электронная почта, телефон, чат, социальные сети и др.Портал самообслуживания для автоматизации помощи своим клиентам.Портал сообщества для сбора своих поклонников.Многопрофильная поддержка глобальной компании.Поддержка нескольких языков и часовых поясов.Опросы для определения степени удовлетворённости заказчика.Умная автоматика для экономии времени агентов.Интегрированная игровая механика для мотивации своих агентов.Мощные отчёты о вашей справочной службе. | - высокая цена;- отсутствие шаблонов ответов;- отсутствие управления инцидентами- отсутствие уведомлений   |

1. **Совокупность условий, при которых предполагается эксплуатировать будущую систему, архитектура системы, аппаратные и программные ресурсы, условия функционирования, обслуживающий персонал и пользователи системы**

Создание отдельного приложения для самостоятельной регистрации обращений. Приложение используется сотрудниками отдела сопровождения информационных систем (далее ОСИС) и пользователями ИС компании (далее Пользователи). В подразделении ОСИС 4 специалиста – администраторы программы, которые обрабатывают обращения, поступающие по телефону горячей линии. Особых условий эксплуатации не требуется.

Архитектура приложения – клиент-серверная с сервером СУБД. Тип архитектуры выбран из-за ряда причин:

- многопользовательский режим работы;
- гарантия целостности данных.

В процессе функционирования приложения должны использоваться программные и аппаратные средства с учетом удобства их применения в рамках программного продукта. Интерфейс веб-приложения построен на основе платформы 1С 8.3.

Для веб-приложения существуют следующие условия функционирования:

Параметры хостинга:

операционная система Microsoft Windows Server и СУБД MS SQL (под сервер баз данных).

виртуальный сервер на базе MS Windows Server. (это будет VDS с виртуализацией KVM).

2 Гб. оперативной памяти и 40 Гб. места на диске.

1. **Сроки завершения отдельных этапов, форма приемки/сдачи работ, привлекаемые ресурсы, меры по защите информации**

| Этап работ | Содержание работ | Сроки работ |
| --- | --- | --- |
| Подготовительный этап | Подготовка к внедрению, предпроектные работы. | 14.02.2019 – 05.03.2019 |
| 1 этап | Дизайн | 06.03.2019 – 19.03.2019 |
| 2 этап | Программирование | 19.03.2019 – 22.04.2019 |
| 3 этап | Отладка | 22.04.2019 – 22.12.2018 |

| Категория специалиста | Кол-во | Занятость специалистов по категориям (раб. часы) |
| --- | --- | --- |
| Представитель заказчика | 1 | 248 |
| Руководитель проекта | 1 | 200 |
| Консультант | 1 | 80 |
| Программист | 2 | 344 |
| **Итого:** | **5** | **1 916** |



| Режим задачи | Название задачи | Длительность | Начало | Окончание | Предшественники | Названия ресурсов | Затраты |
| --- | --- | --- | --- | --- | --- | --- | --- |
|   | **Итог** | **74 дней** | **Чт 14.02.19** | **Вт 28.05.19** |   |   | **444 768,00р.** |
| **Автоматическое планирование** | **Подготовка, предпроектные работы.** | **29 дней** | **Чт 14.02.19** | **Вт 26.03.19** |   |   | **79 968,00р.** |
| Автоматическое планирование |       Определение концепции | 2 дней | Чт 14.02.19 | Пт 15.02.19 |   | Руководитель проекта | 4 544,00р. |
| Автоматическое планирование |       Маркетинговые исследовани | 4 дней | Пн 18.02.19 | Чт 21.02.19 | 3 | Консультант;Руководитель проекта | 27 776,00р. |
| Автоматическое планирование |       Определение функционала | 2 дней | Пт 22.02.19 | Пн 25.02.19 | 4 | Представитель заказчика;Руководитель проекта | 4 544,00р. |
| Автоматическое планирование |       Разработка графической схемы | 4 дней | Вт 26.02.19 | Пт 01.03.19 | 5 | Программист;Руководитель проекта | 40 832,00р. |
| Автоматическое планирование |       Составление технического задания | 2 дней | Пн 04.03.19 | Вт 05.03.19 | 6 | Представитель заказчика | 0,00р. |
| Автоматическое планирование |       Согласование и подпись договора | 1 день | Ср 06.03.19 | Ср 06.03.19 | 7 | Представитель заказчика;Руководитель проекта | 2 272,00р. |
| Автоматическое планирование |        Подготовка завершена | 14 дней | Чт 07.03.19 | Вт 26.03.19 | 8 | Представитель заказчика | 0,00р. |
| **Автоматическое планирование** | **Дизайн** | **10 дней** | **Ср 27.03.19** | **Вт 09.04.19** |   |   | **76 384,00р.** |
| Автоматическое планирование |    Разработка дизайн-концепции | 3 дней | Ср 27.03.19 | Пт 29.03.19 | 9 | Консультант;Программист | 37 824,00р. |
| Автоматическое планирование |    Отрисовка дизайн-макета | 4 дней | Пн 01.04.19 | Чт 04.04.19 | 11 | Программист | 31 744,00р. |
| Автоматическое планирование |    Согласование дизайн-макета | 2 дней | Пт 05.04.19 | Пн 08.04.19 | 12 | Представитель заказчика;Руководитель проекта | 4 544,00р. |
| Автоматическое планирование |    Согласование дизайна | 1 день | Вт 09.04.19 | Вт 09.04.19 | 13 | Представитель заказчика;Руководитель проекта | 2 272,00р. |
| **Автоматическое планирование** | **Программирование** | **35 дней** | **Ср 10.04.19** | **Вт 28.05.19** |   |   | **288 416,00р.** |
| Автоматическое планирование |    Программирование | 23 дней | Пт 12.04.19 | Вт 14.05.19 | 14;17;18 | Программист | 182 528,00р. |
| Автоматическое планирование |    Получение информации от заказчика | 2 дней | Ср 10.04.19 | Чт 11.04.19 | 14 | Представитель заказчика;Руководитель проекта | 4 544,00р. |
| Автоматическое планирование |    Наполнение информацией | 1 день | Ср 10.04.19 | Ср 10.04.19 | 14 | Консультант;Программист | 12 608,00р. |
| Автоматическое планирование |    Согласование продукта | 1 день | Ср 15.05.19 | Ср 15.05.19 | 16 | Представитель заказчика;Программист;Руководитель проекта | 10 208,00р. |
| **Автоматическое планирование** | **   Отладка** | **9 дней** | **Чт 16.05.19** | **Вт 28.05.19** |   |   | **78 528,00р.** |
| Автоматическое планирование |       Тестирование | 1 день | Чт 16.05.19 | Чт 16.05.19 | 19 | Консультант | 4 672,00р. |
| Автоматическое планирование |       Опытная эксплуатация | 5 дней | Пт 17.05.19 | Чт 23.05.19 | 21 | Представитель заказчика;Программист;Руководитель проекта | 51 040,00р. |
| Автоматическое планирование |       Исправление ошибок | 2 дней | Пт 24.05.19 | Пн 27.05.19 | 22 | Программист | 15 872,00р. |
| Автоматическое планирование |       Презентация готового продукта | 1 день | Вт 28.05.19 | Вт 28.05.19 | 23 | Консультант;Представитель заказчика;Руководитель проекта | 6 944,00р. |

Будут предприняты следующие меры по защите информации:

- исключение случаев ведения особо важных работ только одним человеком;
- работа в офисе заказчика;
- организация обслуживания системы посторонней организацией или лицами, незаинтересованными в сокрытии фактов нарушения работы;
- универсальность средств защиты от всех пользователей (включая высшее руководство);
- источники бесперебойного питания аппаратуры, а также различные устройства стабилизации, предохраняющие от резких скачкообразных перепадов напряжения и пиковых нагрузок в сети электропитания;
- предоставление возможности входа в систему только однозначно идентифицированным пользователям;
- резервное копирование данных.

Согласно п. 1.3 ГОСТ 34.603-92 для автоматизированных систем устанавливают следующие основные виды испытаний:

- предварительные;

- опытная эксплуатация;

- приемочные.

Для приемки системы в промышленную эксплуатацию создается приемочная комиссия из сотрудников Заказчика.

Выполненные работы принимаются функциональным заказчиком с подписанием акта сдачи-приёмки исполнения договорных обязательств.

1. **Расчет экономического эффекта от внедрения системы**  **Service**** Desk ****.**

Главный экономический эффект от внедрения средств автоматизации заключается в улучшении экономических и хозяйственных показателей работы предприятия, в первую очередь за счет повышения оперативности управления и снижения трудозатрат на реализацию процесса управления, то есть сокращение времени и ресурсов на обработку обращений.

- снижение трудозатрат на регистрацию обращений;
- сокращение времени на работу с обращениями;
- сокращения служащих предприятия.

Критерием эффективности создания и внедрения новых средств автоматизации является ожидаемый  **экономический эффект**.

Он определяется по формуле:

| _Э=Э __год__ -Е __н__ \*К_ |
| --- |

где _Э__год_ - годовая экономия;

_Е __н__  -_ нормативный коэффициент (Eн=0.15);

_К _- капитальные затраты на проектирование и внедрение, включая первоначальную стоимость программы.

 Годовая экономия _Э__год_ складывается из экономии эксплуатационных расходов и экономии в связи с повышением производительности труда пользователя. Таким образом, получаем:

| _Э __год__ =Р1-Р2_ |
| --- |

где Р1 и Р2 - соответственно эксплуатационные расходы до и после внедрения разрабатываемой программы;



_Капитальные затраты:_

Чтобы найти _К_ - капитальные затраты на создание и внедрение программы воспользуемся формулой:

| _К = К __об_ _+ К__ мон_ _+С__р_ |
| --- |

где: _К__об_- капитальные затраты на оборудования;

_К__мон_- капитальные затраты по монтажу.

_С__р_ - себестоимость разработки программного обеспечения.

Капитальные затраты по монтажу в нашем случае не учитываются.

Необходимо приобрести оборудование и обеспечение.

Показатели, используемые при расчетах, предоставлены в таблице:

| № п/п | Наименование оборудования и программ | Количество, шт | Цена за единицу, руб. | Стоимость, руб. | Норма амортизации |
| --- | --- | --- | --- | --- | --- |
| 1. | Лицензия на сервер 8.3 | 1 | 86 400 | 86 400 |   |
| **ВСЕГО:** | **86 400** |   |

_Ср-_ себестоимость разработки программного обеспечения складывается из:

- основной зарплаты участников проекта - З_осн_ (руб);

- основные затраты на соц. нужды – _С__соц.нуж_

Таким образом, себестоимость разработки программного обеспечения рассчитаем по формуле:

| _С __р__ = З __осн_ _+ С__ соц.нуж __С__ р_= 444 768+13% = 502 587 руб. |
| --- |

_К_ - капитальные затраты на создание и внедрение программы по формуле составят:

| _К = Коб + Кмон +Ср__К_ = 86 400 + 502 587 = 588 987 руб. |
| --- |

_Расчет эффективности от внедрения программы:_

До внедрения информационной системы на оформление и обработку одного обращения затрачивалось 30 минут. После внедрения информационной системы время сократилось на 10 минут.

Рабочий день специалиста составляет восемь часов, или 480 минут. В день до внедрения программного обеспечения специалист оформлял:

480/30=16 заявок/день;

После внедрения:

480/20=24 заявки/день;

Рассчитаем разницу в количестве обращений, оформляемых специалистом до внедрения программного обеспечения и после за год.

ДО внедрения:

16\*255=4080 обращений/год;

ПОСЛЕ внедрения:

24\*255=6 120 обращений/год.

В день после внедрения программного проекта экономия времени составляет:

16\*20мин = 320 мин;

480-320=160 мин, или 2,7 часа.

После внедрения у специалиста появилось больше свободного времени, которое он может занять другой работой. Или же, при имеющихся обращениях, успеть обработать большее количество за день.

Рассчитаем экономичность, при условии сокращения 1 специалиста:

|   | ДО внедрения | ПОСЛЕ внедрения |
| --- | --- | --- |
| Время обработки 1 обращения | 30 мин | 20 мин |
| Количество обращений, выполняемых 1 специалистом в день (шт) | 16 обр/день | 24 обр/день |
| Количество обращений, выполняемых 1 специалистом (шт) | 4 080 обр/год | 6 120 обр/год(на 2 040 обращений больше) |
| Количество обращений, выполняемых 4-мя специалистами (шт) | 4 080\*4 = 16 320 обр/год | 6 120\*4 = 73 440 обр/год( на 24 480 обращений больше) |
| Расходы на з/пл 4-х специалистов | 50 000\*3\*12 = 2 400 000 руб. |
| Количество обращений, выполняемых 3-мя специалистами (шт) |   | При условии, что в год поступает 16 320 обращений, сократив 1 сотрудника, подразделение будет выполнять 18 360 обращений.6 120 \*3 = 18 360 обр/год  |
| Расходы на з/пл 3-х специалистов | 50 000\*3\*12 =1 800 000 |
| Экономия на з/пл | 2 400 000 – 1 800 000 = 600 000 руб/год. |

Годовая экономия _Э__год_ составит:

| _Э __год__ =Р1-Р2 __Э__ год_ = 2 400 000 – 1 800 000 = 600 000 руб/год. |
| --- |

Срок окупаемости:

| _Т __ок.__ =_ _К/ __Э__ год __.__ =_588 987/600 000 = 0,9, что составляет примерно 7,5 месяца. |
| --- |

Экономический эффект составит:

| **Э=Э**** год ****-Е**** н ****\*К** = 600 000-(588 987\*0,15) = 511 652 руб. |
| --- |

В итоге получаем следующую ожидаемую экономическую эффективность:

**Э =****   ****511 652 руб.**

О чем говорят эти цифры? Даже при приблизительном расчете экономическая эффективность от внедрения программного средства получилась значительной. Такой она получилась за счет сокращения 1 сотрудника и сокращении расходов на оплату з/пл. ** **

**Заключение:**

 По результатам расчета экономической эффективности проектирования и внедрения системы ServiceDesk сразу можно сказать, что это выгодно. Хоть выгода и косвенная, но, как правило, заметная в средней и долгосрочной перспективе. Внедрение средств автоматизации может привести к корректированию самого бизнес-процесса, так как задачи выполняются быстрее. Сотрудники могут обрабатывать большие объемы информации за свое рабочее время, что можно использовать или для уменьшения затрат на персонал или для быстрого развития бизнеса при неизменности количества сотрудников, занятых обработкой обращений.

1. **Что не будет реализовано в рамках проекта**

В рамках проекта не будут реализованы интеллектуальные компоненты, позволяющие прогнозировать и планировать деятельность предприятия.