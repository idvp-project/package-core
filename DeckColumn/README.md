# DeckColumn
> Теги: -

Тип данных, хранящий в себе информацию о колонке пузырьковой тепловой карты.

Код примера использования DeckColumn:

```xml
{% include_relative presentations/presentation.xml %}
```

DeckColumn наследуется от Bindable.


## Свойства:

| **Свойство**                  | **Тип**                     | **Описание**                             |
| ----------------------------- | --------------------------- | ---------------------------------------- |
| **ColumnCaption**             | string                      | Заголовок столбца.                       |
| **ID**                        | string                      | Идентификатор столбца.                   |
| **IsClickable**               | boolean                     | Установка разрешения на кликабельность заголовка столбца.|



## События:

Отсутствуют.


## Команды:

Отсутствуют.


## Схема:

```xml
<xs:schema version="1.0" xmlns:xs="http://www.w3.org/2001/XMLSchema">
<xs:complexType name="DeckColumn">
 <xs:complexContent>
  <xs:extension base="Bindable">
   <xs:sequence>
   </xs:sequence>
   <xs:attribute default="" name="ColumnCaption" type="xs:string" />
   <xs:attribute default="columncaptionid" name="ID" type="xs:string" />
   <xs:attribute default="false" name="IsClickable" type="xs:boolean" />
  </xs:extension>
 </xs:complexContent>
</xs:complexType>
</xs:schema>
```


## Рекомендуемые ссылки:

Отсутствуют.

