# Варианты использования RequestInfoStagesControl 

Внешний вид RequestInfoStagesControl определяется 3D моделью, которая загружена в него. Модели могут отличаться сложностью, материалами, цветами и размерами.

Ниже приведено несколько вариантов использования RequestInfoStagesControl. Варианты использования демонстрируют примеры загрузки различных моделей и несколько типичную реакций MeshControl на нажатие.

## Изменение цветов модели 

За раскрашивание частей модели отвечает сложное свойство **ProcessStage**.

Свойство **StageCondition** будет определять цвета кубов (частей) модели, а за смену цветов для кружка в блоке под каждым из кубов отвечает свойство **ProcessCondition**.

Возможные значения свойства **StageCondition** и соответствующие им цвета: 

| Значение                | Цвет    |
| ----------------------- | ------- |
| Denied                  | серый   |
| DoesntStartYet          | синий   |
| InTime                  | зелёный |
| DeadlineExceededWarning | жёлтый  |
| DeadlineExeededCaution  | красный |

В случае, если значение **StageCondition** равно ***DeadlineExeededCaution***, блок под кубом окрасится в красный цвет, во всех остальных случаях он имеет синий цвет.

![](screenshots/no_image.png)

Код этого примера.

```xml

```



## Изменение текста модели

Текст плашек справа и слева от модели редактируется посредством свойств **RightText, LeftText,**  а также с помощью сложного свойства **ProcessStage**.

За изменение текста частей модели и их количественные параметры изменяются посредством сложного свойства **ProcessStage**.

![](screenshots/no_image.png)

Код этого примера.

```xml

```



## Изменение количества частей модели

Количество частей модели формируется согласно количеству свойств сложного свойства ProcessStageCondition. Размеры частей задаются из верстки.

При изменении набора свойств свойства **ProcessStageCondition** изменяется количество частей.

Между частями модели можно установить размер зазора с помощью свойства **RelativeColumnOffset**.

Если количество частей  модели больше, чем возможно для отображаения в стандартных размерах кубов модели, кубы масштабираются, чтобы все части поместились.



![](screenshots/no_image.png)

Код этого примера.

```xml

```



## Изменение минимоделей

За минимодели, расположенные над частями основной модели отвечает свойство **StageModelId**.

![](screenshots/no_image.png)

Код этого примера.

```xml

```





## Рекомендуемые ссылки:

- [RequestInfoStagesControl Основные сведения](README.md)
- [Особенности и приемы работы с RequestInfoStagesControl](hints.md)