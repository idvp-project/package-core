# Варианты использования MeshControl 

Внешний вид MeshControl определяется 3D моделью, которая загружена в него. Модели могут отличаться сложностью, материалами, цветами и размерами.

Ниже приведено несколько вариантов использования MeshControl. Варианты использования демонстрируют примеры загрузки различных моделей и несколько типичную реакций MeshControl на нажатие.

## Анимация камеры при нажатии на MeshControl 

![](../.screenshots/IDVP_01_default_button.png)

```xml
<ButtonControl ID="lightbutton" Skin="invisible" Visible="true">
       <Transform Depth="40%" DepthAlignment="Front"/>
       <Event Name="BigButtonClearClick"/>
       <ImageControl Src="Main_btn_01" Stretch="true" >
           <Transform Width="100%" Height="100%" Depth="10%" HorizontalAlignment="Center"/>
       </ImageControl>
</ButtonControl>
```

## Изменение цвета модели

Кнопка с текстом ОК и небольшой иконкой вначале или рамкой вокруг

Код этого примера.



## Рекомендуемые ссылки:

- [MeshControl Основные сведения](../README.md)
- [Особенности и приемы работы с MeshControl](../README_hints.md)