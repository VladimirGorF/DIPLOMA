# DIPLOMA
This is my diploma project as the end of study  in Geek Brains.

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
Нажимаем Download Wordpress 6.1.1 и затем копируем все файлы из скачанной папки WORDPRESS. Заходим в наши Приложения на компьютере, находим там папку MAMP, открываем в нем папку htdocs, в ней создаем папку wordpress.dev и вставляем туда все наши файлы(поместив таким образом WORDPRESS в конкретный проект, находяшийся на нашем условном сервере). Затем возвращаемся на localhost и нажимаем My Website. Сервер даст нам выбор Index OF с указанием наших проектов , находящихся в нашей папаке. Выбираем нужный. Затем нужно будет вводить учетные данные в WORD PRESS.

Перед этим нам следует узнать о следующем.

Имя БД
Имя пользователя базы данных
Пароль к базе данных
Хост БД
Префикс таблиц (если вы хотите запустить более чем один WordPress на одной базе)
Эта информация требуется для создания файла wp-config.php. Если по какой-то причине автоматическое создание файла не удалось, не волнуйтесь. Всё это предназначено лишь для заполнения файла настроек. Вы можете просто открыть wp-config-sample.php в текстовом редакторе, внести вашу информацию и сохранить его под именем wp-config.php. 

Но перед этим, вернемся на наш localhost, выберем наверху вкладку TOOLS и затем PhpMyAmin.
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
Мы выбрали цель - создание работающего сайта в WEB, определились с инструментарием WORPDPRESS с использованием локального сервера MAMP. Произвели необходимую установку серверов и стартовый запуск WORDPRESS, убедились в работоспособности системы.
Таким образом мы закончили подготовку к основной работе и можем перейти непосредственно к созданию сайта.

.
.
.
.
.

2.1 Создание сайта. Первые шаги.

В связи с тем, что на момент проектирования у нас отсутствует точное понимание того, как должен выглядеть сайт  и какой именно контент там будет размещен, мы будем придерживаться итерационной модели создания этого продукта, изменяя в процессе наши меню, добавляя и трансформируя страницы, виджеты, записи и тп. В нашем случае это довольно просто, так как и исполнитель и заказчик у нас в одном лице и все решения принимаются мгновенно.

В папке wordpress.dev\wp-content\themes создаем свою папку Sparrow, она будет являться темой сайта(внешний вид), и создаем в нем файл style.css и screenshot.png. Первый нужен для подключения стилей, и чтобы WORDPRESS (далее везде WP), не считал нашу тему поврежденной и показал нам ее в своем меню в WP(Внешний вид\Темы). Второй нужен как заставка нашей темы,  WP увидит ее в папке и подгрузит самостоятельно. Также создаем базовый файл - страницу:  index.php. 
<img width="2048" alt="Снимок экрана 2023-05-16 в 13 35 03" src="https://github.com/VladimirGorF/DIPLOMA/assets/110591063/0893c3f1-158f-4302-835f-5413e24cc330">


Далее идем на сайт underscores.me - генератор тем для WordPress  и генерируем там нашу тему sparrow, которой мы будем пользоваться как базовым шаблоном при созданиии нашего собственного сайта.

Теперь переходим непосредственно к WORDPRESS.
В меню WP заходим в раздел  "Все записи" и через "добавить запись" создаем три новые новостные записи: Новость1, Новость2, Новость3.  Заполняем их произвольным тестовым текстом , без рубрик и меток, котрые мы создадим далее. Разрешаем отклики и комментарии, установив соответсвующие галочки.
<img width="2048" alt="Снимок экрана 2023-05-16 в 16 59 58" src="https://github.com/VladimirGorF/DIPLOMA/assets/110591063/b8b65ce8-2075-4add-93f6-4fb3eacfc0b4">

Далее проходим в меню "Рубрики" и создаем Рубрику1 и Рубрику2, утсановив им соответсвующие ярлыки без родительских рубрик.
<img width="2048" alt="Снимок экрана 2023-05-16 в 17 06 18" src="https://github.com/VladimirGorF/DIPLOMA/assets/110591063/74d844e4-d609-4626-8ad3-f71d7437e105">

