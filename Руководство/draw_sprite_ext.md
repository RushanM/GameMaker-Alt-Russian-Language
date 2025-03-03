# draw_sprite_ext

[*Оригинальная статья.*](https://manual.gamemaker.io/beta/en/index.htm#t=GameMaker_Language%2FGML_Reference%2FDrawing%2FSprites_And_Tiles%2Fdraw_sprite_ext.htm&rhsearch=draw_sprite_ext&rhhlterm=draw_sprite_ext)

---

Эта функция работает так же, как [**draw_sprite**](https://github.com/RushanM/GameMaker-Alt-Russian-Language/blob/main/%D0%A0%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE/draw_sprite.md), но дополнительно позволяет изменять масштаб, цветовую заливку, угол поворота и прозрачность отрисовываемого спрайта. Изменения этих значений *никак* не затрагивают исходный ресурс — меняется только то, как спрайт отображается. Для всех аргументов можно использовать [переменные, связанные со спрайтом](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Instance_Variables/Sprite_Instance_Variables.htm). На изображении ниже показано, как различные параметры влияют на вывод спрайта:

<p align="center">
    <img src="https://manual.gamemaker.io/beta/en/assets/Images/Scripting_Reference/GML/Reference/Drawing/spr_ext.png">
</p>

> **Примечание:** не рекомендуется использовать смешивание цветов на HTML5 при выключенном WebGL. Без WebGL установка цвета смешения по-прежнему возможна, но GameMaker при этом создаёт копию спрайта и помещает её в кэш, что при постоянных изменениях цвета может сильно повлиять на производительность. Если вы не хотите включать WebGL, можно уменьшить влияние этого эффекта, настроив размер кэша спрайтов с помощью функции [**`sprite_set_cache_size()`**](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Manipulation/sprite_set_cache_size_ext.htm).

> **Примечание:** при использовании спрайтов со скелетной анимацией эта функция может работать некорректно, отображая только первый кадр стандартной позы. В таких случаях следует применять функции вида **`draw_skeleton_*`**.

## Синтаксис

```gml
draw_sprite_ext(sprite, subimg, x, y, xscale, yscale, rot, colour, alpha);
```

| Аргумент | Тип | Описание |
| --- | --- | --- |
| sprite   | [**Спрайтовый ассет**](https://manual.gamemaker.io/beta/en/The_Asset_Editors/Sprites.htm) | Спрайт, который нужно отрисовать |
| subimg   | [**Вещественное число**](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Overview/Data_Types.htm) | Индекс подизображения (кадра) спрайта (можно использовать `image_index` или `-1` для текущего кадра анимации экземпляра) |
| x        | [**Вещественное число**](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Overview/Data_Types.htm) | Координата **x**, где нужно нарисовать спрайт |
| y        | [**Вещественное число**](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Overview/Data_Types.htm) | Координата **y**, где нужно нарисовать спрайт |
| xscale   | [**Вещественное число**](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Overview/Data_Types.htm) | Горизонтальный масштаб (1 = без изменений, 0.5 = вдвое меньше и т. д.) |
| yscale   | [**Вещественное число**](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Overview/Data_Types.htm) | Вертикальный масштаб (1 = без изменений, 0.5 = вдвое меньше и т. д.) |
| rot      | [**Вещественное число**](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Overview/Data_Types.htm) | Угол поворота спрайта (0 = без поворота, 90 = поворот на 90° против часовой стрелки и т.д.) |
| colour   | [**Цвет**](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha.htm) | Цвет, которым будет залит спрайт (например, `c_white` для вывода без изменений) |
| alpha    | [**Вещественное число**](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Overview/Data_Types.htm) | Прозрачность (0 = полностью прозрачно, 1 = непрозрачно) |

## Возвращаемое значение

*(Функция не возвращает никаких значений.)*

## Пример

```gml
draw_sprite_ext(sprite_index, image_index, x, y, image_xscale, image_yscale, image_angle, image_blend, image_alpha);
```

Данный пример отрисовывает спрайт экземпляра со всеми параметрами по умолчанию (по сути, то же самое, что вызов **`draw_self`**).

---

* назад: [«Спрайты и тайлы»](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Reference/Drawing/Sprites_And_Tiles/Sprites_And_Tiles.htm);
* далее: [«draw_sprite_general»](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Reference/Drawing/Sprites_And_Tiles/draw_sprite_general.htm).
