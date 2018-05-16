# DeckBubble
> Теги: -

Тип данных, хранящий в себе информацию о шаре пузырьковой тепловой карты.

Код примера использования DeckBubble:

```xml
{% include_relative presentations/presentation.xml %}
```

DeckBubble наследуется от Bindable.


## Свойства:

| **Свойство**                  | **Тип**                     | **Описание**                             |
| ----------------------------- | --------------------------- | ---------------------------------------- |
| **Info**                      | **[DeckBubbleInfo](../DeckBubbleInfo/README.md)**| Объект, содержащий краткую информацию о шаре.|
| **ID**                        | string                      | Идентификатор шара.                      |
| **Size**                      | float                       | Размер шара.                             |
| **Color**                     | ***Color***                 | Цвет шара.                               |
| **Cost**                      | double                      | Стоимость шара.                          |

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
<xs:complexType name="DeckBubble">
 <xs:complexContent>
  <xs:extension base="Bindable">
   <xs:sequence>
    <xs:element minOccurs="0" name="Info" type="DeckBubbleInfo" />
   </xs:sequence>
   <xs:attribute name="ID" type="xs:string" use="required" />
   <xs:attribute default="0" name="Size" type="xs:float" />
   <xs:attribute default="Red" name="Color" type="Color" />
   <xs:attribute default="0" name="Cost" type="xs:double" />
  </xs:extension>
 </xs:complexContent>
</xs:complexType>
</xs:schema>
```


## Рекомендуемые ссылки:

Отсутствуют.

