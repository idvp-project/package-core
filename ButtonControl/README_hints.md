# Особенности и приемы работы с ButtonControl

## Использование свойства skin для различных состояний кнопки

Визуальное отображение кнопки (текстура), задается свойством skin и хранится в 2х файлах:

1. Графический файл с несколькими вариантами текстур, соответствующие различным свойствам ButtonControl.

![](Screenshots/SKIN_IDVP_comp_01.png)

2. Файл skin.xml, содержащий текстурный атлас, определяющий области внутри графического файла, соответствующие определенным состояниям.

```xml
  <Resource type="ResourceSkin" name="main_btn" size="85 85" texture="SKIN_IDVP_comp_01.png">
        <BasisSkin type="SubSkin" offset="0 0 85 85" align="Stretch">
            <State name="normal" offset="0 0 85 85"/>
            <State name="pushed" offset="86 0 85 85"/>
        </BasisSkin>
  </Resource>
```

После того, как текстуры определены, при смене состояния кнопки автоматически меняется и текстура соответсвующая этому состоянию.

ToDo:

1. нужно вставить реальный код для кнопки и описать почему выше <State name="pushed").
2. Исправить растяжение скинов как в тоггле

```xml
  <Resource type="ResourceSkin" name="main_btn" size="85 85" texture="SKIN_IDVP_comp_01.png">
        <BasisSkin type="SubSkin" offset="0 0 85 85" align="Stretch">
            <State name="normal" offset="0 0 85 85"/>
            <State name="pushed" offset="86 0 85 85"/>
        </BasisSkin>
  </Resource>
```



## ToggleButton

Для реализации toggle кнопки или кнопки-переключателя, которая меняет свое состояние по клику и вовзращается в исходное по второму клику, применяется следующий прием: создается 2 кнопки, расположенные одна под другой.

![buttoncontrol_toggle_button](Screenshots/buttoncontrol_toggle_button.png)

Пример кода с реализацией toggle кнопки:

```xml
<ButtonControl ID="lightbutton" Skin="slider_on_off" Width="188" Toggle="true" Height="68" Visible="true">
      <Transform Depth="40%" DepthAlignment="Front"/>
</ButtonControl>
```

Видно, что свойство Toggle="true", что запускает кнопку в режиме переключатель. Это обеспечивает переключение скинов при нажатии. Для того, чтобы скины переключались их необходимо подготавливать и хранить в формате описанном выше в параграфе "Использование свойства skin для различных состояний кнопки".



## Рекомендуемые ссылки:

- [ButtonControl Основные сведения](README.md)
- [Варианты использования ButtonControl](README_usage.md)



