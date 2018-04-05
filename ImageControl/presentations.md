# Варианты использования ImageControl 

Внешний вид ImageControl определяется текстурой - картинкой, загружаемой из графического файла.
Компонент имеет несколько свойств для насторйки отображения и изменения исходного графического файла.

## Изменение размеров картинки

ImageControl имеет возможность независимо растягиваться вдоль осей. Это задается свойством Stretch="true".

![](screenshots/presentation1.png)

Код примера хранится в файле presentation1.xml.

```xml
{% include_relative presentations/presentation1.xml %}
```

## Заливка картинки цветом

Картинка может быть залита сплошным цветом, что задается свойством ImageColorARGB. (Планировалась демонстрация IsColored и домножение на цвет)

Код примера хранится в файле presentation2.xml.

![](screenshots/presentation2.png)



```xml
{% include_relative presentations/presentation2.xml %}
```



## Рекомендуемые ссылки:

- [ImageControl Основные сведения](README.md)
- [Особенности и приемы работы с ImageControl](hints.md)