
<div align="center"><img src="./images/InnoLab.png" height="150"/></div>
<h1 align="center">Instruction<img src="./images/flutter.png" height="28"/></h1>
<h3 align="center"><img src="./images/Android.png" height="55"/><img src="https://seeklogo.com/images/W/windows-11-icon-logo-6C39629E45-seeklogo.com.png" height="55"/></h3>

## Оглавление 05.11.2022

0. [Программный минимум](#Программный-минимум)
1. [Установка Flutter](#Установка-Flutter)
    1. [Flutter SDK](#Flutter-SDK)
    2. [Установка Flutter SDK](#Установка-Flutter-SDK)


## Программный минимум

1. <a href="https://developer.tizen.org/development/tizen-studio/download/installing-tizen-studio/hardware-accelerated-execution-manager" target="_blank">HAXM</a>
2. <a href="https://www.oracle.com/java/technologies/downloads/" target="_blank">JDK</a>
3. <a href="https://docs.flutter.dev/development/tools/sdk/releases" target="_blank">Flutter SDK </a>
4. <a href="https://visualstudio.microsoft.com/ru/thank-you-downloading-visual-studio/?sku=Community&channel=Release&version=VS2022&source=VSLandingPage&cid=2030&passive=false" target="_blank">Visual Studio</a>
5. <a href="https://marketplace.visualstudio.com/items?itemName=Dart-Code.dart-code" target="_blank">Dart для Visual Studio Code</a>
6. <a href="https://marketplace.visualstudio.com/items?itemName=Dart-Code.flutter" target="_blank">Flutter для Visual Studio Code</a>
7. <a href="https://developer.android.com/studio" target="_blank">SDK tools package (sdkmanager android)</a>
____

## Установка Flutter

#### Flutter SDK

Скачиваем актуальный архив <a href="https://docs.flutter.dev/development/tools/sdk/releases">Stable channel (Windows)</a> 

#### Установка Flutter SDK

2. Распоковать файл flutter_windows_3.3.7-stable в например C:\src\flutter

3. Добавить переменные среды Windows
 3.1 Win + R и ввести sysdm.cpl.
 3.2 На вкладке «Дополнительно» нажмите кнопку «Переменные среды…».
 3.3 Переменные среды пользователя для (имя пользователя) выбрать Path и нажать изменить.
 3.4 Добавить в строчку C:\src\flutter\bin и нажать ОК и еще раз ОК

4. Вести в компандную строку flutter doctor
 
 Смотрим что еще необходимо доставить для рабты flutter

5. В нашем случае мы не хотим отправлять никакую аналитику. Отключаем! Используем терминал.

OFF - Аналитика инструмента Flutter
 flutter config --no-analytics

 OFF - Аналитика инструмента Dart
 dart config --no-analytics

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


Windows SDK
https://developer.microsoft.com/en-us/windows/downloads/windows-sdk/



Плагины для VS code
https://marketplace.visualstudio.com/items?itemName=Dart-Code.dart-code


https://marketplace.visualstudio.com/items?itemName=Dart-Code.flutter



 Создание проект flutter create testapp --offline
