.. title: NetworkManager перешел на GDBus
.. slug: networkmanager-перешел-на-gdbus
.. date: 2016-02-23 13:55:00
.. tags:
.. category:
.. link:
.. description:
.. type: text
.. author: Peter Lemenkov

**Это архивная статья**


`Dan Williams <https://www.openhub.net/accounts/dcbw>`__ официально
`объявил <https://blogs.gnome.org/dcbw/2016/02/19/die-dbus-glib-die/>`__,
что NetworkManager полностью перешел с использования устаревшей
библиотеки dbus-glib на современную альтернативу - GDBus. Задача решена
в основном усилиями `уже
известного </content/networkmanager-обрастает-enterprise-grade-функционалом>`__
вам `Dan Winship <https://fedoraproject.org/wiki/User:Danw>`__. Для
подавляющего большинства пользователей изменение будет незаметно. К
сожалению, некоторые legacy-апплеты потребуется переделать. Для этого
разработчики предлагают использовать библиотеку libnm, которую как раз и
создали на этот случай. В процессе перевода некоторых компонентов на
использование libnm, удалось заметно сократить их кодовую базу, заодно
приобретя юнит-тесты, сократив цепочку зависимостей, и полагаясь на
более правильный API.

В последнее время NetworkManager быстро разрабатывается, получая все
новые и новые десктопные функции. Появился `улучшенный поиск Wi-Fi
сетей <https://blogs.gnome.org/dcbw/2016/01/18/networkmanager-1-2-has-better-wi-fi-scanning/>`__,
реализована `улучшенная защита от отслеживания в Wi-Fi
сетях <https://blogs.gnome.org/lkundrak/2016/01/18/networkmanger-and-tracking-protection-in-wi-fi-networks/>`__
(рандомизация MAC-адреса при сканировании). Последняя фича тоже была
подсмотрена нашими коллегами у лидеров по юзабилити, придумавших не один
хитрый трюк, у компании Apple. Кстати, помните, как они `сумели добиться
получения DHCP-адреса менее, чем за
секунду </content/Суб-миллисекундное-получение-адреса-по-dhcp-в-systemd>`__,
а наши коллеги потом разработали свой вариант, превзошедший решение
Apple?
Так же нужно отметить долгожданное появление т.н. `"Airplane
mode" <http://www.hadess.net/2016/01/support-for-airplane-mode-keys.html>`__
- это уже не NetworkManager, но функционал был давно ожидаемый. Вокруг
стабилизирующейся платформы рабочего окружения в Linux тоже начали
появляться интересные проекты - например, `появилась возможность
экспортировать настройки NetworkManager в виде
QR-кода <https://blogs.gnome.org/muelli/2015/12/using-networkmanager-to-export-your-wifi-settings-as-a-barcode/>`__.

Было сложно скопировать настройки с вашего компьютера на телефон? Теперь
это элементарно! Надо лишь знать Python.