По аналогии в меню Метки, создаем три новые метки: Life, Sport и WorkPlace.
<img width="2048" alt="Снимок экрана 2023-05-16 в 18 14 44" src="https://github.com/VladimirGorF/DIPLOMA/assets/110591063/47bd3130-cf91-4221-85aa-d9cfc23e469d">


В меню Страницы через  "Добавить новую" добавляем несколько страниц: Главная, Гражданство РФ, Гражданам других государств, Гражданам СССР И СНГ, Миграционный учет, Патент, Разрешение на работу, Помощь в трудоустройстве, Портфолио, Контакты.
<img width="2048" alt="Снимок экрана 2023-05-16 в 18 15 56" src="https://github.com/VladimirGorF/DIPLOMA/assets/110591063/28453b63-0eae-4dc9-8b87-35779b4d3e8d">

Также в разделе Плагины, нам необходимо установить Advanced Custom Fields для создания собственных таксономий, а также установим Contact Form 7 для получения удобных контактных форм на нашем сайте. А также добавим еще один плагин Flamingo, для перехвата входящих сообщений с сайта, оставляемых пользователеми, потому что они должны отправляться на контактную почту администратора, но если будет сбой, то нигде не сохранятся. Flamingo помогает избежать этой проблемы, сохраняя все сообщения с сайта.
<img width="2048" alt="Снимок экрана 2023-05-16 в 18 17 15" src="https://github.com/VladimirGorF/DIPLOMA/assets/110591063/123f2913-1790-4457-a762-0e8959dd4c9e">


2.2 Создание сайта. Функции.

 Для полноценного использования возможностeй WORDPRESS откроем нашу папку с темой  Sparrow в которой ранее мы создавали файл со стилями, базовую страницу и скриншот. Добавим в нее еще один очень важный файл functions.php, в котором благодаря встроенному функционалу WP мы сможем подключить нужные нам стили, дополнительные меню, подключать сайдбары, создавать собственные темы и таксономии, шорткоды, и различные действия.
 
 2.2.1 Шрифты и стили.

 Начнем с подключения шрифтов и стилей. Для этого нам необходимо создать функции 'style_theme' и 'scripts_theme'. 
 
 function style_theme(){
 
    wp_enqueue_style('style', get_stylesheet_uri());
    wp_enqueue_style('default', get_template_directory_uri() . '/assets/css/default.css');
    wp_enqueue_style('layout', get_template_directory_uri() . '/assets/css/layout.css');
    wp_enqueue_style('media-queries', get_template_directory_uri() . '/assets/css/media-queries.css');
    wp_enqueue_style('fonts', get_template_directory_uri() . '/assets/css/fonts.css');
}

function scripts_theme(){

    wp_enqueue_script('jquery.flexslider', get_template_directory_uri() . '/assets/js/jquery.flexslider.js' );
    wp_enqueue_script('doubletaptogo', get_template_directory_uri() . '/assets/js/doubletaptogo.js' );
    wp_enqueue_script('init', get_template_directory_uri() . '/assets/js/init.js' );
}
 
 Под эти функции мы создадим хуки в момент срабатывания которых будут вызваться наши функции и подключаться стили и темы.
 
add_action('wp_enqueue_scripts', 'style_theme');

add_action('wp_footer', 'scripts_theme');



 2.2.2 Название сайта и логотип.
Для того чтобы выводить на страницах назавание сайта будем использовать специальные функции WP. В header.php напишем следущий код:

 <div class="logo">
    <a href="<?php echo home_url(); ?>">
        <div>
            <?php bloginfo('name'); ?>
        </div> 
        <img alt="" src="images/myiPoto2.png">
    </a>
</div>

Функция php echo home_url() - будет всегда выдавать нам домашний адрес стартовой страницы. Мы обернули ее в тег 'a' чтобы она была рабочей ссылкой на нее.
Функия php bloginfo('name') - будет возваращать нам название сайта, которое мы можем менять в админке WP. 
Заходим в меню WP - Внешний вид/настроить/свойства сайта и в поле "Название сайта" пишем наше название RossVisa. 
В этом же меню мы можем установить иконку сайта, которая будет показываться при поиске нашего сайта в поисковых системах.

