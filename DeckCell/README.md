# DeckCell
> Теги: -

Тип данных, хранящий в себе информацию о ячейке пузырьковой тепловой карты.

Код примера использования DeckCell:

```xml
{% include_relative presentations/presentation.xml %}
```

DeckCell наследуется от Bindable.


## Свойства:

| **Свойство**                  | **Тип**                     | **Описание**                             |
| ----------------------------- | --------------------------- | ---------------------------------------- |
| **Bubbles**                   | **[DeckBubble](../DeckBubble/README.md)**| Коллекция шаров внутри ячейки.           |
| **ID**                        | string                      | Идентификатор ячейки.                    |



## События:

Отсутствуют.


## Команды:

Отсутствуют.


## Схема:

```xml
<xs:schema version="1.0" xmlns:xs="http://www.w3.org/2001/XMLSchema">
<xs:complexType name="DeckCell">
 <xs:complexContent>
  <xs:extension base="Bindable">
   <xs:sequence>
    <xs:element maxOccurs="unbounded" minOccurs="0" name="Bubbles" type="DeckBubble" />
   </xs:sequence>
   <xs:attribute name="ID" type="xs:string" use="required" />
  </xs:extension>
 </xs:complexContent>
</xs:complexType>
</xs:schema>
```


## Рекомендуемые ссылки:

Отсутствуют.

