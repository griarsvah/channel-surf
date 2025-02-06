# channel-surf
Телевизионные каналы на компьютере, смартфоне, планшете

## IPTV (Internet Protocol Television)

## Вцелом четыре способа:
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

### Минимальный код
```
#EXTM3U

#EXTINF:-1, Первый (HD ready)
https://edge1.1internet.tv/dash-live2/streams/1tv-dvr/1tvdash.mpd

#EXTINF:-1, Мир (HD)
http://hls.mirtv.cdnvideo.ru/mirtv-parampublish/mirtv_2500/playlist.m3u8
```

### Добавим возможность групировать
```
#EXTM3U

#EXTINF:-1, Первый (HD ready)
#EXTGRP:Общественные
https://edge1.1internet.tv/dash-live2/streams/1tv-dvr/1tvdash.mpd

#EXTINF:-1, Рен ТВ
#EXTGRP:Общие
http://ad-hls-rentv.cdnvideo.ru/ren/smil:ren.smil/playlist.m3u8
```

### Добавим иконки
```
#EXTM3U

#EXTINF:-1 tvg-logo="https://iptvx.one/picons/pervy.png", Первый (HD ready)
#EXTGRP:Общественные
https://edge1.1internet.tv/dash-live2/streams/1tv-dvr/1tvdash.mpd

#EXTINF:-1 tvg-logo="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT0EGi4FTU0XG3__lvnQjoPUQ8R72MIaRRBDQ&s", Рен ТВ
#EXTGRP:Общие
http://ad-hls-rentv.cdnvideo.ru/ren/smil:ren.smil/playlist.m3u8
```


### Рабочий пример
```
#EXTM3U url-tvg="http://epg.it999.ru/ru2.xml.gz, https://iptvx.one/epg/epg.xml.gz"

#EXTINF:-1 tvg-id="pervy" tvg-logo="https://iptvx.one/picons/pervy.png" group-title="Общественные",Первый (HD ready)
#EXTGRP:Общественные
https://edge1.1internet.tv/dash-live2/streams/1tv-dvr/1tvdash.mpd

#EXTINF:-1 tvg-id="mir" tvg-logo="https://iptvx.one/picons/mir.png" group-title="Общественные",Мир (HD)
#EXTGRP:Общественные2
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
