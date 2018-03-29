# RequestInfoStagesControl
> Теги: 3D, визуальные, сложная логика 

Визуальный компонент для отображения информации о состоянии выполнения KPI многоэтапного процесса в разрезе этапов.  

## Основное использование:

Следующий пример демонстрирует RequestInfoStagesControl в действии:

![RequestInfoStagesControl](.screenshots/RequestInfoStagesControl.png)Код примера хранится в файле RequestInfoStagesControl.xml (необходимо определиться с системой хранения стилей, например сейчас подложка под +4 и боковые белые полоски хранятся в проекте газпром и не попали в сборку каталога, так же перепутаны шрифты).

```xml
<RequestInfoStagesControl
                          ParameterName="Id"
                          Padding="0.005"
                          RelativeColumnOffset="0.005"
                          ProcessCondition="InTime"
                          Duration="38"
                          Overtime="4"
                          LeftText="01.02.03"
                          RightText="04.05.06">
  <ProcessStagesList>
    <ProcessStage
                  Id="1"
                  Name="Этап сдан вовремя"
                  StandardTime="1"
                  ActualTime="1"
                  StageCondition="InTime"
                  StageModelId="1"/>
    <ProcessStage
                  Id="2"
                  Name="На этапе получен отказ"
                  StandardTime="7"
                  ActualTime="5"
                  StageCondition="Denied"
                  StageModelId="2"/>
    <ProcessStage
                  Id="3"
                  Name="Ещё один сданный вовремя этап"
                  StandardTime="14"
                  ActualTime="10"
                  StageCondition="InTime"
                  StageModelId="3"/>
    <ProcessStage
                  Id="4"
                  Name="Потрачено"
                  StandardTime="10"
                  ActualTime="12"
                  StageCondition="DeadlineExceededWarning"
                  StageModelId="4"/>
    <ProcessStage
                  Id="5"
                  Name="Полный потрачено"
                  StandardTime="1"
                  ActualTime="1"
                  StageCondition="DeadlineExeededCaution"
                  StageModelId="5"/>
    <ProcessStage
                  Id="6"
                  Name="Этап ещё не начался"
                  StandardTime="1"
                  ActualTime="3"
                  StageCondition="DoesntStartYet"
                  StageModelId="9"/>
  </ProcessStagesList>
</RequestInfoStagesControl>
```

## Свойства компонента:

| **Свойство**             | **Тип**                   | **Описание**                             |
| ------------------------ | ------------------------- | ---------------------------------------- |
| **ProcessStagesList**    |                           | Список этапов процесса.                  |
| **ProcessStage**         | **ProcessStage**          | Раскрашивает части модели в указанные цвета (если трехмерная модель это поддерживает). |
| **OnSelect**             | **Event**                 | Название трехмерной модели.              |
| **ParameterName**        | string                    | Имя параметра события.                   |
| **Padding**              | float                     | Относительный отступ от границ контрола. |
| **RelativeColumnOffset** | float                     | Относительный отступ между столбцами.    |
| **ProcessCondition**     | **ProcessStageCondition** | Состояние процесса в целом.              |
| **Overtime**             | int                       | Нормативное количество дней.             |
| **Duration**             | int                       | Фактичекое количество дней.              |
| **IsIndividual**         | boolean                   | Если true - не рисуем круги.             |

### Описание типа **ProcessStage**

| **Свойство**       | **Тип**                   | **Описание**                             |
| ------------------ | ------------------------- | ---------------------------------------- |
| **Id**             | int                       | Идентификатор этапа процесса.            |
| **Name**           | string                    | Имя этапа процесса.                      |
| **StandardTime**   | string                    | Нормативное количество дней.             |
| **ActualTime**     | string                    | Фактичекое количество дней.              |
| **StageCondition** | **ProcessStageCondition** | Состояние этапа. Принимает одно из предустановленных значений (см. ниже). |
| **StageModelId**   | int                       | ID 3D-модели, отображаемой на кубе этапа. |

### Состояния типа **ProcessStageCondition**

| **Значение**                | **Описание**                             |
| --------------------------- | ---------------------------------------- |
| **DoesntStartYet**          | Этап ещё не начался.                     |
| **InTime**                  | Этап в процессе работы или завершён в срок. |
| **DeadlineExceededWarning** | Срок превышен.                           |
| **DeadlineExceededCaution** | Срок сильно превышен.                    |
| **Denied**                  | Отказ.                                   |

## Команды:

 Отсутствуют.

## Рекомендуемые ссылки:

* [Варианты использования RequestInfoStagesControl](.presentations/README.md)
* [Особенности и приемы работы с RequestInfoStagesControl](README_hints.md)

