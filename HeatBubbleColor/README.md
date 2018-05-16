# HeatBubbleColor
> Теги: -

Тип данных, хранящий в себе цвет для использования в пузырьковой тепловой карты.

Код примера использования HeatBubbleColor:

```xml
{% include_relative presentations/presentation.xml %}
```

HeatBubbleColor наследуется от Bindable.


## Свойства:

| **Свойство**                  | **Тип**                     | **Описание**                             |
| ----------------------------- | --------------------------- | ---------------------------------------- |
| **Color**                     | ***Color***                 | Параметр цвета для использования в пузырьковой тепловой карты.|

#### Варианты значений Color:
* **Unknown** - -
* **Green** - -
* **DarkGreen** - -
* **Red** - -
* **Yellow** - -
* **Gray** - -
* **DarkGray** - -
* **LightGray** - -
* **LimeGreen** - -
* **Transparent** - -
* **Crimson** - -
* **CrimsonGlory** - -
* **Citrine** - -
* **Vinous** - -
* **White** - -
* **Blue** - -
* **Pink** - -
* **Orange** - -
* **DirtyOrange** - -
* **DeepPurple** - -
* **Purple** - -
* **LightPurple** - -
* **Lust** - -
* **Aqua** - -
* **Black** - -
* **Water** - -
* **Salad** - -
* **Carrot** - -
* **Swamp** - -
* **Magenta** - -
* **Sky** - -



## События:

Отсутствуют.


## Команды:

Отсутствуют.


## Схема:

```xml
<xs:schema version="1.0" xmlns:xs="http://www.w3.org/2001/XMLSchema">
<xs:complexType name="HeatBubbleColor">
 <xs:complexContent>
  <xs:extension base="Bindable">
   <xs:sequence>
   </xs:sequence>
   <xs:attribute name="Color" type="Color" use="required" />
  </xs:extension>
 </xs:complexContent>
</xs:complexType>
</xs:schema>
```


## Рекомендуемые ссылки:

Отсутствуют.

