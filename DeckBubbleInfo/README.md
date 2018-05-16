# DeckBubbleInfo
> Теги: -

Тип данных, хранящий в себе краткую информацию об объекте, представленного в виде шара на пузырьковой тепловой карты.

Код примера использования DeckBubbleInfo:

```xml
{% include_relative presentations/presentation.xml %}
```

DeckBubbleInfo наследуется от Bindable.


## Свойства:

| **Свойство**                  | **Тип**                     | **Описание**                             |
| ----------------------------- | --------------------------- | ---------------------------------------- |
| **ClientNameCaption**         | string                      | Название категории названия клиента шара.|
| **ClientNameValue**           | string                      | Название клиента шара.                   |
| **ManagerNameCaption**        | string                      | Название категории ФИО менеджера шара.   |
| **ManagerNameValue**          | string                      | ФИО менеджера шара.                      |



## События:

Отсутствуют.


## Команды:

Отсутствуют.


## Схема:

```xml
<xs:schema version="1.0" xmlns:xs="http://www.w3.org/2001/XMLSchema">
<xs:complexType name="DeckBubbleInfo">
 <xs:complexContent>
  <xs:extension base="Bindable">
   <xs:sequence/>
   <xs:attribute default="" name="ClientNameCaption" type="xs:string" />
   <xs:attribute default="" name="ClientNameValue" type="xs:string" />
   <xs:attribute default="" name="ManagerNameCaption" type="xs:string" />
   <xs:attribute default="" name="ManagerNameValue" type="xs:string" />
  </xs:extension>
 </xs:complexContent>
</xs:complexType>
</xs:schema>
```


## Рекомендуемые ссылки:

Отсутствуют.

