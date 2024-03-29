Задание 2.

Высоконагруженная база данных MySql, критичная к отказу.

Выбор: Физические сервера

Причины:

- Надежность
- Производительность

Использование виртуализации создает дополнительную нагрузку ввиду наличие прослойки в виде гипервизора между Hardware и Software.
Виртуализация на уровне ОС не так надежна, как физический сервер ввиду использования общего ядра ОС.

Различные web-приложения.

Выбор: Виртуализация уровня ОС

Причины:

- Масштабируемость
- Гибкость
- Производительность
- Изоляция

Физические сервера надежны, но неудобны по части масштабирования. Относительно паравиртуализации это решение выигрывает в удобности управления и производительности. Виртуализация на уровне ОС использует общее ядро без прослойки в виде гипервизора. И управлять этими абстракциями проще и быстрее.

Windows-системы для использования бухгалтерским отделом.

Выбор: Паравиртуализация

Причины:

- Гибкость
- Изоляция

Ввиду того, что это windows-система, использование Виртуализации на уровне ОС при использовании хостовой системы на базе Windows дает не такую гибкость, как использование ОС на базе ядра Linux. А использование в качестве хостовой машины Linux омрачается тем, что на таких машинах не запустить контейнер на базе Windows из-за различия ядер, API. Допустимо использовать физические сервера, но тут гибкость и масштабируемость будет хромать.

Системы, выполняющие высокопроизводительные расчёты на GPU.

Выбор: Физические сервера

Причины: 

- Надежность
- Производительность

В случае с паравиртулазиацией и с Виртуализацией уровня ОС есть недостаток - использование прослоек и ограничение доступа к Hardware. Физический сервер не предполагает использование прослоек и не ограничен в доступе к Hardware - для таких систем это идеальный вариант.



Задание 3.

1. Тут подходит система управления виртуализацией VMware vSphere. VMware предлагает широкий спектр возможностей для управления виртуальными машинами, включая балансировку нагрузки, репликацию данных и создание резервных копий.
2. Для небольшой инфраструктуры подходит KVM (Kernel-based Virtual Machine). KVM является частью ядра Linux и обеспечивает высокую производительность для виртуализации. Можно выбрать Xen, но для он требует больше шагов для настройки.
3. Для виртуализации Windows-инфраструктуры подойдет Hyper-V, т.к. это решение от Microsoft, которое обеспечивает хорошую совместимость с Windows-средой и высокую производительность.
4. Для тестирования программного продукта на нескольких дистрибутивах Linux подойдет VirtualBox, так как это бесплатное решение, которое обеспечивает хорошую совместимость с различными дистрибутивами Linux и легко настраивается для тестирования.


Задание 4.

Гетерогенная среда виртуализации имеет несколько недостатков:

1. Сложность управления: Использование различных систем управления виртуализацией может привести к сложностям в управлении и мониторинге всей среды. Различные интерфейсы и методы управления могут создавать дополнительные сложности для администраторов.

2. Совместимость: Различные системы виртуализации могут иметь ограничения в совместимости с другими системами, что может привести к проблемам при миграции виртуальных машин или обмене данными между ними.

3. Безопасность: Использование нескольких систем управления виртуализацией может создавать дополнительные уязвимости и слабые места в безопасности среды из-за различий в методах аутентификации, авторизации и контроля доступа.

Для минимизации рисков и проблем нужно:

1. Стандартизировать процессы управления: Важно создать стандарты для управления и мониторинга всех систем виртуализации, чтобы упростить процессы администрирования.

2. Использовать единый интерфейс: Возможно, использование унифицированного интерфейса управления для всех систем виртуализации поможет упростить работу администраторов.

3. Тщательно планировать совместимость: При выборе различных систем виртуализации необходимо тщательно планировать и проверять их совместимость друг с другом.

Если бы у меня был выбор, я бы предпочел избегать гетерогенной среды виртуализации, поскольку это позволит уменьшить сложность управления, повысить безопасность и обеспечить более простую поддержку и мониторинг. Однако, в некоторых случаях, например, при необходимости поддерживать легаси-системы, гетерогенная среда имеет место быть.