<img width="1728" alt="Снимок экрана 2023-08-23 в 12 22 56" src="https://github.com/VladimirGorF/DIPLOMA/assets/110591063/188ff68c-a90b-4d7e-84f2-28166074d154">


2.2.3 Меню.
Далее мы создадим функцию, позволяющую зарегистрировать нам меню сайта, добавим в нее реализацию добавления изображений  в определенных типах записей, фильтр для вывода подсказки "Читать далее", 

function theme_register_nav_menu() { 

	register_nav_menu( 'top', 'Меню в шапочке' );
	add_theme_support( 'title-tag' );
	// создаем в WP в записях возможность добавления картинок
	add_theme_support( 'post-thumbnails', array( 'post', 'portfolio' ) );  // в скобках пишем в каких типах записей можно добавлять картинки
	// фильтра для вывода "Читать далее"
	add_filter( 'excerpt_more', 'new_excerpt_more' );
	function new_excerpt_more( $more ){
	global $post;
	return '<a href="'. get_permalink($post). '">  читать дальше...</a>';  
}
}
 
Чтобы все это заработало, создаем действие, срабатывающее в момент 'after_setup_theme'.

add_action( 'after_setup_theme', 'theme_register_nav_menu' );


Заведем  меню в админке WP. Внешний вид\ Меню \Создать новое меню. Назовем его 'Верхнее Меню'  и установим область отображения 'Меню в шапочке'. Нажимаем создать меню. 
![Снимок экрана 2023-08-23 в 20 44 30](https://github.com/VladimirGorF/DIPLOMA/assets/110591063/f79a2f48-0c55-405e-abd2-67e0380aa982)

После этого к меню применятся нужные стили и оно выстроится в строчку, как и нужно.

Далее добавим еще несколько страниц в наше меню. 
<img width="1728" alt="Снимок экрана 2023-08-23 в 13 11 55" src="https://github.com/VladimirGorF/DIPLOMA/assets/110591063/0d5edc66-6a05-4bd8-bb05-063a81b94c59">

И после публикации наше меню уже выглядит вполне весомо:
<img width="1728" alt="Снимок экрана 2023-08-23 в 13 17 02" src="https://github.com/VladimirGorF/DIPLOMA/assets/110591063/62344bbe-791a-45bd-8cca-cdee8158579d">

Далее, для того чтобы выбранная страниц а в нашем меню подсвечивалась необходимо откорректировать стили css. Идем в   assets/css/layout.css, находим в нем код "ul#nav li.current a { color: #fff; }" и вместо "current" пишем "current-menu-item". Проверяем работу подсветки зайдя в страничку Контакты и видим, что она подсвечивается теперь белым цветом:
<img width="1728" alt="Снимок экрана 2023-08-23 в 13 28 12" src="https://github.com/VladimirGorF/DIPLOMA/assets/110591063/b2c13ed6-474e-40e1-af8a-99efb8988200">


2.2.4 Вложенные страницы.
Теперь для одной из наших страниц создадим вложенные страницы. Для этого зайдем в раздел Внешний вид\Меню. Странички 'Гражданам других государств' и 'Гражданам СССР И СНГ' сдвинем на одну табуляцию вправо. 

<img width="1728" alt="Снимок экрана 2023-08-23 в 19 00 49" src="https://github.com/VladimirGorF/DIPLOMA/assets/110591063/2c0cf416-3b58-4d5d-8823-f601c99ef31b">

Таким образом они станут дочерними для вышестоящей страницы 'Гражданство РФ' и при наведении курсора на родительскую страницу будет выскакивать подменю с двумя дочерними страницами.  Стандартое меню, которое у нас было в header.php изначально, необходимо удалить, чтобы было только наше новое.

<img width="1728" alt="Снимок экрана 2023-08-23 в 19 01 55" src="https://github.com/VladimirGorF/DIPLOMA/assets/110591063/616b1f12-0687-4742-8510-52c9000d915d">


Теперь зарегистрируем еще 2 меню в нашей функции function theme_register_nav_menu() добавим еще две строчки в файле functions.php:

register_nav_menu( 'footer', 'Меню в подвале' );

register_nav_menu( 'page_menu_top', 'Меню в страничке page' );

И затем в footer.php page.php добавим: 

            <nav id="footer-nav">
                <?php wp_nav_menu(array(
                  'theme_location'  => 'footer',
                  'container'       => null,
                  'menu_class'      => 'footer-nav',
                  'menu_id'         => 'footer-nav'
                ));?>
            </nav> 

Заведем   это меню в админке WP. Внешний вид\ Меню \Создать новое меню. Назовем его 'Меню в подвале'  и установим область отображения 'Меню в подвале'. Нажимаем создать меню. Далее добавим еще несколько страниц в наше меню. 
После этого к меню применятся нужные стили и оно выстроится в строчку, как и нужно.
<img width="1728" alt="Снимок экрана 2023-08-23 в 20 52 13" src="https://github.com/VladimirGorF/DIPLOMA/assets/110591063/bdc4aac9-019c-4235-ba64-8760eedb0b5f">

Теперь закомментируем бывшее меню:
     <!-- <ul class="footer-nav">
		<li><a href="#">Home.</a></li>
              	<li><a href="#">Blog.</a></li>
              	<li><a href="#">Portfolio.</a></li>
              	<li><a href="#">About.</a></li>
              	<li><a href="#">Contact.</a></li>
               <li><a href="#">Features.</a></li>
	</ul> -->

и посмотрим как оно выглядит у нас на сайте.
<img width="1728" alt="Снимок экрана 2023-08-23 в 20 56 03" src="https://github.com/VladimirGorF/DIPLOMA/assets/110591063/51b7e03a-883e-4aca-b74f-7f2b5615ff48">


А в header-page.php добавим:  

	    <nav id="footer-nav">
                <?php wp_nav_menu(array(
                  'theme_location'  => 'page_menu_top',
                  'container'       => null,
                  'menu_class'      => 'footer-nav',
                  'menu_id'         => 'footer-nav'
                ));?>
            </nav> 

Заведем  это меню также в админке WP. Внешний вид\ Меню \Создать новое меню. Назовем его 'Меню-page'  и установим область отображения 'Меню в страничке page'. Нажимаем создать меню. Далее добавим еще несколько страниц в наше меню. 
<img width="1728" alt="Снимок экрана 2023-08-23 в 21 00 42" src="https://github.com/VladimirGorF/DIPLOMA/assets/110591063/d498f15f-1599-42bd-95f3-843dc8250344">


После этого к меню применятся нужные стили и оно выстроится в строчку, как и нужно.
на страничке page.php вызываем уже по другому наш header для страницы page:
<?php get_header('page'); ?>

Теперь првоеряем меню на странице контакты.
<img width="1728" alt="Снимок экрана 2023-08-23 в 21 09 19" src="https://github.com/VladimirGorF/DIPLOMA/assets/110591063/905c3340-3df7-4bb5-a10c-096a6a2ce64d">








Далее создадим функцию для регистрации собственного типа Portfolio. Установим 'menu_position'  => 4 , очередность вывода в меню WP нового типа.  И немного расширим 'supports'  => [ 'title', 'editor','author','thumbnail', 'excerpt' ], чтобы изспользовать возможности 'thumbnail' и 'excerpt'(частичное вопроизведение). 
Сразу укажем параметр 'taxonomies'  => ['skills'], поскольку мы ниже будем регистрировать и его тоже.

function register_post_types(){

	register_post_type( 'portfolio', [
		'label'  => true,
		'labels' => [
			'name'               => 'Портфолио', // основное название для типа записи
			'singular_name'      => 'Портфолио', // название для одной записи этого типа
			'add_new'            => 'Добавить Портфолио', // для добавления новой записи
			'add_new_item'       => 'Добавление Портфолио', // заголовка у вновь создаваемой записи в админ-панели.
			'edit_item'          => 'Редактирование Портфолио', // для редактирования типа записи
			'new_item'           => 'Новое Портфолио', // текст новой записи
			'view_item'          => 'Смотреть Портфолио', // для просмотра записи этого типа.
			'search_items'       => 'Искать Портфолио', // для поиска по этим типам записи
			'not_found'          => 'Не найдено Портфолио', // если в результате поиска ничего не было найдено
			'not_found_in_trash' => 'Не найдено в корзине', // если не было найдено в корзине
			'parent_item_colon'  => '', // для родителей (у древовидных типов)
			'menu_name'          => 'Портфолио', // название меню
		],
		'description'            => '',
		'public'                 => true,
		// 'publicly_queryable'  => true, // зависит от public
		// 'exclude_from_search' => true, // зависит от public
		// 'show_ui'             => true, // зависит от public
		// 'show_in_nav_menus'   => true, // зависит от public
		'show_in_menu'           => true, // показывать ли в меню админки
		// 'show_in_admin_bar'   => true, // зависит от show_in_menu
		'show_in_rest'        => true, // добавить в REST API. C WP 4.7
		'rest_base'           => null, // $post_type. C WP 4.7
		'menu_position'       => 4,
		'menu_icon'           => null,
		//'capability_type'   => 'post',
		//'capabilities'      => 'post', // массив дополнительных прав для этого типа записи
		//'map_meta_cap'      => true, // Ставим true чтобы включить дефолтный обработчик специальных прав
		'hierarchical'        => false,
		'supports'            => [ 'title', 'editor','author','thumbnail', 'excerpt' ], // 'title','editor','author','thumbnail','excerpt','trackbacks','custom-fields','comments','revisions','page-attributes','post-formats'
		'taxonomies'          => ['skills'],
		'has_archive'         => false,
		'rewrite'             => true,
		'query_var'           => true,
	] );

}

Вызываться это все будет действием в мемент срабатывания 'init' :
add_action( 'init', 'register_post_types' );


Далее зарегистрируем таксономию "skills" путем написания функции ниже с указанием нужных нам параметров и названий полей.

function create_taxonomy(){

	// список параметров: wp-kama.ru/function/get_taxonomy_labels
	register_taxonomy( 'skills', [ 'portfolio' ], [
		'label'                 => '', // определяется параметром $labels->name
		'labels'                => [
			'name'              => 'Навык',
			'singular_name'     => 'Навык',
			'search_items'      => 'Search Навык',
			'all_items'         => 'All Навык',
			'view_item '        => 'View Навык',
			'parent_item'       => 'Parent Навык',
			'parent_item_colon' => 'Parent Навык:',
			'edit_item'         => 'Edit Навык',
			'update_item'       => 'Update Навык',
			'add_new_item'      => 'Add New Навык',
			'new_item_name'     => 'New Навык Name',
			'menu_name'         => 'Навык',
			'back_to_items'     => '← Назад в Навык',
		],
		'description'           => 'Навыки, которые использовались в работе над проектами', // описание таксономии
		'public'                => true,
		'publicly_queryable'    => null, // равен аргументу public
		'hierarchical'          => false,
		'rewrite'               => true,
	] );
}

Вызовем это все действием add_action( 'init', 'create_taxonomy' );


Теперь зарегистрируем наш сайдбар.

function register_my_widgets(){   

	register_sidebar( array(
		'name'          => "Left Sidebar",
		'id'            => "left_sidebar",
		'description'   => 'Левый  сайдбар',
		'before_widget' => '<div class="widget %2$s">',
		'after_widget'  => "</div>\n",
		'before_title'  => '<h5 class="widgettitle">',
		'after_title'   => "</h5>\n",
		'before_sidebar' => '', // WP 5.6
		'after_sidebar'  => '' // WP 5.6
	) );
}

Подключим его: add_action( 'widgets_init', 'register_my_widgets' );







2.500 Создание сайта. Работа со страницами.











4. Источники.
Полезные ссылки:  
underscores.me - генератор тем для WordPress
wp-kama.ru руководство по использованию функций  в WORDPRESS














