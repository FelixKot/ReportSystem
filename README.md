# ReportSystem
	Система репорта V3.6.0
	АВТОР СКРИПТА: Felix.
								ReportSystem
---Введение:
Данный FS был написан с целью улучшения условий работы администрации и контроля над ними главными админами.

---Функции:
= Меню репортов для администрации<br>
= Уникальный номер каждому репорту
= Вывод каждому репорту его статуса
= Возможность просматривать репорт перед ответом
= Возможность напечатать ответ перед отправкой
= Возможность редактирования ответа перед отправкой
= Возможность удаления репорта
= Лимит макисимального кол-ва репортов
= Лимит для отправки репортов одному игроку
= Лимит времени перед отправкой повторного репорта
= Уведомление игроку о изменении позиции его репорта в очереди
= Уведомление игроку о том, что админ принялся за рассмотрение его жалобы
= Уведомление игроку о том, что админ удалил его репорт
= Уведомление админам каждые n-сек о неотвеченных репортах, если от админов нет активности
= Логирование репортов
= Логирование ответа админов
= Логирование удалённых репортов
= Логирование каждые n-сек админов в онлайн, если никто не отвечает на репорты
= Проверка мута перед подачей репорта
= Возможность отправки готового ответа от вышедшего администратора
= Автоматическая очистка репортов игрока, покинувшего сервер
= Перезагрузка конфигов без рестарта сервера
= Возможность выбора стиля ответа игроку с сохранением на сессию
= Возможность включать и отключать репорт
= Панель управления CVar's прямо на сервере
= Возможность отслеживать кол-во ответов Ваших админов для записи в MySQL (если запись велась до установки fs)
= Запрет администрации писать в репорт (анти-накрутка)
= Возможность мгновенного ответа
= Функция очистки репортов
= Возможность ответа без диалогов (даже если репорт не создан)
= Звуки репорта и ответа
= Возможность дать доступ к меню хелперам
= Система оффлайн ответов

---Особенности:
= Настройка всех переменных через конфиг
= Настройка всех выводимых текстов через файл перевода
= Возможность использовать цвета для текста (формат HEX)
= Мультиязычность
= Прост в установке и настройке
= Уведомления об обновлениях скрипта

---Команды:
= Клиентские команды:
= /report - открытие меню отправки репорта (опционально)
= Админские команды:
= /ans (/ans id) - ответ (опционально)
= /ansmenu - открыть меню репортов (опционально)
= Команды для root админа:
= /rms - открыть (изменить) настройки конфига
= /reloadreportcfg - перезагрузка настроек (опционально)

---CVars:
= version -> версия скрипта (не менять)
= language -> язык перевода. По умолчанию: 1
= admin -> уровень админки, для доступа к меню репортов. По умолчанию: 1
= helper -> уровень хелперки, для доступа к меню репортов (0 = выкл). По умолчанию: 0
= root -> уровень админки, для доступа к /rms. По умолчанию: 0(выкл)
= mute -> вкл/выкл проверку на мут. По умолчанию: 1
= log -> управление логами (подробнее в конфиге). По умолчанию: 4
= style -> вкл / выкл выбор стиля (подробнее в конфиге). По умолчанию: 0
= floodtime -> время перед повторной подачей репорта. По умолчанию: 15
= error_msg -> вкл / выкл сообщение проверяющему админу, о том что игрок покинул сервер. По умолчанию: 1
= a_newmes -> вкл / выкл сообщение админам, о поступлении нового репорта. По умолчанию: 1
= mes_check -> вкл / выкл оповещание игроку о изменениях пизиции его репорта в очереди. По умолчанию: 1
= mes_open -> вкл / выкл оповещание игроку, когда администратор открывает его репорт. По умолчанию: 1
= mes_del -> вкл / выкл оповещание игроку, когда администратор удаляет его репорт. По умолчанию: 1
= max_player_report -> максимальное кол-во репортов от одного игрока. По умолчанию: 3
= warning -> время до вывода предупреждения, если админы не отвечают на репорты. По умолчанию: 180
= r_warns -> кол-во предупреждений до вывода админов онлайн в лог. По умолчанию: 5
= rm_check -> отключить возможность просмотра репорта. По умолчанию: 0
= rm_print -> отключить возможность печатать ответ на репорт. По умолчанию: 0
= rm_ansed -> отключить возможность отправки ответа на репорт. По умолчанию: 0
= rm_delete -> отключить возможность удаления репорта через меню репортов. По умолчанию: 0
= report_plus -> вкл/выкл REPORT++ на экране. По умолчанию: 1
= rm_offans -> 0 - автоочистка репортов при выходе; 1 - система оффлайн ответов. По умолчанию: 1
= report_text -> оформление (подробнее в конфиге). По умолчанию: 1
= rm_ansbutton -> Вкл / выкл кнопку 'Отправить ответ'. По умолчанию: 1
= report_sound_report -> Звуковое оповещание при поступлении нового репорта (подробнее в конфиге). По умолчанию: 41603
= report_sound_ans -> Звуковое оповещание при поступлении нового ответа (подробнее в конфиге). По умолчанию: 1085

---Переводы:
= Русский.
= Английский. (не обновлялся с версии 3.2)
Большое спасибо Mirby за помощь в переводе.

---Используемые плагины:
= sscanf

***Скрипт предоставляется бесплатно! Для регистрации обращайтесь в лс vk.com/pberezin0***
