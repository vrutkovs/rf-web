.. title: Docker напрягся.
.. slug: docker-напрягся
.. date: 2015-05-06 14:54:13
.. tags: docker, coreos, google, redhat, vmware, rkt, bsd
.. category:
.. link:
.. description:
.. type: text
.. author: Peter Lemenkov

Docker, упорно пытающийся вылезти за пределы "запустить три версии руби
одновременно", возможно переживает сильнейший удар. Три больших игрока
объединились против него. На недавно прошедшем `CoreOS
Fest <https://coreos.com/fest/>`__ Google, Red Hat, и VMware `официально
поддержали <https://coreos.com/blog/appc-gains-new-support/>`__ стандарт
`App Container <https://github.com/appc>`__ в своих продуктах. Этот
стандарт уже поддерживается в собственном продукте CoreOS,
`Rocket </content/coreos-отказывается-от-btrfs>`__, а теперь будет
поддерживаться и другими компаниями и коммьюнити.

Архитектурно, `повторимся </content/Безопасность-docker-будущее>`__,
Docker ничем похвалиться не может - это еще один из продуктов, чья
популярность возникла впопреки. Это вас не должно удивлять - дело в том,
что зачастую делать правильно сложнее, чем неправильно. Да, если делаешь
не по инструкции, то результат может быть плохой. А что если он будет
хороший? О плохих историях почти никто не рассказывает (что
рассказывать-то? сам дурак, сделал неправильно), да и вообще, плохое
возникает реже, чем хорошее. Вот по блогам и форумам кочуют
прекраснодушные рассказчики с их "отключил SELinux, и ничего!",
"поставил венду, и не ослеп", "не учил математику, и не дурее других".

И до Docker были контейнеры (LXC, Parallels, и т.п.), но его
разработчики сделали одно простое, но умное решение - ставка на
начинающих, и поддержка популярного у них дистрибутива, одновременно
предложив рабочее решение, обходящее все его недостатки. Тем не менее,
остались открытыми вопросы безопасности, управления сетью (хотя в
последнее время управление сетью в Docker начало улучшаться, как
благодаря работе независимых разработчиков, так и `благодаря усилиям их
команды <https://blog.docker.com/2015/04/docker-networking-takes-a-step-in-the-right-direction-2/>`__),
зависимостей между процессами (а зависимости никуда не делись, как ни
радуйся тому, что можно "запустить три версии руби одновременно"),
управление хранилищем, декомпозиция толстого бинарника на работающие
независимо компоненты (как это было сделано в systemd). Разумеется, со
временем, у Docker будет решение всех этих и прочих проблем, но нашими
друзьями из CoreOS, как нам кажется, было предложено архитектурно
гораздо более правильное решение. Которое, теперь, еще и будет
стандартизировано.

Стандартизация App Container, и управление оргвопросами коммьюнити будет
осуществляться на демократической модели, с помощью выбираемых по
совокупности заслуг участниками (как это делается почти везде в успешных
OpenSource-проектах). Пока проектом управляют пятеро человек - `Charles
Aylward <https://twitter.com/cdaylward>`__ из Twitter, `Vincent
Batts <https://github.com/vbatts>`__ из Red Hat, `Tim
Hockin <https://github.com/thockin>`__ из Google, и `Brandon
Philips <https://github.com/philips>`__ и `Jonathan
Boulle <https://github.com/jonboulle>`__ из CoreOS.

Интересно, что стандарт уже поддерживается и на FreeBSD, в продукте
`Jetpack <https://github.com/3ofcoins/jetpack>`__.

.. image:: https://regmedia.co.uk/2014/12/01/container_disaster.jpg
   :align: center
   :target: http://www.theregister.co.uk/2015/05/05/coreos_fest_roundtable

.. class:: align-center

**Может уже пора сбегать?**
