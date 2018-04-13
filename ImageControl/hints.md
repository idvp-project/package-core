# Особенности и приемы работы с ImageControl

## Загрузка картинки из локального файла или по URL ссылке

Кроме стандартного способа «зашить» картинки в приложение при сборке, их также можно подтянуть из собранного приложения как по url так и из локальной папки. 

### URL

Например мы используем картинку, которая находится по ссылке https://i.ytimg.com/vi/iKz0HiS7tQk/maxresdefault.jpg . 

Для этого указываем:

```xml
<BinaryDataSource Address=" https://i.ytimg.com/vi/iKz0HiS7tQk"Name="maxresdefault" 
                  Code="maxresdefault.jpg" 
 /> 
```

А сам компонент ImageControl при этом загружается следующим образом:

```xml
<ImageControl Src="maxresdefault" Stretch="false" SourceType="PreloadedFile"> 
</ImageControl>
```

### Локальная папка

Этот способ используется только в случае, если визуальные шаблоны скопированы локально.

Размещаем рисунок в папке Templates\resources\ . При копировании картинки в папку необходимо удалить окончание, т.е. maxresdefault.jpg станетTemplates\resources\maxresdefault .

Затем:

```xml
<BinaryDataSource Name="maxresdefault" 
Code="maxresdefault"
/>
```

А сам компонент ImageControl при этом загружается следующим образом:

```xml
<ImageControl Src="maxresdefault" Stretch="false" SourceType="PreloadedFile"> 
</ImageControl>
```

## Хранение картинок в тексте верстки и загрузка их в 64base

Существует возможность хранения картинок прямо в тексте верстки. Это может быть удобным в некоторых случаях для небольших изображений.

В таком случае необходимо, чтобы картинка была в формате .png, и указать SourceType = “Base64”. 

Пример кода с реализацией toggle кнопки:

```xml
<ButtonControl ID="lightbutton" Skin="slider_on_off" Width="188" Toggle="true" Height="68" Visible="true">
      <Transform Depth="40%" DepthAlignment="Front"/>
</ButtonControl>
```

Видно, что свойство Toggle="true", что запускает кнопку в режиме переключатель. Это обеспечивает переключение скинов при нажатии. Для того, чтобы скины переключались их необходимо подготавливать и хранить в формате описанном выше в параграфе "Использование свойства skin для различных состояний кнопки".

## Рекомендуемые ссылки:

- [ImageControl Основные сведения](README.md)
- [Варианты использования ImageControl](presentations.md)



