.. title: Новости Linux-платформы - systemd 216
.. slug: Новости-linux-платформы-systemd-216
.. date: 2014-08-22 10:48:09
.. tags:
.. category:
.. link:
.. description:
.. type: text
.. author: Peter Lemenkov

**Это архивная статья**


| Уже давно не секрет, что наши коллеги создают платформу Linux (все
  работы проводятся в рамках Fedora Project, конечно). Эта будущая
  платформа в "софтверной" части будет состоять из Linux-ядра, systemd,
  GNU C Library (glibc), RPM, как менеджер пакетов, и Wayland, как
  графическая система. Создание такой платформы резко упростит
  разработку открытого ПО (мы вам рекомендуем отказаться от поддержки
  различных вариантов BSD, ограничившись может быть лишь Mac OS X,
  которой пополам с Windows и пользуются BSD-любители), избавит от
  необходимости клепать сто тыщ дистрибутивов, сведя разницу между ними
  лишь к различным обоям. На самом деле это, конечно, полемическое
  упрощение - разница между дистрибутивами сведется лишь к бизнес-логике
  (вопросы обновления ПО, ориентация на какие-то конкретные задачи и
  архитектуры, и т.п.), но тем не менее, понятно, что общая платформа
  избавит разработчиков от тучи проблем.

| Из последних новостей о платформе стоит поставить на первое место
  `выход systemd
  216 <https://thread.gmane.org/gmane.comp.sysutils.systemd.devel/22172>`__.

  Среди большого количества изменений хочется выделить то, что в нем
  улучшена работа DNS-резолвера (вернее в нем теперь включен полноценный
  DNS-резолвер с возможностью кэшировать запросы), и реализована
  библиотека для работы с TTY (собственный подход к `задаче удаления
  виртуальных терминалов из
  ядра </content/Идет-работа-по-удалению-виртуальных-терминалов-из-ядра-configvtn>`__).

  Коллеги-аналитики уже обсуждают изменения на
  `OpenNET.ru <https://www.opennet.ru/opennews/art.shtml?num=40414>`__ и
  `Linux.org.ru <https://www.linux.org.ru/news/linux-general/10782717>`__.

  Системные администраторы локальных машин немного запаниковали, и
  некоторые полагают, что пора покупать Macbook, но мы рекомендуем
  поступить иначе и не экономить на обедах в школе и институте ради
  дорогостоящего профессионального инструмента. Вместо этого
  перспективнее было бы добавить в закладки systemd cheatsheet:

|image0|

| 
| А ведь мы пару лет назад по-дружески предупреждали любителей SysVinit:

    `...критикам systemd пора перестать беспомощно критиковать его
    (особенно на уровне "Lennart Poettering supports it" и "Lennart
    Poettering is an asshole" - этот сорт критики смотрится особо
    #жалко), а начать его изучать. Это ваше будущее, и вам с ним
    придется работать (если придется,
    конечно). </content/И-вновь-приветствуем-изменения-в-archlinux>`__

| 
| В очередной раз, как мы говорили вам, так оно и стало.


| 

    `Они сожрут твоих детей, Марк. Живьем сожрут,
    понимаеш? <https://plus.google.com/+VadimRutkovsky/posts/N1kCqm5GsEe>`__
    Редхатовские зомби, Марк, они такие. Думаеш чего в
    Опенстаке каноникал проигрывают? Потому что редхатовских
    зомби пули не берут. Убунтушники их пытаются убить, Марк, но
    это трудно. Их только "Юнити" можно. А сколько
    убунтушников съели заживо?! Слакварщики плачут как маленькие
    мальчики, когда редхатовкие зомби разгрызают им животы
    и вынимают еще горячие кишки, Марк. Это страшно,
    пропаганда об этом молчит, Линус скрывает что бы не
    деморализировать. Жесткая цензура везде, в LKML, в
    рассылках... что бы паники не создавать. Представь реакцию,
    Марк, когда населению скажут что рядом, в интернетах
    живет 6000 зомби которые поедают убунтушников?
    Представил? Вот и молчат все в тряпочку, а редхатовские
    зомби жрут. И продвигаются все дальше в миддлвэр. Уже в
    Ланчпаде пару словили, а говорили коммьюнити мол меритократичное.

    Беда, Марк, беда.


.. |image0| image:: https://cdn.rawgit.com/ruzickap/linux.xvx.cz/gh-pages/files/systemd_cheatsheet/systemd_cheatsheet.svg
   :target: http://linux.xvx.cz/2014/06/systemd-cheatsheet.html
