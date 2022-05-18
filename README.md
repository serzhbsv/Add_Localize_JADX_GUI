# Add Localizatin JADX GUI<br>
Добовляем Русскую локализацию в Jadx GUI - Dex to Java decompiler https://github.com/skylot/jadx<br>
 открываем jadx/gui/utils/NLS.java
 и там редактируем такой массив добовлением своей строчки LANG_LOCALES.add(new LangLocale("ru", "RU")); в:<br>
 ............................................................................................................
........................LANG_LOCALES.add(new LangLocale("en", "US"));<br>
........................LANG_LOCALES.add(new LangLocale("zh", "CN"));<br>
........................LANG_LOCALES.add(new LangLocale("zh", "TW"));<br>
........................LANG_LOCALES.add(new LangLocale("es", "ES"));<br>
........................LANG_LOCALES.add(new LangLocale("de", "DE"));<br>
........................LANG_LOCALES.add(new LangLocale("ko", "KR"));<br>
чтоб получилось допустим как у меня<br>
........................LANG_LOCALES.add(new LangLocale("en", "US"));<br>
........................LANG_LOCALES.add(new LangLocale("zh", "CN"));<br>
........................LANG_LOCALES.add(new LangLocale("zh", "TW"));<br>
........................LANG_LOCALES.add(new LangLocale("es", "ES"));<br>
........................LANG_LOCALES.add(new LangLocale("de", "DE"));<br>
........................LANG_LOCALES.add(new LangLocale("ko", "KR"));<br>
........................LANG_LOCALES.add(new LangLocale("ru", "RU"));<br>
    сохраняем и компелируем....<br>
   также там есть готовый собранный NLS.class и орегенальный NLS.java~ из jadx-gui-1.3.5-with-jre-win текущей на данный момент версии. <br>
   А собирал я так скачал openjdk-18.0.1.1_windows-x64_bin<br>
   в HxD - это хекс редактор под windows<br>
   Разделил jadx-gui-1.3.5.exe с zip частью<br>
   все разложил по папкам и дальше в cmd ввел SET PATH=C:\Users\Serzh\Desktop\jadx-gui-1.3.5-with-jre-win\jdk-18.0.1.1\bin<br>
   и после javac -d class -cp jadx-gui-1.3.5.zip jadx/gui/utils/NLS.java<br>
   закинул из папки class файл NLS.class в jadx/gui/utils/ zip архива<br>
   и после командой COPY /b jadx-gui-1.3.5.exe.bak+jadx-gui-1.3.5.zip jadx-gui-1.3.5_Rus.exe<br>
   Собрал это дело.<br>
