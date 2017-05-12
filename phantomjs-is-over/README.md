# PhantomJS всё?
*Расшифровка интервью с [Виталием Слободиным](https://github.com/Vitallium), автором [PhantomJS](http://phantomjs.org). Интервью ведут [Вадим Макеев](https://github.com/pepelsbey/) и [Алексей Симоненко](https://github.com/meritt) в рамках [65-го выпуска подкаста «Веб-стандарты»](https://soundcloud.com/web-standards/episode-65).*


**Вадим:**
Когда мы записывали последний выпуск, [пришла неожиданная новость, что PhantomJS всё](https://groups.google.com/forum/#!msg/phantomjs/9aI5d-LDuNE/5Z3SMZrqAQAJ), и, может быть, мы немножечко увлеклись и драматизировали, но мы увидели твой анонс, что ты отходишь от должности мейнтейнера PhantomJS. Можешь ты немного рассказать: откуда это всё взялось, почему так произошло и что будет дальше с PhantomJS?

**Алексей:**
А можно я сразу перебью и спрошу главный вопрос: PhantomJS 2.5 в итоге выйдет или нет? Ну, понятно, может быть без твоего участия, но его стоит ожидать или нет? А потом уже можешь на вопросы Вадима отвечать.

**Виталий:**
Думаю, я могу совместить ответ и ответить сразу на оба ваших вопроса: нет, релиза 2.5 не будет. Почему? Отвечаю на вопрос Вадима: начиная где-то с версии 1.9.7 PhantomJS мы долго думали всем нашим маленьким составом из трёх человек, что мы будем делать дальше. На тот момент PhantomJS версии 1 использовал библиотеку Qt 4, там же уже была Qt 5, и было принято решение портировать всю нашу кодовую базу на Qt 5 - это и будет тот самый PhantomJS 2. Но, к сожалению, так сложились обстоятельства, что потихонечку, один за одним, вся наша дружная команда начала отходить от дел. То есть просто не было уже свободного времени на продолжение разработки. И вторую версию портировал только я один. Потом так сложилось, что, начиная с версии 2, я, как говорится, тащил весь проект на себе. То есть выпускаемые нами версии, 2.1, 2.1.1, они, по сути, были сделаны только мной одним. Да, была помощь от людей, которые приходили, открывали пулреквесты и помогали, но именно значительные изменения или багфиксы какие-то — таковых на самом деле не было.

Ну и резюмируя всё сказанное: версии 2.5 не будет, к сожалению.

**Алексей:**
В любом случае, тебе огромное спасибо за то, что ты тащил ветку 2, потому что мы ей активно пользуемся.

**Виталий:**
Всегда пожалуйста.

**Вадим:**
Очень интересно, как люди воспринимают такие опенсорсные проекты. Я помню обсуждение Фантома годичной давности, когда все такие: «Ну, господи, ну, сколько можно, уже несколько лет прошло без мажорного релиза. Почему?! Почему эти люди не выпускают следующую версию Фантома?!»

И всё это воспринимается как Windows, как какой-нибудь редактор кода, как Atom. То есть там огромная компания людей сидит, разрабатывает. И мы все никак не можем дождаться, когда они приоритезируют и наконец-то выпустят огромный и классный продукт, которым многие пользуются. А потом выясняется, что там сидело 3 человека, потом остался сидеть один человек и этому человеку не хватает времени, и проект сложный и большой. И странно, что не нашлось людей, готовых спонсировать, готовых самим участвовать. Потому что многие опенсорсные проекты, важные для отрасли (а я нахожу Фантом очень важным для отрасли), они каким-то образом попадают под крыло компаний. То есть компания приводит своих разработчиков и начинает ставить свои бейджики куда-нибудь там в readme, мол «поддерживается компанией X», или каким-то образом компания нанимает сторонних разработчиков, но так или иначе что-то происходит.

Например, у проекта [CSSO](https://github.com/css/csso) логотип Avito сейчас стоит, рядышком логотип Яндекса. У [Autoprefixer](http://autoprefixer.github.io) и [PostCSS](http://postcss.org) компания «Злые Марсиане» спонсирует тем, что [Ситник](http://sitnik.ru/) у них работает и продолжает разрабатывать и помогать, а Фантом как-то вот... не получилось его подобрать. Не знаешь, почему так случилось? Или, может быть, Фантом уже не актуален и надо просто закрыть его и забыть?

**Виталий:**
Вопрос понятен, и, раз уж тут у нас русский подкаст, я могу рассказать немного того, что происходит за сценой, грубо говоря, нашу внутреннюю кухню. Начну по порядку: почему не поднимался вопрос спонсорства? На самом деле, он поднимался и довольно давно, потому что помимо публичных рассылок у нас есть свои собственные, где общаемся только мы, что называется, главные разработчики.

Вопрос о принятии donations (денег, грубо говоря) у нас поднимался, когда мы ещё делали версию 1.8, если я не ошибаюсь, и у нас было 4 голоса, то есть у нас было 4 человека в команде и мы единогласно проголосовали против кнопочки donate. Потому что мы все такого мнения: проект большой, очень большой, на одно закрытое issue открывается сразу 5 новых, и, если мы разрешим людям помогать нам деньгами, мы попадём в такую небольшую зависимость или денежную кабалу. «Ребята, я тут вам деньги отправил, почините, пожалуйста, этот баг». А этот баг мы будем чинить примерно полгода, и не факт, что в результате вообще починим. То есть это сразу бы отсекло такого пользователя от последующих пожертвований нашему проекту.

А почему ни одна большая компания не смогла взять проект под своё крыло, это на самом деле тоже очень больная тема, потому что я знаю, этим проектом пользуются большие компании, начиная от Vmware и заканчивая New York Times. Я думаю, самая главная проблема в том, что порог входа в проект невероятно высок.

Потому что, одно дело, когда есть какая-нибудь популярная библиотека, та же самая CSSO, написанная на JavaScript - популярном языке, и сейчас, что называется, каждый второй человек владеет им, - и прийти, почитать код, немного разобраться в проекте не составит труда. А у нас в проекте на JavaScript только тесты и примеры написаны. Всё остальное у нас - низкоуровневый код. И это я ещё не трогаю самую большую и критичную часть — web-движок, который мы патчили собственными руками. Поэтому я понимаю, почему ни одна компания не хочет брать проект под своё крыло, потому что, если она это сделает, на эту компанию ляжет большой груз ответственности и придётся тащить проект.

**Вадим:**
Я помню историю с [Sass](http://sass-lang.com), когда его с Ruby переписывали на [LibSass](http://sass-lang.com/libsass). Я слышал доклад, по-моему, Криса Эпштейна, про то, как это начиналось. Не знавший C++ человек просто взял и начал его изучать, и написал реализацию каких-то совсем базовых вещей в Sass на C. То есть он просто перевёл какие-то кодовые структуры с одного языка на другой. Заработало. Потом он начал изучать язык больше, больше и больше, и, в итоге, первая версия LibSass была написана довольно-таки неэффективно и плохо. А потом уже присоединились люди, понимавшие, что происходит, и пошло-поехало.

Я к тому, что интерес к проекту был настолько высокий, что даже полные дилетанты в необходимом стеке технологий брались, и что-то делали. Неэффективно, плохо, но оно работало, и, в итоге, мы имеем LibSass, использующийся большинством как основной движок для обработки Sass сейчас, потому что он быстрее, даже не смотря на то, что, по-моему, по фичам он немножко до сих пор отстаёт от Ruby-версии, но, кажется, они уже паритет закрыли по многим возможностям. По крайней мере новые фичи появляются и там, и там одновременно.

**Алексей:**
Да нет, подожди, LibSass по сравнению с Фантомом — это микроб. В Фантоме просто настолько большая база кода... Там же не одна технология используется, правильно, Виталий? Там очень много всего используется, давайте так. И тебе нужно погрузиться во всё это: как должен работать headless-режим, как тебе можно притащить движок браузера, какие проблемы в нём и как тебе это всё обновлять. Огромное количество систем тебе нужно поддерживать. Тебе нужно сделать так, чтобы это работало на Винде, на Маке, на Линуксе, то есть это вот прям совсем не LibSass.

**Виталий:**
Вопрос понятен, и, на самом деле, всё не так страшно, как выглядит. И если ты хочешь контрибьютить PhantomJS, на самом деле, знать, как работает web-движок, тебе вообще не обязательно. Достаточно понять, как работает сам PhantomJS на уровне того, как он загружает JavaScript файл, как он его исполняет, как вообще он командует, грубо говоря, теми самыми нашими headless-страницами.

И я могу ответить на вопрос Вадима, что приходит полный дилетант. Да, такие люди приходили к нам в проект, они писали «я хочу помочь, чем я могу помочь?», мы потом начали выставлять специальные лейблы на GitHub, что называется «good first bug» или «feature», причём мы давали нашу документацию, которой нет на сайте, о том, как вообще работает PhantomJS внутри, чтобы помочь людям разобраться, чтобы они могли помогать нам.

Но, к сожалению, я не знаю почему, но у людей очень быстро пропадал запал. То есть они писали даже на личную почту мне «я хочу помочь, как мне это сделать?». Мы ему бросаем ссылку — вот, посмотри этот баг, он такой маленький, ничего страшного нет, знание web-движка тебе вообще не обязательно, он очень маленький, его можно сделать за недельку, чтобы разобраться и понять. И потом человек пропадал. Всё. И так вот было с каждым.

**Вадим:**
Ну да, видимо, всё не так просто.

**Алексей:**
Да, мне всё-таки кажется, потому что уровень сложности большой, порог входа очень велик.

**Виталий:**
Да, это была очень большая проблема.

**Вадим:**
Ну хорошо, допустим у вас были сложности с тем, чтобы притаскивать к себе WebKit в текущем его состоянии, патчить, чтобы он был совместим, и так далее. Но ведь устройство PhantomJS, насколько я понимаю, такое, что есть, грубо говоря, какой-то API, с которым можно взаимодействовать, а есть собственно движок. И через эту прослойку мы с движком общаемся. А может быть будет проще заменить WebKit на другой движок? И, собственно, мы приходим к проблеме, из-за которой и возник этот вопрос, и даже этот эфир мы собрали потому что [выходит безголовый Chrome](https://www.chromestatus.com/features/5678767817097216), который, может быть, будет лучше? Но он ведь довольно голый, то есть к нему не написаны все обвязки, чтобы с ним было так же удобно общаться, как с Фантомом. Может быть, возможно подменить WebKit на Chromium? И это будет проще, и у компании Google появятся подходящие приоритеты, чтобы участвовать в разработке Фантома. У них там голов хватает.

**Виталий:**
Да, я могу даже сказать о том, что когда мы ещё даже не выпустили бету 2.5, у нас там было огромное количество разнообразных экспериментов по замене движка, по реализации вообще новой версии PhantomJS на основе... есть такая библиотека, называется [Chromium Embedded Framework](https://en.wikipedia.org/wiki/Chromium_Embedded_Framework), предоставляющая прослойку между Хромом и твоим приложением.

То есть экспериментов было огромное количество, мы пытались прийти к некому решению проблемы по замене нашего устаревшего WebKit. С новостью о том, что выходит headless Chrome, многие люди ринулись его пробовать и были немного опечалены, потому что headless Chrome - по сути, тот же самый browser Chrome, устанавливающийся на вашу систему и тянущий все зависимости, которые тянет обычный Chrome. И этот большой список зависимостей не устраивает очень многих людей. Потому что если мы берём какой-нибудь CI-сервер на Linux, многие хотят поставить один маленький бинарный файл с минимумом зависимостей. А поставить туда headless Chrome в его текущем состоянии будет проблематично, там будет очень много зависимостей.

Я могу немножко раскрыть тайну. Мне недавно писал [Пол Айриш](https://www.paulirish.com) о том, что один из инженеров Google как раз-таки делает небольшую обвязочку как в PhantomJS, но которая работает с headless Chrome.

**Вадим:**
Там похожий API используется?

**Виталий:**
Да, вся суть именно в том, чтобы использовать тот же самый API. Он скопировал все наши тесты, лежащие у нас на Гитхабе, и прогоняет, скажем так, своё детище на наших тестах, чтобы достичь 100% проходимости. И на текущий момент, я могу сказать, что там уже проходит процентов 50 тестов, и, самое главное, API полностью совместимо.

**Алексей:**
Звучит здорово, но, как я понимаю, работа над уменьшением зависимостей, чтобы играть с headless-режимом Хрома, пока не планируется?

**Виталий:**
Раз у нас такой вот воскресный день откровений, я могу рассказать, что люди очень быстро заприметили у меня на Гитхабе пустой проект с цитатой из «Звёздный Войн» — [Phantomium](https://github.com/Vitallium/phantomium), начали активно ставить звёздочки. В общем, это будет тот самый новый PhantomJS, работающий на headless Chrome и с минимумом зависимостей.

Если кто-то не знает, то у headless Chrome есть ещё такой специальный режим, который, к сожалению, нужно будет собирать самому. Он называется headless lib. Это вот та самая минимальная библиотека, используя которую можно будет использовать headless-режим Хрома. Работа кипит - то, что могу сказать сейчас.

**Алексей:**
Ещё один вопрос волнует. Ну ты ответь насколько можешь или насколько знаешь. Сейчас, чтобы запустить headless-режим Хрома, тебе всё равно нужен оконный менеджер. Пускай это будет виртуальный оконный менеджер, какой-нибудь Xvfb, но, тем не менее, он нужен. У Фантома вся прелесть была в том, что тебе ничего не нужно. Ты просто берёшь бинарник и запускаешь. Это просто идеально простое решение для того, чтобы поставить и начать работать. Все эти игры с виртуальными оконными менеджерами порождают проблемы, нужны необходимые знания для запуска и так далее. В будущем Phantomium будет больше похож на PhantomJS всё-таки или всё равно тебе будут нужны виртуальные оконные менеджеры и ещё что-нибудь?

**Виталий:**
На самом деле, не совсем так. Тот самый headless Chrome, который был анонсирован и над которым велась работа уже некоторое количество времени, не потребует никакого виртуального фреймбуфера. На текущий момент без всяких этих оконных менеджеров и виртуальных фреймбуферов его можно запустить только на Линуксе. Если вы попытаетесь сейчас запустить канарейку на Windows и запустить её headless Chrome, вы увидите, что у вас всё равно будет окно, но, к сожалению, вы не сможете кликать по меню. Даже если откроете меню, Chrome просто крешится, потому что всё ещё довольно сырое и, если не ошибаюсь, такая же сейчас проблема на Маке.

Многие знают, что и до этого можно было запускать Chrome при помощи виртуального фреймбуфера и проводить в нём тесты, но это многих не устраивало, это было медленно, и вот headless Chrome как раз призван решить эту проблему.

**Алексей:**
Ну, опять же, звучит хорошо. А как по твоим прикидкам, как ты думаешь, когда простые разработчики смогут переписать, перевезти свои тесты на работу с Хромиумом?

**Виталий:**
Хороший вопрос. Я думаю, что я не смогу ответить на него, потому что, если я не ошибаюсь, там ещё не хватает обвязки вокруг всего доступного API. То есть, если кто-то не читал руководство headless Chrome, он на самом деле запускается в режиме такого удалённого веб-инспектора, то есть предоставляя вам удалённый протокол для отладки, при помощи которого вы можете манипулировать браузером, что-то смотреть, что-то делать. Просто так, скажем, с пылу, с жару, взять Chrome и быстро переписать на него тесты, к сожалению, не получится. Придётся очень сильно разбираться в API и, скорее всего, даже что-то там править в API, я имею ввиду в том самом npm-пакете, который сейчас предоставляется для управления headless-режимом.

**Вадим:**
Ну, по-моему, все люди, занимающиеся тестами в браузерах, допустим, функциональными тестами, привыкли, что какой бы ты движок/фреймворк не взял, каждый чего-то не умеет. И, видимо, вот этот вот безголовый Chrome тоже по началу чего-то будет не уметь, но какие-то базовые вещи всегда присутствуют.

То есть я думаю, в каждой базе тестов у любого проекта есть закомментированные тесты, которые должны работать, но не работают.

**Виталий:**
Да, я знаю, что PhantomJS очень часто используют для печати pdf-файлов. То есть когда бралась веб-страница и печаталась в pdf. Насколько я помню, headless Chrome до сих пор не умеет печатать. То есть вы не сможете печатать страницу в pdf-файл. До сих пор многие вещи в headless Chrome ещё не доступны, потому что, понятное дело, он ещё сырой и он будет активно дорабатываться.

**Алексей:**
От этого немножко грустно, потому что я знаю, что в Фантоме была проделана громаднейшая работа. Давайте возьмем простой пример: сглаживание шрифтов. То есть чтобы у вас на сервере не важно где было нормальное сглаживание шрифтов, вообще-то нужно попотеть, чтобы это всё работало. И много других похожих вещей.

Или, например, часто ведь для тестирования нужно имитировать какие-нибудь события, например, наведение мышкой, то есть какие-то события ховеров и так далее. В Фантоме, конечно, было не всё супер с этим, но как-то чуть-чуть это работало, и, опять же, как это будет в Chrome? То есть тут получается, что ребята стартовали абсолютно новый проект по замене того, что у нас есть сейчас. Но у нас будет видимо какая-то огромная временная задержка от того, что мы не сможем сейчас использовать headless-режим в новом Chrome, и Фантом при этом остаётся с теми проблемами, которые у него есть. В смысле поддержки фич браузеров: она там слишком старая, скажем так.

Я очень ждал 2.5, потому что вы там сделали очень хорошую работу, и подвели туда поддержку всего современного стека. Это в чейнджлогах выглядело очень хорошо.

**Виталий:**
Да, на самом деле, скриншоты — это очень больная тема. Потому что разработчики, или, скажем, тестировщики, приходили к нам на Гитхаб и жаловались: «Ребята, я сделал три скриншота одинаковых: на Windows, MacOS и на Linux, но они разные, ребята. Как мне сделать так, чтобы они были одинаковые, что называется pixel perfect?».

И вот тут возникает проблема, что это невозможно сделать. Невозможно сделать абсолютно одинаковые скриншоты, потому что, даже если вы запустите Chrome во всех трёх системах, вы увидите, что там даже те же самые шрифты, они по-другому отображаются на странице. Вы не можете просто сделать абсолютно одинаковые скриншоты. И та же самая участь будет и у headless Chrome, он тоже будет отображать страницы на разных операционных системах по разному, чуть-чуть, но немного иначе.

Что касается версии 2.5, если кто-то не знает, Константин Токарев решил возродить проект QtWebKit, тот самый движок, который мы использовали, и проапгрейдить его до последних версий, которые сейчас есть в оригинальном движке WebKit, но с тем условием, чтобы его можно было использовать с библиотекой Qt. После анонса новости я активно подключился к этому проекту, мы смогли его возродить до какого-то более-менее рабочего состояния, что я даже смог выпустить бета-версию 2.5, чтобы люди посмотрели, потому что там действительно, список изменений очень большой. Я бы, с одной стороны, даже не стал его делать, потому что я понимал, что мы, грубо говоря, взяли движок шестилетней давности и проапгрейдили его на движок сегодняшнего дня.

**Вадим:**
Ну, а насколько бета... насколько она альфа? Насколько ей вообще можно пользоваться? То есть если сейчас взять Фантом 2.5, вот ту самую бету, она принципиально заведётся? Насколько минорные там эти баги? Насколько это RC может быть уже?

**Виталий:**
Пользоваться можно на MacOS и Windows. Linux это вот ещё одна боль в наших головах была, потому что если на MacOS и Windows всё стабильно, всё понятно, всё работает, то Linux это всегда проблемы. Нельзя просто так взять и завести всё это дело на Линуксе.

На текущий момент использовать можно, несмотря на то, что многие жалуются, что оно падает, но на самом деле оно гораздо стабильнее, чем версия 2.1. Под Linux проблема в том, что тянется куча зависимостей, то есть мы так и не смогли закончить работу по уменьшению зависимостей, это как-раз планировалось сделать именно в релизе 2.5, и даже где-то у меня есть инструкция, как это сделать. Но, к сожалению, это не было реализовано.

**Вадим:**
Обычно все эти CI как раз работают на Юниксах и потому, да, новость грустная.

**Алексей:**
Что другие члены команды думают про всю эту историю? Тот же самый [Ария](https://github.com/ariya), у которого репозиторий Фантома собственно держится в личном GitHub? Я видел как там у вас в рассылке все сказали тебе «спасибо», «отличная работа» и так далее, но никаких новостей, дальнейших шагов. Что будет дальше с проектом вообще не очень понятно. Ну ушёл мейнтейнер, это понятная история, но, тем не менее, у проекта же остались ещё какие-то люди, сайт, рассылка, всё что угодно. Можно же прийти в этот проект, стать мейнтейнером и продолжить разработку.

**Виталий:**
Да, безусловно, можно, и я всячески агитирую за это. То есть я всячески помогу, чтобы, допустим, пришёл новый мейнтейнер и просто начал пилить проект.

И возвращаясь к вопросу о новичках, о тех, кто хочет помочь проекту, мы всегда открыты. Мы поможем, расскажем, покажем, проверим и примем.

**Вадим:**
Но вот что-то пока нет таких людей, да?

**Виталий:**
Да, к сожалению.

**Вадим:**
Ну ладно, мы тут загрустили. А можешь дать какую-то перспективу вообще безголовым браузерным движкам? Может быть конкуренция в этом смысле поможет? То есть есть ли какие-то такие же простые и интересные решения как Фантом или перспективы их появления на основе других движков, там Фокса, Эджа, ещё чего-то? Или это слишком узкая задача и Фантома хватало всегда?

**Виталий:**
Это был, скажем так, довольно обширный вопрос и я отвечу на него так: с момента моего сообщения о том, что я ухожу с поста мейнтейнера, я получил огромное количество отзывов от людей. Потом там были неоднократные обсуждения в подкастах, которые мне не очень были понятны, но проблема в том, что PhantomJS просто занимал свою нишу. Это было очень нишевое решение, и с точки зрения конкуренции это было очень неплохо, потому что даже тот же самый Firefox: недавно там появился первый патч, включающий полный headless mode для Firefox.

Если кто не знает, у нас есть брат в нашей семье призраков, он называется [SlimerJs](https://slimerjs.org), это полный аналог PhantomJS, работающий на движке Firefox, на Gekko, я даже больше скажу, у нас есть ещё такой малоизвестный брат, называется [trifleJS](http://triflejs.org) - это headless-режим для Internet Explorer, который пилил один человек, и он довольно сносно работал.

Если подумать про будущее безголовых браузеров — куда мы без них? Потому что все тесты у нас сейчас находятся на сервере, у нас есть continuous deployment и прочее. И каждый раз запускать Silenium и серверные гриды те же держать, это довольно дорогостоящи и требует серъёзной настройки, когда headless-браузеры, что называется, поставил, настроил и забыл.

**Вадим:**
Ну, на самом деле чаще всего тестирование — оно ведь базовое, unit-тесты нужно прогнать. И не нужно разворачивать вообще всё целиком, нужно очень маленький такой, знаешь, сабсет браузера, чтобы в нём всё прогнать. Не обязательно всё там прокликивать, в живом браузере, на живой операционной системе. Поэтому в этом смысле Фантом был и остаётся таким очень важным и крутым решением. Но там всё-таки свой джаваскриптовый движок, а их есть много других, и вот, собственно, вот в этом тоже вопрос.

**Алексей:**
Ну и я хочу сказать, что Фантом-то среди всех движков лидер. Вот ты сказал про SlimerJS и про патч, да, там у SlimerJs основная проблема была в том, что он всё равно запускался с виртуальным оконным менеджером, как я понимаю, патч сейчас старается избавиться от этого, чтобы это всё-таки был настоящий headless-режим, а уж про trifleJS, его основная проблема в том, что он запускается только на Windows. Это же совсем не то, что надо.

**Виталий:**
Вот в этом и есть основная прелесть Фантома, в том, что у тебя, по сути, есть один файл, и это полноценный браузер в одном исполняемом файле. И это была, как сейчас модно говорить, killer feature.

**Вадим:**
Я думаю, мы никуда от Фантома так или иначе не денемся, как уж мы будем его называть, склонять и так далее. Я надеюсь, что интерес Пола Айриша и твои собственные разработки, и вообще интерес сообщества к тому, что нужно тестировать удобно и быстро, они приведут нас к тому, что появится новое решение. Даже если старое мы похороним, то знаешь, тесты вы ведь не зря писали, поэтому и удобное API и уже написанный код, совместимость... в общем мы не бросим это дело. Я почему-то уверен.

**Виталий:**
Да, я тоже никуда не пропадаю, я хочу работать над этим дальше и посмотрим, что будет.

---

*Слушайте наш подкаст в [iTunes](https://itunes.apple.com/ru/podcast/девшахта/id1226773343) и [SoundCloud](https://soundcloud.com/devschacht), читайте нас на [Medium](https://medium.com/devschacht), контрибьютьте на [GitHub](https://github.com/devSchacht), общайтесь в [группе Telegram](https://t.me/devSchacht), следите в [Twitter](https://twitter.com/DevSchacht) и [канале Telegram](https://t.me/devSchachtChannel), рекомендуйте в [VK](https://vk.com/devschacht) и [Facebook](https://www.facebook.com/devSchacht).*

[Статья на Medium](https://medium.com/devschacht/phantomjs-is-over-df065e5b23bf)