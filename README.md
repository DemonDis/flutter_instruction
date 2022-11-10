
<div align="center"><img src="./images/InnoLab.png" height="150"/></div>
<h1 align="center">Instruction<img src="./images/flutter.png" height="28"/></h1>
<h3 align="center"><img src="./images/Android.png" height="55"/><img src="https://seeklogo.com/images/W/windows-11-icon-logo-6C39629E45-seeklogo.com.png" height="55"/></h3>


## Оглавление (05.11.2022)

0. [Программный минимум](#Программный-минимум)
1. [Установка Flutter](#Установка-Flutter)
    1. [Flutter SDK](#Flutter-SDK)
    2. [Установка Flutter SDK](#Установка-Flutter-SDK)
        1. [Переменные среды Windows](#Переменные-среды-Windows)
        2. [Отключаем аналитику](#Отключаем-аналитику)
    3. [Проверка работы flutter](#Проверка-работы-flutter)
2. [Установка Java](#Установка-Java)
3. [Установка HAXM](#Установка-HAXM)
4. [Установка Windows SDK](#Установка-Windows-SDK)
5. [Установка Visual Studio](#Установка-Visual-Studio)
6. [Установка плагинов Visual Studio Code](#Установка-плагинов-Visual-Studio-Code)
7. [Установка Android](#Установка-Android)

## Программный минимум

1. <a href="https://developer.tizen.org/development/tizen-studio/download/installing-tizen-studio/hardware-accelerated-execution-manager" target="_blank">HAXM</a>
2. <a href="https://www.oracle.com/java/technologies/downloads/" target="_blank">JDK</a>
3. <a href="https://www.oracle.com/java/technologies/downloads/" target="_blank">Windows SDK</a>
4. <a href="https://docs.flutter.dev/development/tools/sdk/releases" target="_blank">Flutter SDK </a>
5. <a href="https://visualstudio.microsoft.com/ru/thank-you-downloading-visual-studio/?sku=Community&channel=Release&version=VS2022&source=VSLandingPage&cid=2030&passive=false" target="_blank">Visual Studio</a>
6. <a href="https://marketplace.visualstudio.com/items?itemName=Dart-Code.dart-code" target="_blank">Dart для Visual Studio Code</a>
7. <a href="https://marketplace.visualstudio.com/items?itemName=Dart-Code.flutter" target="_blank">Flutter для Visual Studio Code</a>
8. <a href="https://developer.android.com/studio" target="_blank">SDK tools package (sdkmanager android)</a>
____

## Установка Flutter

#### Flutter SDK

Скачиваем актуальный архив <a href="https://docs.flutter.dev/development/tools/sdk/releases">Stable channel (Windows)</a> 
____
#### Установка Flutter SDK

 1. Распоковать файл flutter_windows_3.3.7-stable (версия flutter на 05.11.2022) в C:\src\flutter
____
##### Переменные среды Windows

 1. Win + R в появившемся окне "Выполнить" ввести 
 ```
 sysdm.cpl
 ```
 2. На вкладке «Дополнительно» нажмите кнопку «Переменные среды…».
 3. Переменные среды пользователя для (имя пользователя) выбрать Path и нажать изменить.
 4. Добавить в строчку C:\src\flutter\bin (или тот маршрут куда вы положили Flutter SDK)и нажать ОК и еще раз ОК
____
##### Отключаем аналитику

:boom: Это не обязательный  пункт
 1. Отключаем аналитику Flutter (сбор данных)
 ```
 flutter config --no-analytics
 ```
  2. Отключаем аналитику Dart (сбор данных)
 ```
 dart config --no-analytics
 ```
____
#### Проверка работы flutter
 
 1. Вести в командную строку терминала 
 ```
 flutter doctor
 ```
 2. После того как команда отработает появится список программ или ошибок (может и не появиться, если все ноебходимое уставноленно и исправно).
____
## Установка Java


____
## Установка HAXM


____
## Установка Windows SDK


____
## Установка Visual Studio


____
## Установка плагинов Visual Studio Code

1. Палагин <a href="https://marketplace.visualstudio.com/items?itemName=Dart-Code.dart-code" target="_blank">DART</a>
2. Палагин <a href="https://marketplace.visualstudio.com/items?itemName=Dart-Code.dart-code" target="_blank">FLUTTER</a>
____


 6. Установить Visual Studio 2022 (Community)
 https://visualstudio.microsoft.com/ru/thank-you-downloading-visual-studio/?sku=Community&channel=Release&version=VS2022&source=VSLandingPage&cid=2030&passive=false

Нам понадобятся следующие пакеты

Для установки в автономном режиме 
https://learn.microsoft.com/en-us/visualstudio/install/create-an-offline-installation-of-visual-studio?view=vs-2022

6.1 Переходим по ссылке и качаем Visual Studio 2022 Корпоративная vs_enterprise.exe
https://learn.microsoft.com/en-us/visualstudio/install/create-a-network-installation-of-visual-studio?view=vs-2022


Для утсновки offline переходим по ссылке
https://learn.microsoft.com/ru-ru/visualstudio/install/create-an-offline-installation-of-visual-studio?view=vs-2022

Скачиваем Visual Studio 2022 Build Tools vs_buildtools.exe
Далее переходим в терминал и запускаем exe

Для скачивания всего \
vs_enterprise.exe --layout c:\localVSlayout --lang ru-RU

Для разработки классических приложений C++ выполните следующую команду
vs_enterprise.exe --layout c:\localVSlayout --add Microsoft.VisualStudio.Workload.NativeDesktop --includeRecommended --lang en-US

Чтобы установщик не попытался подключиться к Интернету, используйте параметр --noweb.

Далее запускаем локульную установку
vs_enterprise.exe --layout c:\localVSlayout --add Microsoft.VisualStudio.Workload.ManagedDesktop --add Microsoft.VisualStudio.Workload.NetWeb --includeOptional --lang en-US

 Создание проект flutter create testapp --offline
