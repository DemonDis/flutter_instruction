
    1) Качаем и ставим HAXM, если не стоит (https://developer.tizen.org/development/tizen-studio/download/installing-tizen-studio/hardware-accelerated-execution-manager)
    
    2) Поставил jdk-8u281-windows-x64.exe (https://www.oracle.com/in/java/technologies/javase/javase-jdk8-downloads.html).

    3) Складываю файлы на диск С и настраиваю среду окружения.
Свойство моего компа -> Дополнительные параметры -> Параметры среду (вкладка дополнительно) -> Изменить Path -> C:\Program Files\Java\jdk-15.0.2\bin

    4) Качаю sdkmanager android (https://developer.android.com/studio) - commandlinetools-win-6858069_latest.zip

    5) Распаковываю файлы на диск C sdkmanager и обновляю на всякий случай .\C с командой .\Android-SDK\tools\bin\sdkmanager.bat --sdk_root=sdkRootPath --update

    6) В папку Android-SDK\tools\lib_ залетели файлы apkanalyzer-classpath, avdmanager-classpath, lint-classpath, screenshot2-classpath, sdkmanager-classpath.
Я их перекладываю выше и жму .\Android-SDK\tools\bin\sdkmanager.bat --sdk_root=sdkRootPath --update

    7) Далее ставлю следующие пакеты .\Android-SDK\cmdline-tools\bin\sdkmanager.bat --sdk_root=sdkRootPath "platforms;android-29" "build-tools;29.0.3" "extras;google;m2repository" "extras;android;m2repository"

    8) Прописываю ANDROID_HOME. Свойство моего компа -> Дополнительные параметры -> Параметры среду (вкладка дополнительно) -> Создать -> ANDROID_HOME -> C:\Android-SDK

    9) Прописываю ANDROID_SDK_ROOT. Свойство моего компа -> Дополнительные параметры -> Параметры среду (вкладка дополнительно) -> Создать -> ANDROID_SDK_ROOT-> C:\Android-SDK

    10) Меняю Path. Свойство моего компа -> Дополнительные параметры -> Параметры среду (вкладка дополнительно) -> Изменить Path -> C:\Android-SDK\cmdline-tools\tools\bin

    11) Делаю команды из папки С. echo $env:ANDROID_HOME

PIE (9.0) API 28
    .\Android-SDK\cmdline-tools\bin\sdkmanager.bat --sdk_root=sdkRootPath Run the sdkmanager commands sdkmanager --install "system-images;android-28;google_apis;x86"

 Use AVDMANAGER to create emulators
Pixel Emulator with Google Apis and x86 architecture
    echo "no" | avdmanager --verbose create avd --force --name "pixel_9.0" --device "pixel" --package "system-images;android-28;google_apis;x86" --tag "google_apis" --abi "x86"
Generic Emulator with Google Apis
    echo "no" | avdmanager --verbose create avd --force --name "generic_9.0" --package "system-images;android-28;google_apis;x86" --tag "google_apis" --abi "x86"

npx react-native start
npx react-native run-android


https://gist.github.com/mrk-han/66ac1a724456cadf1c93f4218c6060ae
https://www.youtube.com/watch?v=VdNKahMk27U

android\gradle\wrapper\gradle-wrapper.properties
distributionUrl=https\://services.gradle.org/distributions/gradle-6.8.1-all.zip

android\local.properties
sdk.dir=C:\\Android-SDK

taskkill /f /im node.exe