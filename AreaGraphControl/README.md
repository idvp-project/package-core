# AreaGraphControl
> Теги: 2D, функциональные, визуальные, управляющие элементы, отображение данных

Кнопка предназначена для вызова связанного события при её нажатии пользователем.

## Основное использование:

Следующий пример демонстрирует AreaGraphControl в действии:

![AreaGraphControl](.screenshots/AreaGraphControl.png)

Код примера, приведенного выше хранится в файле AreaGraphControl.xml: 

```xml
<ButtonControl ID="lightbutton" Skin="create_btn" Width="188" Height="68" Visible="true">
</ButtonControl>
```

## Свойства компонента:

Наследуются от [BaseGraphControl](../BaseGraphControl/README.md).



## События:

Наследуются от [BaseGraphControl](../BaseGraphControl/README.md).

## Команды:

| **Команда**        | **Параметры**                        | **Реакция компонента на команды**        |
| ------------------ | ------------------------------------ | ---------------------------------------- |
| **zoomin**         | -                                    | Растягивает график, увеличивая масштаб отображения по оси X. |
| **zoomout**        | -                                    | Сжимает график, уменьшаяет масштаб отображения по оси X. |
| **select**         | @SelectParamKey                      | Передвигает точку на оси X, тег которой соответствует переданному параметру, на правую границу видимой области. |
| **setlegendstate** | @LegendParamKey                      | Переключает видимость графика, соответствущего переданному параметру. |
| **setslider**      | @SliderParamKey                      | Показывает подписи значений графиков, соответствующих точке на оси X, тег которой соответствует переданному параметру. |
| **setlegendtext**  | @LegendParamKey, @LegendTextParamKey | Устанавливает переданный в @LegendTextParamKey текст в качестве подписи для легенды с идентификатором @LegendParamKey. |

## Рекомендуемые ссылки:

* [Варианты использования AreaGraphControl](.presentations/README.md)
* [Особенности и приемы работы с AreaGraphControl](README_hints.md)


