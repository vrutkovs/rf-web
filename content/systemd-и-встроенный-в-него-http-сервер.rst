.. title: systemd и встроенный в него http-сервер
.. slug: systemd-и-встроенный-в-него-http-сервер
.. date: 2012-10-09 11:59:06
.. tags:
.. category:
.. link:
.. description:
.. type: text
.. author: Peter Lemenkov

**Это архивная статья**


В рассылке Fedora-Devel интересная дискуссия о функционале systemd. Наш
товарищ, инженер Red Hat и участник Fedora Project и Gentoo Linux (наши
есть и в вашей гентушечке!), `Petr Písař <http://xpisar.wz.cz/>`__, с
изумлением обнаружил, что `systemd версии 194 теперь включает web-сервер
и библиотеку для создания
QR-кодов <https://thread.gmane.org/gmane.linux.redhat.fedora.devel/169082>`__.

Петр нисколько не сомневается в том, что web-сервер очень нужен в
современной системе загрузки, но он просто хотел бы чтобы ему объяснили,
зачем он там, т.к. сам он не может это понять. В комментариях участники
Fedora начали высказывать свои догадки и предположения. Так, методом
"обратного объяснения", порой вырабатываются руководящие принципы
разработки Fedora. Заодно решается вопрос, можно-ли это выключить по
умолчанию или не устанавливать вовсе.

