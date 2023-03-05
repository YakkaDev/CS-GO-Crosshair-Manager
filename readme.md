# CS:GO Crosshire Manager

Crosshire Manager - это инструмент для организации, взаимодействия и управления вашими прицелами, их настройкой и зависимостями из одного конфигурационного файла.

![Crosshair Manager](/images/preview.gif "Crosshire Manager")

Данный органайзер предоставляет возможность использовать несколько пресетов для ваших прицелов одновременно. Каждый пресет содержит конфигурацию прицела для смоков, основного и второстепенных слотов. Итого: Crosshire Manager - инструмент, позволяющий осуществить горячуюю замену до четырёх различных прицелов одним нажатием клавиши и непосредственно во время матча. 

Теперь все Ваши конфигурации намного проще хранить. Больше нет необходимости каждый раз править autoexec.cfg, ведь каждый прицел хранится и считывается из своего отдельного файла, а вся настройка доступна в `crosshair-UI.cfg`.

---


## Install
Для установки менеджера необходимо перенести все файлы из архива (кроме *autoexec.cfg*, о нём ниже) в свою папку конфигурации по пути `<csgo folder>/csgo/cfg`

В файл **autoexec.cfg** по пути `<csgo folder>/csgo/cfg` необходимо добавить строчки из аналогичного конфигурационного файла в пакете Crosshire Manager.

> Данный файл является автозагрузчиком параметров основного файла настроек игры. У опытных игроков autoexec зачастую уже находится в параметрах запуска CS:GO, но если вы - другой случай, то необходимо проследовать в библиотеку Steam, далее *выбрать CS:GO при помощи ПКМ - Свойства - Общие - Параметры запуска* и указать `+exec autoexec.cfg`

Строка `bind "key" "changeCrosshair"` отвечает за переключение прицела. Замените *key* на вашу желаемую клавишу.

![Launch settings](/images/launch.png "Launch settings")

## Settings
В файле **crosshair_UI.cfg** вы сможете найти строки `alias cross_tech_primary "exec ..."` и `alias cross_tech_second "exec ..."` имеющие соответственное предписание внутри файла. Данные алиасы указывают на конфигурационные файлы ваших прицелов - первый и второй режимы соответственно. Сюда необходимо указать названия ваших файлов с настройками прицела, которые предварительно поместить в папку по пути `<csgo folder>/csgo/cfg`. Для удобста, я использую нумерацию в наименованиях, например *"crosshire_1.cfg"* и т.д.

Тут же присутствует универсальная строка `alias cross_tech_other "exec ..."` - это общий прицел для третьего и четвёртого слота, а так же всех гранат, кроме дымовой. Последний тип гранат так же прописан в данном файле, а именно - колонке "Engine" и выглядит так: `alias cross_tech_smokes "exec crosshire_smokes.cfg"`. 

Остальные бинды в файле рекомендуется не кастомизировать, поскольку это может привести к отказу работоспособности менеджера, либо попросту не имеет никакого смысла.

## Config
В архиве присутствует три файла: *"crosshire_1.cfg", "crosshire_2.cfg" и "crosshire_3.cfg"*. Данные файлы полностью одинаковые и являются примером правильного конфигурационного файла прицела.

Внутри конфигурационного файла прицела должны находиться следующие строки:
```
cl_crosshair_drawoutline "0"
cl_crosshair_dynamic_maxdist_splitratio "0"
cl_crosshair_dynamic_splitalpha_innermod "0"
cl_crosshair_dynamic_splitalpha_outermod "0"
cl_crosshair_dynamic_splitdist "0"
cl_crosshair_friendly_warning "0"
cl_crosshair_outlinethickness "0"
cl_crosshair_t "0"
cl_crosshairalpha "0"
cl_crosshairdot "0"
cl_crosshairgap "0"
cl_crosshairgap_useweaponvalue "0"
cl_crosshairsize "0"
cl_crosshairstyle "0"
cl_crosshairthickness "0"
cl_crosshairusealpha "0"
```

>Note: Цвет прицела в файле указывать не нужно!

## Colors
Чтобы изменить цвет прицела воспользуйтесь командами ниже:
|   Command     |     Color     |                       Image                          |
| ------------- | ------------- | ---------------------------------------------------- |
| cross_red     | Red           | ![Red](/images/colors/cross_red.png "Red")           |
| cross_green   | Green         | ![Green](/images/cross_green.png "Green")            |
| cross_blue    | Blue          | ![Blue](/images/cross_blue.png "Blue")               |
| cross_black   | Black         | ![Black](/images/cross_black.png "Black")            |
| cross_white   | White         | ![White](/images/cross_white.png "White")            |
| cross_yellow  | Yellow        | ![Yellow](/images/cross_yellow.png "Yellow")         |
| cross_orange  | Orange        | ![Orange](/images/cross_orange.png "Orange")         |
*| cross_breathe | Blue-Light    | ![Blue-Light](/images/cross_breathe.png "Blue-Light")|
| cross_pink    | Pink          | ![Pink](/images/cross_pink.png "Pink")               |
*| cross_purple  | Purple        | ![Purple](/images/cross_purple.png "Purple")         |
| cross_brown   | Brown         | ![Brown](/images/cross_brown.png "Brown")            |
| cross_chestnut| Chestnut      | ![Chestnut](/images/cross_chestnut.png "Chestnut")   |