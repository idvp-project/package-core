# Особенности и приемы работы с ButtonControl

## Использование свойства skin для различных состояний кнопки

Визуальное отображение кнопки (текстура), задается свойством skin и хранится в 2х файлах:

1. Графический файл с несколькими вариантами текстур, соответствующие различным свойствам ButtonControl.

![](screenshots/SKIN_IDVP_comp_01.png)

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



## Рекомендуемые ссылки:

- [ButtonControl Основные сведения](README.md)
- [Варианты использования ButtonControl](README.md)



