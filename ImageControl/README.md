# ImageControl
> Теги: 2D, базовые, визуальные

Компонент для отображения графических файлов.

## Основное использование:

Следующий пример демонстрирует ImageControl в действии:

![ImageControl](.screenshots/imagecontrol.PNG)

Код примера, находится в файле ImageControl.png: 

```xml
<PanelControl ID="ButtonElement">
  <Transform Width="100%" Height="50%" Depth="10%" DepthAlignment="Front" HorizontalAlignment="Center" VerticalAlignment="Center" Margin="0% 0% 15% 0%"/>

  <ImageControl Src="IDVP_logo_01" Stretch="true">
    <Transform Height="60%" Width="50%" Depth="10%" DepthAlignment="Front" VerticalAlignment="Center" HorizontalAlignment="Center"/>
  </ImageControl>

</PanelControl>
```

## Свойства компонента:

| **Свойство**       | **Тип**                    | **Описание**                             |
| ------------------ | -------------------------- | ---------------------------------------- |
| **Stretch**        | boolean                    | Отвечает за то, будет ли картинка растягиваться по каждой оси  независимо, чтобы целиком заполнить выделенную область для размещения. |
| **FlipHorizontal** | boolean                    | Отображать ли картинку зеркально по горизонтали. |
| **FlipVertical**   | boolean                    | Отображать ли картинку зеркально по вертикали. |
| **Src**            | string                     | Название картинки или закодированная в base64 картинка в формате .png (в зависимости от параметра **IsBase64**). |
| **Opaque**         | boolean                    | Будет ли картинка непрозрачной.          |
| **SourceType4**    | **ImageControlSourceType** | Тип хранимого в свойстве **Src** значения. |
| **ImageColorARGB** | **ColorARGB**              | Цвет картинки.                           |
| **IsColored**      | boolean                    | Будет ли картинка домножена на цвет.     |

## События:

Отсутствуют. 

## Команды:

| **Команда**       | **Параметры** | **Реакция компонента на команды**        |
| ----------------- | ------------- | ---------------------------------------- |
| **Resource**      | -             | Изображение хранится в ресурсах приложения. В **Src** находится имя ресурса. |
| **Base64**        | -             | Изображение передаётся закодированной в Base64 строкой. В **Src** находится кодированная строка. |
| **PreloadedFile** | -             | Изображение скачивается через сервис получения файлов. В **Src** находится имя скачанного файла. |

## Рекомендуемые ссылки:

* [Варианты использования ImageControl](.presentations/README.md)
* [Особенности и приемы работы с ImageControl](README_hints.md)


