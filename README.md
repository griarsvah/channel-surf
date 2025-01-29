# channel-surf
Телевизионные каналы на компьютере, смартфоне, планшете

## IPTV (Internet Protocol Television)

## Вцелом Четыре способа:
1. Онлайн-сервисы(просто выбери нужный канал)
2. IPTV
3. ТВ-тюнеры
4. Кабельные и спутниковые провайдеры


## Рассмотрим IPTV
Любой проигрыватель, который умеет работать с IPTV player, OTTPlayer, SS IPTV, VLC Player


## Форматы
Файла - list.m3u
Ссылки - playlist.m3u8

## Создание собственного плейлиста
```
#EXTM3U: Указывает на начало плейлиста.

#EXTINF: Задает продолжительность и название медиафайла в плейлисте.

#EXT-X-VERSION: Указывает версию протокола HLS, используемого в плейлисте.

#EXT-X-TARGETDURATION: Указывает максимальную продолжительность сегмента в плейлисте.

#EXT-X-MEDIA-SEQUENCE: Указывает номер первого сегмента в плейлисте.

#EXT-X-KEY: Указывает метод шифрования и ключ для сегментов.

#EXT-X-STREAM-INF: Указывает информацию о потоке, такую как разрешение и битрейт.

#EXT-X-ENDLIST: Указывает на конец плейлиста.
```

### Разбор кода
```
#EXTM3U url-tvg="http://epg.it999.ru/ru2.xml.gz, https://iptvx.one/epg/epg.xml.gz"
#PLAYLIST:ИмяПлэйлиста
#EXTGRP:ИмяГруппы
#EXTINF:-1 tvg-id="rentv-int" tvg-logo="Путь к иконке.png" group-title="Общественные",ИмяКанала
СсылкаТрансляции.m3u8
```

### Рабочий пример
```
#EXTM3U url-tvg="http://epg.it999.ru/ru2.xml.gz, https://iptvx.one/epg/epg.xml.gz"

#PLAYLIST:IPTVstable
#EXTGRP:Общественные
#EXTINF:-1 tvg-id="pervy" tvg-logo="https://iptvx.one/picons/pervy.png" group-title="Общественные",Первый (HD ready)
https://edge1.1internet.tv/dash-live2/streams/1tv-dvr/1tvdash.mpd

#PLAYLIST:IPTVstable2
#EXTGRP:Общественные2
#EXTINF:-1 tvg-id="mir" tvg-logo="https://iptvx.one/picons/mir.png" group-title="Общественные",Мир (HD)
http://hls.mirtv.cdnvideo.ru/mirtv-parampublish/mirtv_2500/playlist.m3u8
```


## Расширение для браузера хром
https://chromewebstore.google.com/detail/fast-iptv/dbdgibnjfnomhihldbjcdbgddamjmboi


## С помощью проигрывателей
[VLC](https://www.videolan.org/vlc/)


## Онлайн сервисы(нужна только ссылка трансляции)
https://livepush.io/hlsplayer/index.html
https://www.hlsplayer.org/
https://www.downloadhelper.net/
