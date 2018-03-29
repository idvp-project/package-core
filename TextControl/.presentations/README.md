# Варианты использования TextControl 

Текст один из наиболее популярных элементов интерфейса, поэтому TextControl имеет множество настроек для форматирования выводимого текста. Ниже приведено несколько демонстрационных примеров по форматированию текста.

## Объемный текст

Эффект трехмерности теста достигается свойством is3D=true. При работе с трехмерным текстом важно учитывать положение камеры. 

![](../.screenshots/textcontrol1.png)

```xml
<PanelControl ID="TextElement">
  <Transform Width="30%" Height="50%" Depth="10%" DepthAlignment="Front" HorizontalAlignment="Center" VerticalAlignment="Center" Margin="0% 0% 15% 0%"/>

  <TextControl Is3D="true" Size="20" Text="Hello, World!" PixelSize="50" Anchor="MiddleCenter" Alignment="Center" ExtrudeDepth="2">
    <Transform Width="80%" Height="80%" Margin="0% 0% 0% 0%" DepthAlignment="Front" Depth="10%" VerticalAlignment="Center" HorizontalAlignment="Center"/>
    <ColorARGB A="255" R="8" G="9" B="15"/>
  </TextControl>

</PanelControl>
```

## Форматированный текст

Для создания кнопки-переключателя (toggle button) используется слудующий прием: одна под одной создается две кнопки сответсвенно с текстурой первого и второго состояния, которые при нажаитии меняют статус видлимости на противоположный. 

![](../.screenshots/buttoncontrol_toggle_button.png)



```xml
<PanelControl ID="ButtonElement">
  <Transform Width="20%" Height="40%" Depth="10%" DepthAlignment="Front" HorizontalAlignment="Center" VerticalAlignment="Center" Margin="0% 0% 15% 0%"/>
  <ButtonControl ID="lightbutton" Skin="invisible" Visible="true">
    <Transform Depth="40%" DepthAlignment="Front"/>
    <Event Name="BigButtonClearClick"/>
    <ImageControl Src="Main_btn_01" Stretch="true" >
      <Transform Width="100%" Height="100%" Depth="10%" HorizontalAlignment="Center"/>
    </ImageControl>
  </ButtonControl>
  <ButtonControl ID="pushedbutton" Skin="invisible" Visible="false">
    <Transform Depth="40%" DepthAlignment="Front"/>
    <Event Name="BigButtonPushedClick"/>
    <ImageControl Src="Main_btn_pushed_01" Stretch="true" >
      <Transform Width="100%" Height="100%" Depth="10%" HorizontalAlignment="Center"/>
    </ImageControl>
  </ButtonControl>
</PanelControl>
```

## Кнопка с текстом

Добавление текста в кнопку, например надписи "ОК" осуществляется размещением компонента TextControl внутри компонента ButtonControl.

Код этого примера.



## Рекомендуемые ссылки:

- [ButtonControl Основные сведения](../README.md)
- [Особенности и приемы работы с ButtonControl](../README_hints.md)