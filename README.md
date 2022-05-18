# Add Localizatin JADX GUI
Добовляем Русскую локализацию в Jadx GUI - Dex to Java decompiler https://github.com/skylot/jadx
 открываем jadx/gui/utils/NLS.java
 и там редактируем такой массив добовлением своей строчки LANG_LOCALES.add(new LangLocale("ru", "RU")); в:
		LANG_LOCALES.add(new LangLocale("en", "US"));
		LANG_LOCALES.add(new LangLocale("zh", "CN"));
		LANG_LOCALES.add(new LangLocale("zh", "TW"));
		LANG_LOCALES.add(new LangLocale("es", "ES"));
		LANG_LOCALES.add(new LangLocale("de", "DE"));
		LANG_LOCALES.add(new LangLocale("ko", "KR"));
чтоб получилось допустим как у меня
    LANG_LOCALES.add(new LangLocale("en", "US"));
		LANG_LOCALES.add(new LangLocale("zh", "CN"));
		LANG_LOCALES.add(new LangLocale("zh", "TW"));
		LANG_LOCALES.add(new LangLocale("es", "ES"));
		LANG_LOCALES.add(new LangLocale("de", "DE"));
		LANG_LOCALES.add(new LangLocale("ko", "KR"));
		LANG_LOCALES.add(new LangLocale("ru", "RU"));
    сохраняем и компелируем....
   также там есть готовый собранный NLS.class и орегенальный NLS.java~ из jadx-gui-1.3.5-with-jre-win текущей на данный момент версии. 
   А собирал я так скачал openjdk-18.0.1.1_windows-x64_bin
   в HxD - это хекс редактор под windows
   Разделил jadx-gui-1.3.5.exe с zip частью
   все разложил по папкам и дальше в cmd ввел SET PATH=C:\Users\Serzh\Desktop\jadx-gui-1.3.5-with-jre-win\jdk-18.0.1.1\bin
   и после javac -d class -cp jadx-gui-1.3.5.zip jadx/gui/utils/NLS.java
   закинул из папки class файл NLS.class в jadx/gui/utils/ zip архива
   и после командой COPY /b jadx-gui-1.3.5.exe.bak+jadx-gui-1.3.5.zip jadx-gui-1.3.5_Rus.exe
   Собрал это дело.
