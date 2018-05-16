# DeckPerson
> Теги: -

Тип данных, хранящий в себе информацию о строке пузырьковой тепловой карты.

Код примера использования DeckPerson:

```xml
{% include_relative presentations/presentation.xml %}
```

DeckPerson наследуется от Bindable.


## Свойства:

| **Свойство**                  | **Тип**                     | **Описание**                             |
| ----------------------------- | --------------------------- | ---------------------------------------- |
| **Cells**                     | **[DeckCell](../DeckCell/README.md)**| Коллекция ячеек внутри строки. Кажадя ячейка является "лотком" с шарами.|
| **ID**                        | string                      | Идентификатор строки.                    |
| **FirstName**                 | string                      | Первая строка заголовка строки.          |
| **FamilyName**                | string                      | Вторая строка заголовка строки.          |
| **IsClickable**               | boolean                     | Установка разрешения на кликабельность заголовка строки.|



## События:

Отсутствуют.


## Команды:

Отсутствуют.


## Схема:

```xml
<xs:schema version="1.0" xmlns:xs="http://www.w3.org/2001/XMLSchema">
<xs:complexType name="DeckPerson">
 <xs:complexContent>
  <xs:extension base="Bindable">
   <xs:sequence>
    <xs:element maxOccurs="unbounded" minOccurs="0" name="Cells" type="DeckCell" />
   </xs:sequence>
   <xs:attribute name="ID" type="xs:string" use="required" />
   <xs:attribute name="FirstName" type="xs:string" use="required" />
   <xs:attribute name="FamilyName" type="xs:string" use="required" />
   <xs:attribute default="false" name="IsClickable" type="xs:boolean" />
  </xs:extension>
 </xs:complexContent>
</xs:complexType>
</xs:schema>
```


## Рекомендуемые ссылки:

Отсутствуют.

