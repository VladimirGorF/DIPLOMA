# DIPLOMA
This is my  diploma project as the end of study of Geek Brains teaching.

 Оглавление:
 1. Цели и Задачи проекта. 1.1 Выбор инструментов и подготовка.
 
 2. Создание сайта.
 
 3. Итоги
 
 4. Источники
 
 
 
 1.
 Цели и задачи проекта.
 
 Целью проекта является создание работающего сайта в WEB, для помощи людям, желающим получить гражданство Российской Федерации, с учетом соблюдения законов РФ, правил и норм нахождения в стране. В целях реализации поставленных целей необходимо будет решать задачи связанные с установкой необходимого программного обеспечения, разработкой стрктуры сайта, его наполнением, подключением к WEB и запуском в продакшн.
 
 1.1. Подготовка.
 
 Работа выполняется на базе MAC OS Ventura версия 13.2.1. Будем устанавливать WORPDPRESS с использованием локального сервера MAMP.
 Краткая справка из Википедии:
 "WordPress — свободно распространяемая система управления содержимым сайта с открытым исходным кодом; написана на PHP; сервер базы данных — MySQL; выпущена под лицензией GNU GPL версии 2. Сфера применения — от блогов до достаточно сложных новостных ресурсов. Встроенная система «тем» и «плагинов» вместе с удачной архитектурой позволяет конструировать проекты широкой функциональной сложности."
 
Мы используем локальный сервер MAMP, потому что программе WORDPRESS необходима база данных, например MySQL для функционирования.

Что содержит в себе MAMP:

MySQL
MAMP supports MySQL 5.7

Apache
The leading HTTP server is integrated

Nginx
Also the Apache alternative is included

PHP
The leading scripting language in web development incl. the new version PHP 8


НА сайте (https://www.mamp.info/en/mac/) находим бесплатную версию, она называется просто MAMP, скачиваем и устанавливаем ее.
<img width="2048" alt="Снимок экрана 2023-03-19 в 13 07 10" src="https://user-images.githubusercontent.com/110591063/226168402-d1da126b-63cf-4ba1-b0c2-faf852448f2b.png">

ВАЖНО: при скачивани необходимо выбрать соответствующий вашему компьютеру тип (у меня это MAC Intel *86 CPU). Сама установка проходит без подводных камней, со всем соглашеаемся и везде жмем далее. Как итог успешной установки, будет предложено переместить в корзину установщик(он нам более не потребуетс), также соглашаемся. 
Теперь у нас в Launchpad появятся две иконки с изображением синего и серого слоника. Наш бесплатный, потому серый. Называется просто MAMP. Запускаем его.
Кнопочкой START запускаем наш сервер(можно выбрать что вам более нарвится APACHE or Nginx).  Запустившись, MAMP октроет нам в браузере нашу стартовую страничку http://localhost:8888/MAMP/ .

Далее устанавливаем WORDPRESS.  Для этого прееходим на сайт https://wordpress.org/ .
<img width="2048" alt="Снимок экрана 2023-03-19 в 13 31 19" src="https://user-images.githubusercontent.com/110591063/226169508-f0a29285-27ad-4ad7-85bb-728da7e8a710.png">

Заходим в GET WORDPRESS в верхнем правом углу. Затем выбираем траекторию установки: "Download and install it yourself" или "Set up with a hosting provider". Второй вариант обозначен как "For anyone looking for the simplest way to start". Поэтому мы выбираем первый вариант, для тех, кто не ищет легких путей. 
Нажимаем Download Wordpress 6.1.1 и затем копируем все файлы из скачанной папки WORDPRESS. Заходим в наши Приложения на компьютере, находим там папку MAMP, открываем в нем папку htdocs, в ней создаем папку wordpress.dev и вставляем туда все наши файлы(поместив таким образом WORDPRESS в конкретный проект, находяшийся на нашем условном сервере). Затем возвращаемся на localhost и нажимаем My Website. Сервер даст нам выбор Index OF с указанием наших проектов , находящихся в нашей папаке. Выбираем нужный. Затем нужно будет вводить учетные данные в WORD PRESS, но перед этим, вернемся на наш localhost, выберем наверху вкладку TOOLS и затем PhpMyAmin.
Таким образом мы окажемся в управлении нашими базами данных.  
Создадим новую базу данных, которую затем внесем в графу Database Name в WordPress. В моем случае создалась база "db".
Далее идем во вкладку "Привилегии" и создаем нового пользователя, вводя его имя и пароль. Далее предоставляем ему все Привилегии уровня базы данных поставив нужную галочку.
<img width="2048" alt="Снимок экрана 2023-03-19 в 14 03 49" src="https://user-images.githubusercontent.com/110591063/226171174-b6c8ef60-3eb9-47e8-b379-05b5b36b1428.png">

Теперь у нас есть все, что требуется для запуска установки WORDPRESS. Заходим на вкладку My Website на localhost и заполняем все данные. Хост и префикс оставляем как есть.
Вот что получилось в итоге в нашем случае:
<img width="2048" alt="Снимок экрана 2023-03-19 в 14 12 31" src="https://user-images.githubusercontent.com/110591063/226171571-7d689473-38a9-41ce-bb4a-4a21e6beb9ad.png">
Подтверждаем и запускаем инсталляцию. 
Затем снова заполняем форму устанавливая Заголовок для нашего сайта и вводя нового пользователя и пароль уже для WordPress. 
<img width="2048" alt="Снимок экрана 2023-03-19 в 14 22 17" src="https://user-images.githubusercontent.com/110591063/226171984-700ed257-284c-4183-8520-18d99d75c004.png">
Далее просто заходим используя нового пользователя и пароль.

Затем вводим в браузере http://localhost:8888 и попадаем в наш проект-сайт.
<img width="2048" alt="Снимок экрана 2023-03-19 в 14 25 58" src="https://user-images.githubusercontent.com/110591063/226172186-99ffb85a-61d0-4718-a162-3ab42a2d1a18.png">

Администрирование остается у нас на [http://localhost:8888/wp-admin/ ](http://localhost:8888/wordpress.dev/wp-admin/).

1.3.
Итоги главы :
Мы выбрали цельь - создание работающего сайта в WEB, определились с инструментарием WORPDPRESS с использованием локального сервера MAMP. Произвели необходимую установку серверов и стартовый запуск WORDPRESS, убедились в работоспособности системы.
Таким образом мы закончили подготовку к основной работе и можем перейти непосредственно к созданию сайта.



2. Создание сайта.













4. Источники.
Полезные ссылки:  
underscores.me - генератор тем для WordPress
wp-kama.ru руководство по использованию функций














