<p align="right"><a href="/readme-eng.md"><sup>ENG</sup></a></p>


# CS:GO Crosshair Manager

**Crosshair Manager** - это инструмент для организации, взаимодействия и управления вашими прицелами, их настройкой и зависимостями из одного конфигурационного файла.

<p align="center"><img src="/images/preview.gif"> </p>

Данный органайзер предоставляет возможность использовать несколько пресетов для ваших прицелов одновременно. Каждый пресет содержит конфигурацию прицела для смоков, основного и второстепенных слотов. Итого: Crosshair Manager - инструмент, позволяющий осуществить горячуюю замену до четырёх различных прицелов одним нажатием клавиши и непосредственно во время матча. 

Теперь все Ваши конфигурации намного проще хранить. Больше нет необходимости каждый раз править autoexec.cfg, ведь каждый прицел хранится и считывается из своего отдельного файла, а вся настройка доступна в `crosshair-UI.cfg`.

---


## Install

Для установки менеджера необходимо перенести все файлы из [архива](https://github.com/YakkaDev/CS-GO-Crosshair-Manager/releases/download/v1.1/Crosshair-M.v1.1.rar) (кроме *autoexec.cfg*, о нём ниже) в свою папку конфигурации по пути `<csgo folder>/csgo/cfg`

В файл **autoexec.cfg** по пути `<csgo folder>/csgo/cfg` необходимо добавить строчки из аналогичного конфигурационного файла в [пакете Crosshair Manager](https://github.com/YakkaDev/CS-GO-Crosshair-Manager/releases/download/v1.1/Crosshair-M.v1.1.rar).

> Данный файл является автозагрузчиком параметров основного файла настроек игры. У опытных игроков autoexec зачастую уже находится в параметрах запуска CS:GO, но если вы - другой случай, то необходимо проследовать в библиотеку Steam, далее *выбрать CS:GO при помощи ПКМ - Свойства - Общие - Параметры запуска* и указать `+exec autoexec.cfg`

<p align="center"><img src="/images/launch.png"> </p>

Строка `bind "key" "changeCrosshair"` в параметрах autoexec.cfg отвечает за переключение прицела. Замените *key* на вашу желаемую клавишу.

---

## Settings

В файле **crosshair_UI.cfg** вы сможете найти строки `alias cross_tech_primary "exec ..."` и `alias cross_tech_second "exec ..."` имеющие соответственное предписание внутри файла. Данные алиасы указывают на конфигурационные файлы ваших прицелов - первый и второй режимы соответственно. Сюда необходимо указать названия ваших файлов с настройками прицела, которые предварительно поместить в папку по пути `<csgo folder>/csgo/cfg`. Для удобста, я использую нумерацию в наименованиях, например *"crosshair_1.cfg"* и т.д.

Тут же присутствует универсальная строка `alias cross_tech_other "exec ..."` - это общий прицел для третьего и четвёртого слота, а так же всех гранат, кроме дымовой. Последний тип гранат так же прописан в данном файле, а именно - колонке "Engine" и выглядит так: `alias cross_tech_smokes "exec crosshair_smokes.cfg"`. 

Остальные бинды в файле рекомендуется не кастомизировать, поскольку это может привести к отказу работоспособности менеджера, либо попросту не имеет никакого смысла.

---

## Config

В архиве присутствует три файла: *"crosshair_1.cfg", "crosshair_2.cfg" и "crosshair_3.cfg"*. Данные файлы полностью одинаковые и являются примером правильного конфигурационного файла прицела.

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

---

## Colors

Чтобы изменить цвет прицела воспользуйтесь командами ниже:
|   Command     |     Color     |                       Image                                 |
| ------------- | ------------- | ----------------------------------------------------------- |
| cross_red     | Red           | ![Red](/images/colors/cross_red.png "Red")                  |
| cross_green   | Green         | ![Green](/images/colors/cross_green.png "Green")            |
| cross_blue    | Blue          | ![Blue](/images/colors/cross_blue.png "Blue")               |
| cross_black   | Black         | ![Black](/images/colors/cross_black.png "Black")            |
| cross_white   | White         | ![White](/images/colors/cross_white.png "White")            |
| cross_yellow  | Yellow        | ![Yellow](/images/colors/cross_yellow.png "Yellow")         |
| cross_orange  | Orange        | ![Orange](/images/colors/cross_orange.png "Orange")         |
| cross_breathe | Blue-Light    | ![Blue-Light](/images/colors/cross_breathe.png "Blue-Light")|
| cross_pink    | Pink          | ![Pink](/images/colors/cross_pink.png "Pink")               |
| cross_purple  | Purple        | ![Purple](/images/colors/cross_purple.png "Purple")         |
| cross_brown   | Brown         | ![Brown](/images/colors/cross_brown.png "Brown")            |
| cross_chestnut| Chestnut      | ![Chestnut](/images/colors/cross_chestnut.png "Chestnut")   |

---

<p align="CENTER"><a href="https://github.com/YakkaDev/CS-GO-Crosshair-Manager"><img alt="Hits" src="https://hits.sh/github.com/YakkaDev/CS-GO-Crosshair-Manager.svg?label=Gotcha&color=ffb100"/></a></p>
