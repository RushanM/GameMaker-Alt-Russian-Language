# application_surface

[*Оригинальная статья.*](https://manual.gamemaker.io/beta/en/index.htm?#t=GameMaker_Language%2FGML_Reference%2FDrawing%2FSurfaces%2Fapplication_surface.htm)

---

Эта глобальная встроенная переменная позволяет получить доступ к **поверхности приложения** для использования в любых функциях работы с поверхностями. Эта поверхность всегда доступна и именно на ней GameMaker отрисовывает игру.

Обычные события отрисовки (*«При начале отрисовки»*, *«При отрисовке»* и *«В конце отрисовки»*) по умолчанию выводят всё на эту поверхность. Другие события отрисовки (например, *«Перед отрисовкой»*, *«После отрисовки»* и *«При отрисовке слоя интерфейса»*) не используют поверхность приложения. Дополнительную информацию о работе этих событий см. в разделе [«События отрисовки»](https://github.com/RushanM/GameMaker-Alt-Russian-Language/blob/main/Руководство/%D0%A1%D0%BE%D0%B1%D1%8B%D1%82%D0%B8%D1%8F%20%D0%BE%D1%82%D1%80%D0%B8%D1%81%D0%BE%D0%B2%D0%BA%D0%B8.md).

## Синтаксис

```gml
application_surface
```

## Возвращаемое значение

```gml
Surface
```

## Пример

```gml
var _cam_width = 320;
var _cam_height = 180;
var _resolution_scale = 4;

surface_resize(application_surface, _cam_width * _resolution_scale, _cam_height * _resolution_scale);
```

Данный пример задаёт размер игровой камеры (320 × 180) и коэффициент масштабирования разрешения (4x), то есть во сколько раз целевое разрешение должно быть больше размеров камеры. Размер камеры умножается на этот коэффициент и применяется как размер поверхности приложения, определяющий разрешение игры.

---

* назад: [«Поверхности»](https://github.com/RushanM/GameMaker-Alt-Russian-Language/blob/main/Руководство/Поверхности.md);
* далее: [«application_surface_enable»](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Reference/Drawing/Surfaces/application_surface_enable.htm).
