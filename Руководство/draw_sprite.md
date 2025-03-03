# draw_sprite

*[Оригинальная статья.](https://manual.gamemaker.io/beta/en/index.htm#t=GameMaker_Language%2FGML_Reference%2FDrawing%2FSprites_And_Tiles%2Fdraw_sprite.htm)*

---

Эта функция выводит указанный спрайт и его подизображение (кадр) в определённую позицию внутри комнаты. В качестве спрайта можно использовать переменную экземпляра [**`sprite_index`**](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Instance_Variables/sprite_index.htm), чтобы отрисовать текущий спрайт, назначенный экземпляру, или любой другой спрайт из ассетов проекта. То же самое касается подизображения: вы можете указать переменную [**`image_index`**](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Instance_Variables/image_index.htm), чтобы взять текущий кадр анимации, либо использовать конкретное число для вывода нужного подизображения выбранного спрайта.

Если число, заданное для подизображения, превышает фактическое количество кадров спрайта, GameMaker автоматически зацикливает его. Например, если у спрайта 5 кадров (пронумерованные как от 0 до 4), а вы указали подизображение 7, будет выведен кадр с индексом 2. Наконец, координаты x и y определяют, где в комнате будет нарисован спрайт. При этом спрайт центрируется по смещениям [**`sprite_xoffset`**](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Instance_Variables/sprite_xoffset.htm) и [**`sprite_yoffset`**](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Instance_Variables/sprite_yoffset.htm).

> **Примечание:** при работе со спрайтами с анимацией скелета эта функция может вести себя непредсказуемо, выводя только первый кадр стандартной позы. В таких случаях используйте функции вида **`draw_skeleton_*`**.

## Синтаксис

```gml
draw_sprite(sprite, subimg, x, y);
```

| Аргумент | Тип | Описание |
| --- | --- | --- |
| sprite | [Sprite Asset](https://manual.gamemaker.io/beta/en/The_Asset_Editors/Sprites.htm) | Спрайт, который нужно отрисовать |
| subimg | [Real](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Overview/Data_Types.htm) | Номер подизображения (кадра) спрайта (может быть `image_index` или `-1` для текущего кадра анимации в объекте). |
| x      | [Real](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Overview/Data_Types.htm) | Координата x, где нужно нарисовать спрайт |
| y      | [Real](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Overview/Data_Types.htm) | Координата y, где нужно нарисовать спрайт |

## Возвращаемое значение

*(Функция не возвращает никаких значений.)*

## Пример

```gml
draw_sprite(sprite_index, image_index, x, y);
draw_sprite(spr_Halo, 0, x, y - 32);
```

В этом примере сначала выводится спрайт экземпляра (`sprite_index`) с текущим подизображением (`image_index`) по координатам `x` и `y`. Затем поверх него на 32 пикселя выше рисуется первый кадр спрайта `spr_Halo`.

---

* назад: [«Спрайты и тайлы»](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Reference/Drawing/Sprites_And_Tiles/Sprites_And_Tiles.htm);
* далее: [«draw_sprite_ext»](https://manual.gamemaker.io/beta/en/GameMaker_Language/GML_Reference/Drawing/Sprites_And_Tiles/draw_sprite_ext.htm).
