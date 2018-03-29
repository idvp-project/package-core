# Варианты использования ImageControl 

Внешний вид ImageControl определяется текстурой - картинкой, загружаемой из графического файла.
Компонент имеет несколько свойств для насторйки отображения и изменения исходного графического файла.

## Изменение размеров картинки

ImageControl имеет возможность независимо растягиваться вдоль осей. Это задается свойством Stretch="true".

![](../.screenshots/ImageControl1.png)

Код примера хранится в файле imagecontrol1.xml.

```xml
<PanelControl ID="ButtonElement">
  <Transform Width="100%" Height="50%" Depth="10%" DepthAlignment="Front" HorizontalAlignment="Center" VerticalAlignment="Center" Margin="0% 0% 15% 0%"/>

  <ImageControl Src="IDVP_logo_01" Stretch="true">
    <Transform Height="30%" Width="100%" Depth="10%" DepthAlignment="Front" VerticalAlignment="Center" HorizontalAlignment="Center"/>
  </ImageControl>

</PanelControl>
```

## Заливка картинки цветом

Картинка может быть залита сплошным цветом, что задается свойством ImageColorARGB. (Планировалась демонстрация IsColored и домножение на цвет)

Код примера хранится в файле imagecontrol2.xml.

![](../.screenshots/ImageControl2.png)



```xml
<PanelControl ID="ButtonElement">
  <Transform Width="100%" Height="50%" Depth="10%" DepthAlignment="Front" HorizontalAlignment="Center" VerticalAlignment="Center" Margin="0% 0% 15% 0%"/>

  <ImageControl Stretch="true" IsColored="true">
    <Transform Height="60%" Width="50%" Depth="10%" DepthAlignment="Front" VerticalAlignment="Center" HorizontalAlignment="Center"/>
    <ImageColorARGB A="255" R="100" G="250" B="100" />
  </ImageControl>

</PanelControl>
```



## Рекомендуемые ссылки:

- [ImageControl Основные сведения](../README.md)
- [Особенности и приемы работы с ImageControl](../README_hints.md)