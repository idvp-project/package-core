# HeatBubbleSourceControl
> Теги: -

Компонент, создающий структуру данных для пузырьковой тепловой карты.

## Основное использование:

Следующий пример демонстрирует HeatBubbleSourceControl в действии:

![HeatBubbleSourceControl](screenshots/presentation.png)

Код примера использования HeatBubbleSourceControl:

```xml
{% include_relative presentations/presentation.xml %}
```

HeatBubbleSourceControl наследуется от Control.


## Свойства:

| **Свойство**                  | **Тип**                     | **Описание**                             |
| ----------------------------- | --------------------------- | ---------------------------------------- |
| **Persons**                   | **[DeckPerson](../DeckPerson/README.md)**| Коллекция строк таблицы, содержащей "лотки" с шарами.|
| **ColumnCaptions**            | **[DeckColumn](../DeckColumn/README.md)**| Подписи к колонкам (отображаемые внизу тепловой карты).|
| **error**                     | string                      | В шаблонах не используется.              |
| **ColumnsCount**              | int                         | Количество колонок.                      |
| **RowsCount**                 | int                         | Количество строк.                        |
| **RowsCaption**               | string                      | Подписи к строкам.                       |
| **MainCaption**               | string                      | Заголовок компонента.                    |



## События:

Отсутствуют.


## Команды:

Отсутствуют.


## Схема:

```xml
<xs:schema version="1.0" xmlns:xs="http://www.w3.org/2001/XMLSchema">
<xs:complexType name="HeatBubbleSourceControl">
 <xs:complexContent>
  <xs:extension base="Control">
   <xs:sequence>
    <xs:element maxOccurs="unbounded" minOccurs="0" name="Persons" type="DeckPerson" />
    <xs:element maxOccurs="unbounded" minOccurs="0" name="ColumnCaptions" type="DeckColumn" />
   </xs:sequence>
   <xs:attribute default="" name="error" type="xs:string" />
   <xs:attribute name="ColumnsCount" type="xs:int" use="required" />
   <xs:attribute name="RowsCount" type="xs:int" use="required" />
   <xs:attribute default="Заголовок;столбцов" name="RowsCaption" type="xs:string" />
   <xs:attribute default="Заголовок виджета" name="MainCaption" type="xs:string" />
  </xs:extension>
 </xs:complexContent>
</xs:complexType>
</xs:schema>
```


## Рекомендуемые ссылки:

* [Варианты использования HeatBubbleSourceControl](presentations.md)
* [Особенности и приемы работы с HeatBubbleSourceControl](hints.md)

