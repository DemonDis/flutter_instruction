
<div align="center"><img src="./images/InnoLab.png" height="150"/></div>
<h1 align="center">Instruction<img src="./images/flutter.png" height="28"/></h1>
<h3 align="center"><img src="./images/Android.png" height="55"/><img src="https://seeklogo.com/images/W/windows-11-icon-logo-6C39629E45-seeklogo.com.png" height="55"/></h3>


## Оглавление (05.11.2022)

0. [Программный минимум](#Программный-минимум)
1. [Установка Flutter](#Установка-Flutter)
    1. [Flutter SDK](#Flutter-SDK)
    2. [Установка Flutter SDK](#Установка-Flutter-SDK)
        1. [Переменные среды Windows FLUTTER](#Переменные-среды-Windows-FLUTTER)
        2. [Отключаем аналитику](#Отключаем-аналитику)
    3. [Проверка работы flutter](#Проверка-работы-flutter)
2. [Установка Java](#Установка-Java)
    1. [Переменные среды Windows JAVA](#Переменные-среды-Windows-JAVA)
3. [Установка HAXM](#Установка-HAXM)
4. [Установка Windows SDK](#Установка-Windows-SDK)
5. [Установка пакетов Visual Studio](#Установка-пакетов-Visual-Studio)
6. [Установка плагинов Visual Studio Code](#Установка-плагинов-Visual-Studio-Code)
7. [Локальный Gradle Build Tool](#Локальный-Gradle-Build-Tool)
    1. [Переменные среды Windows GRADLE](#Переменные-среды-Windows-GRADLE)
9. [Установка Android](#Установка-Android)
10. [Проверка установленных программ](#Проверка-установленных-программ)
11. [Hello world Flutter](#Hello-world-Flutter)
    1. [Создание-проекта](#Cоздание-проекта)
    2. [Запуск эмулятора Android](#Запуск-эмулятора-Android)

## Программный минимум

1. <a href="https://developer.tizen.org/development/tizen-studio/download/installing-tizen-studio/hardware-accelerated-execution-manager" target="_blank">HAXM</a>
2. <a href="https://www.oracle.com/java/technologies/downloads/" target="_blank">JDK</a>
3. <a href="https://www.oracle.com/java/technologies/downloads/" target="_blank">Windows SDK</a>
4. <a href="https://docs.flutter.dev/development/tools/sdk/releases" target="_blank">Flutter SDK </a>
5. <a href="https://visualstudio.microsoft.com/ru/thank-you-downloading-visual-studio/?sku=Community&channel=Release&version=VS2022&source=VSLandingPage&cid=2030&passive=false" target="_blank">Visual Studio</a>
6. <a href="https://marketplace.visualstudio.com/items?itemName=Dart-Code.dart-code" target="_blank">Dart для Visual Studio Code</a>
7. <a href="https://marketplace.visualstudio.com/items?itemName=Dart-Code.flutter" target="_blank">Flutter для Visual Studio Code</a>
8. <a href="https://gradle.org/install/" target="_blank">Gradle Build Tool</a>
9. <a href="https://developer.android.com/studio" target="_blank">SDK tools package (sdkmanager android)</a>
____

## Установка Flutter

### Flutter SDK

Скачиваем актуальный архив <a href="https://docs.flutter.dev/development/tools/sdk/releases">Stable channel (Windows)</a> 
____
### Установка Flutter SDK

 1. Распоковать файл flutter_windows_3.3.7-stable (версия на 05.11.2022) в C:\src\flutter
____
#### Переменные среды Windows FLUTTER

 1. Win + R в появившемся окне "Выполнить" ввести 
 ```
 sysdm.cpl
 ```
 2. На вкладке «Дополнительно» нажмите кнопку «Переменные среды…».
 3. Переменные среды пользователя для (имя пользователя) выбрать Path и нажать изменить.
 4. Добавить в строчку C:\src\flutter\bin (или тот маршрут куда вы положили Flutter SDK) и нажать ОК и еще раз ОК.
____
#### Отключаем аналитику

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
### Проверка работы flutter
 
 1. Вести в командную строку терминала 
 ```
 flutter doctor
 ```
 2. После того как команда отработает появится список программ или ошибок (может и не появиться, если все ноебходимое уставноленно и исправно).
____
## Установка Java

1. Скачиваем <a href="https://www.oracle.com/java/technologies/downloads/" target="_blank">Java SE Development</a>
2. Распоковать файл jdk-19_windows-x64_bin.zip (версия на 05.11.2022) в C:\Java\jdk-15.0.2
____
#### Переменные среды Windows JAVA

 1. Win + R в появившемся окне "Выполнить" ввести 
 ```
 sysdm.cpl
 ```
 2. На вкладке «Дополнительно» нажмите кнопку «Переменные среды…».
 3. Переменные среды пользователя для (имя пользователя) выбрать Path и нажать изменить.
 4. Добавить в строчку C:\Java\jdk-15.0.2\bin (или тот маршрут куда вы положили jdk) и нажать ОК и еще раз ОК.
____
## Установка HAXM

1. Скачиваем <a href="https://developer.tizen.org/development/tizen-studio/download/installing-tizen-studio/hardware-accelerated-execution-manager" target="_blank">HAXM</a>
2. Типовая установка.
____
## Установка Windows SDK

1. Скачиваем <a href="https://www.oracle.com/java/technologies/downloads/" target="_blank">Windows SDK</a>
2. Типовая установка.

____
## Установка пакетов Visual Studio

:boom: Данный путь без уставноки Visual Studio. Только необходимые пакеты. 
1. Скачавыем <a href="https://learn.microsoft.com/en-us/visualstudio/install/create-an-offline-installation-of-visual-studio?view=vs-2022" target="_blank">Visual Studio 2022 Build Tools</a>
2. Запускаем программу vs_buildtools.exe с помощью терминала.
 ```
 vs_enterprise.exe --layout c:\localVSlayout --add Microsoft.VisualStudio.Workload.NativeDesktop --includeRecommended --lang ru-RU
 ```
____
## Установка плагинов Visual Studio Code

1. Палагин <a href="https://marketplace.visualstudio.com/items?itemName=Dart-Code.dart-code" target="_blank">DART</a>
2. Палагин <a href="https://marketplace.visualstudio.com/items?itemName=Dart-Code.flutter" target="_blank">FLUTTER</a>
____
## Локальный Gradle Build Tool

1. Скачиваем <a href="https://services.gradle.org/distributions/" target="_blank">Gradle Build Tool</a> (скролим вниз до таблицы)
2. Распоковать файл gradle-7.6-rc-2-all.zip (версия на 05.11.2022) в C:\gradle.
____
#### Переменные среды Windows GRADLE

 1. Win + R в появившемся окне "Выполнить" ввести 
 ```
 sysdm.cpl
 ```
 2. На вкладке «Дополнительно» нажмите кнопку «Переменные среды…».
 3. Переменные среды пользователя для (имя пользователя) выбрать Path и нажать изменить.
 4. Добавить в строчку C:\gradle\gradle-7.6-rc-2-all\bin (или тот маршрут куда вы положили gradle) и нажать ОК и еще раз ОК.
____
## Установка Android

1. Скачиваем <a href="https://developer.android.com/studio" target="_blank">SDK tools package</a>
2. Распоковать файл commandlinetools-win-8512546_latest.zip (версия на 05.11.2022) в C:\Android-SDK
____
#### Переменные среды Windows ANDROID

 1. Win + R в появившемся окне "Выполнить" ввести 
 ```
 sysdm.cpl
 ```
 2. На вкладке «Дополнительно» нажмите кнопку «Переменные среды…».
 3. Смотрим вниз "Системные переменные" жмем создать.
 4. Имя перменной ANDROID_HOME. Значение перменной C:\Android-SDK\cmdline-tools\bin\ (или тот маршрут куда вы положили Android SDK) и жмем ОК и еще раз ОК.
____

4. Переходим <a href="https://developer.android.com/studio/releases" target="_blank">releases notes</a> и выбираем необходимые версии программ. Я возьму последние на 05.11.2022.
6. Запускаем программу sdkmanager с помощью терминала из папки C:\Android-SDK\cmdline-tools\bin\
 ```
 sdkmanager --sdk_root=sdkRootPath "platforms;android-29" "build-tools;29.0.3" "extras;google;m2repository" "extras;android;m2repository"

 ```
 https://medium.com/@quicky316/install-flutter-sdk-on-windows-without-android-studio-102fdf567ce4
  ```
 sdkmanager "system-images;android-27;default;x86_64"
sdkmanager "platform-tools"
sdkmanager "build-tools;27.0.3"
sdkmanager "platforms;android-27"
sdkmanager emulator

 ```
 
____
## Проверка установленных программ

1. Flutter
 ```
 flutter doctor
 ```
 2. Gradle
 ```
 gradle -v
 ```
____
## Hello world Flutter

### Создание проекта


____
### Запуск эмулятора Android


____



 Создание проект flutter create testapp --offline
