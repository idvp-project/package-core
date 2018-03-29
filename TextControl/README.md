# TextControl
> Теги: 2D, 3D, базовые, визуальные

Компонент для отображения текста на экране.

## Основное использование:

Следующий пример демонстрирует TextControl в действии:

![TextControl](.screenshots/TextControl.PNG)

Код примера, находится в файле textcontrol.xml: 

```xml
<TextControl Is3D="false" Size="20" Text="Hello, World!" PixelSize="50" Anchor="MiddleCenter" Alignment="Center" >
  <Transform Width="80%" Height="80%" Margin="0% 0% 0% 0%" DepthAlignment="Front" Depth="10%" VerticalAlignment="Center" HorizontalAlignment="Center"/>
  <ColorARGB A="255" R="8" G="9" B="15"/>
</TextControl>
```

## Свойства компонента:

| **Свойство**      | **Тип**           | **Описание**                             |
| ----------------- | ----------------- | ---------------------------------------- |
| **ColorARGB**     | **ColorARGB**     | Цвет текста.                             |
| **LineSpacing**   | float             | Межстрочный интервал.                    |
| **Alignment**     | **TextAlignment** | По какому краю должен быть выравнен текст. |
| **Anchor**        | **TextAnchor**    | Точка, относительно которой текст будет рисоваться. |
| **ZAnchor**       | string            | Выравнивание текста по глубине.          |
| **Material**      | string            | Имя материала.                           |
| **Is3D**          | boolean           | Будет ли текст в 3D.                     |
| **Font**          | string            | Шрифт текста.                            |
| **Size**          | float             | Размер текста.                           |
| **ExtrudeDepth**  | float             | Глубина выдавливания трехмерного текста. |
| **PixelSize**     | int               | Базовый размер каждого символа шрифта в пикселях. |
| **Text**          | string            | Текст, который должен отобразиться на экране. |
| **AlignToBounds** | boolean           | Будет ли изменен фактический размер текста для размещения данного текста в области текущего контрола. |
| **TextKey**       | string            | Имя параметра для команды **changetext**. |
| **Angle**         | float             | Угол поворота текста.                    |

## События:

Отсутствуют.

## Команды:

| **Команда**    | **Параметры** | **Реакция компонента на команды** |
| -------------- | ------------- | --------------------------------- |
| **changetext** | TextKey       | Изменение текста.                 |

## Рекомендуемые ссылки:

* [Варианты использования TextControl](.presentations/README.md)
* [Особенности и приемы работы с TextControl](README_hints.md)


