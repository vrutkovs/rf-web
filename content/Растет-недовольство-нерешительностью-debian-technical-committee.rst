.. title: Растет недовольство нерешительностью Debian Technical Committee
.. slug: Растет-недовольство-нерешительностью-debian-technical-committee
.. date: 2014-01-18 01:49:23
.. tags: debian, systemd, upstart, canonical, spotify
.. category:
.. link:
.. description:
.. type: text
.. author: Peter Lemenkov

`Мнущееся у входа и никак не решающееся войти
</content/Печальные-новости-о-debian>`__ коммьюнити Debian уже полгода-год
выбирает - systemd или Upstart. За systemd стоит большое коммьюнити
разработчиков, техническое превосходство и инновации, которых так не хватает
Debian. За Upstart стоит единственный корпоративный спонсор Debian (нанял
несколько человек из Debian - другие не сделали и этого), и попытка укусить
руку дающую может привести к `очень тяжелым
<https://www.linux.org.ru/news/bsd/10060466>`__ `последствиям
<https://www.linux.org.ru/news/bsd/10060644>`__. Выбор непрост, и `обсуждение
затянулось далеко за три тысячи сообщений
<http://bugs.debian.org/cgi-bin/bugreport.cgi?bug=727708>`__.

Когда почти все сложилось в пользу Upstart, произошли два события. Во-1 в
состав комитета `вошел Keith Packard
</content/Новости-systemd-за-прошедший-месяц-полтора>`__, а он `утилитарно и
технически грамотно смотрит на вещи </content/systemd-и-wayland>`__. Во-2
`Bdale Garbee <https://en.wikipedia.org/wiki/Bdale_Garbee>`__ предложил
вернуться в самое начало, сообщив, что `он считает, что мэйнтейнеры должны
поддерживать сразу несколько init-систем
<http://bugs.debian.org/cgi-bin/bugreport.cgi?msg=3220;bug=727708>`__.

.. image:: http://raphaelhertzog.com/files/2011/03/bdale.jpg
   :align: center
   :width: 300px
   :target: https://en.wikipedia.org/wiki/Bdale_Garbee

.. class:: align-center

**Работайте, мэйнтейнеры, солнце еще высоко!**

Сложностей в поддержке нескольких init-систем Bdale не видит, как и `жалоб на
искусственную задержку обновления systemd в Debian
<https://lists.debian.org/debian-ctte/2013/12/msg00306.html>`__, мэйнтейнеры
которого вынуждены ждать, пока разработчики Upstart накопипастят еще фич из
systemd, которые недавно теми и критиковались ("комбайн", "не-юниксвэй" и
т.п.).

Это уже не могло понравиться никому. В конце концов, чтоб ничего не решать, для
этого есть целое Debian Community, некоторые участники которого верят, что
`Linux Is About Choice <http://islinuxaboutchoice.com/>`__, а Debian ctte как
раз и позвали, чтоб решить хоть что-то. Инженер Canonical и разработчик
systemd, `Martin Pitt <https://plus.google.com/107564545827215425270/about>`__,
возмутился и в своей ленте Google+ призвал их определяться, `или туда - или
сюда <https://plus.google.com/107564545827215425270/posts/PiX3Y9mmNs3>`__, *"а
то это ваше туда-сюда меня раздражает!"*.

Почти сразу не мучать кота призвали инженеры Spotify. `В их коллективном письме
<http://bugs.debian.org/cgi-bin/bugreport.cgi?msg=3546;bug=727708>`__ они
подчеркивают, что управляют одной из крупнейших Debian-инсталляций, которая
включает одних только физических машин пять тысяч штук, не считая многих тысяч
виртуальных машин с Debian, и призывают перейти на systemd целиком, т.к. он
проще, и лучше приспособлен для больших сложных систем.

К их письму `присоединился
<http://bugs.debian.org/cgi-bin/bugreport.cgi?msg=3571;bug=727708>`__ простой
сисадмин одной из полутора сотен Tier-2 вычислительных сетей для Large Hadron
Collider и также призвал перейти на systemd, как однозначного технического
лидера и, что также немаловажно, гораздо более открытого и свободного проекта,
чем Upstart. Он припомнил Canonical их CLA, то, что они забрасывают проекты,
когда теряют к ним интерес (история угасания bzr им еще не раз аукнется), и их
последние движения в сторону от коммьюнити (Mir vs. Wayland). В противовес
Canonical он поставил традиционную прозрачность и открытость Red Hat для
коммьюнити (это интересно, но у коммьюнити нет рычагов управления Ubuntu, и
решения принимает единолично Canonical).

Спектакль немного затягивается, и решение будет сложным. Можно наверное
начать гадать, кого из крупных корпоративных пользователей Debian
потеряет, как из-за неуверенности в перспективах проекта, управляемого
настолько плохо (и так компаний, предоставляющих техподдержку у них
почти нет, а будет еще меньше), так и из-за позднего решения, неважно
уже какого, но уже точно с которым многие будут несогласны.
