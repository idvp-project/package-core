# Варианты использования ButtonControl 

Внешний вид ButtonControl определяется текстурой - картинкой, загружаемой из графического файла.
Текстура может значительно отличаться в зависимости от дизайна приложения.

Ниже приведено несколько оригинальных кнопок, которые показывают
разнообразие визуальных вариантов и помогут вам с идеями при создании дизайна собственного приложения.

## Объемная кнопка

Эффект трехмерности в кнопке достигается использованием в кнопке текстуры стилизированной под 3D, которая размещается внутри кнопки с помощью дополнительного вложенного компонента ImageControl.

![](../screenshots/volume_button.png)

```xml
<ButtonControl ID="lightbutton" Skin="invisible" Visible="true">
       <Transform Depth="40%" DepthAlignment="Front"/>
       <Event Name="BigButtonClearClick"/>
       <ImageControl Src="Main_btn_01" Stretch="true" >
           <Transform Width="100%" Height="100%" Depth="10%" HorizontalAlignment="Center"/>
       </ImageControl>
</ButtonControl>
```

## Кнопка-переключатель

Для создания кнопки-переключателя (toggle button) используется слудующий прием: одна под одной создается две кнопки сответсвенно с текстурой первого и второго состояния, которые при нажаитии меняют статус видлимости на противоположный. 

![](../screenshots/buttoncontrol_toggle_button.png)



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