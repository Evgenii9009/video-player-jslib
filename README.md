<!-- Плеер будет создан с задержкой, после того как загрузятся все ресурсы на странице. Для этого используется событие `DOMContentLoaded`. Благодаря этой особенности можно вызывать функцию `createPlayer` раньше, чем загрузятся все необходимые библиотеки: jQuery и Playable.
 -->

# Видеоплеер

Пример создания собственного видеоплеера.

Построен на базе библиотеки [Playable](https://wix.github.io/playable/).

## Примеры

Пример работы можно увидеть по [ссылке](https://evgenii9009.github.io/video-player-jslib/index.html)

## Как подключить

JS код поставляется в виде одного файла `player.js`, который нужно скачать из этого репозитория. Для работы он требует двух библиотек - [jQuery](https://jquery.com/) и [Playable](https://wix.github.io/playable/). Пример подключения в браузере:

```html
<script src="https://code.jquery.com/jquery-3.4.1.min.js"></script>
<script src="https://unpkg.com/playable@2.10.3/dist/statics/playable.bundle.min.js"></script>
<script src="player.js"></script>
```

Для работы библиотека требует HTML разметки. Вот полный пример с минимальным количеством настроек:

```html
<div id="player" style="width: 800px; height: 600px;">
    <div class="js-video-container" style="width: 100%; height: 100%"></div>
</div>

<script src="https://code.jquery.com/jquery-3.4.1.min.js"></script>
<script src="https://unpkg.com/playable@2.10.3/dist/statics/playable.bundle.min.js"></script>
<script src="player.js"></script>

<script type="text/javascript">
  createPlayer({elementId: 'player'});
</script>
```

Этот код добавит на страницу плеер, который играет видео по [этой ссылке](https://dvmn.org/media/filer_public/78/db/78db3456-3fd3-4504-9ed9-d2d1fd843c0b/highest_peak.mp4).

Если хочется выбрать другое видео, с помощью аргумента `src` плееру можно указать какое видео проигрывать, ссылки обязаны заканчиваться расширением файла:

```html
<script type="text/javascript">
  createPlayer({
    elementId: 'player',
    src: 'https://dvmn.org/media/filer_public/d0/16/d016d9b8-4180-4bb9-ad83-0241f61627b8/samsung_demo_-_alive_in_color.mp4'
});
</script>
```

**Скрипт `player.js` нужно подключать строго после `<div>` с указанным elementId**


