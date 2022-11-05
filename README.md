
<h1 align="center">Hi, I'm Di</h1>
<h3 align="center">Flutter mobile (Android)</h3>

1. Скачать Flutter SDK 

Я скачаю на Flutter version 3.3.7 на 05.11.2022
https://storage.googleapis.com/flutter_infra_release/releases/stable/windows/flutter_windows_3.3.7-stable.zip


Актуальную стабильную версию можно скачать
https://docs.flutter.dev/development/tools/sdk/releases


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




Плагины для VS code
https://marketplace.visualstudio.com/items?itemName=Dart-Code.dart-code


https://marketplace.visualstudio.com/items?itemName=Dart-Code.flutter





Что необходимо скачать и инсталировать
 1. flutter_windows_3.3.7-stable
 2. Visual Studio 2022 или Visual Studio Build Tools 2022 
 3. Java 8 

 Создание проект flutter create testapp --offline