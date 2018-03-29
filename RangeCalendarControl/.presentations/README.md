# Варианты использования RangeCalendarControl 

Внешний вид RangeCalendarControl определяется набором графических ресурсов, которые загружены в него.

## Темный RangeCalendarControl на светлом фоне 

![](../.screenshots/IDVP_01_default_button.png)

```xml
<ButtonControl ID="lightbutton" Skin="invisible" Visible="true">
       <Transform Depth="40%" DepthAlignment="Front"/>
       <Event Name="BigButtonClearClick"/>
       <ImageControl Src="Main_btn_01" Stretch="true" >
           <Transform Width="100%" Height="100%" Depth="10%" HorizontalAlignment="Center"/>
       </ImageControl>
</ButtonControl>
```





## Рекомендуемые ссылки:

- [RangeCalendarControl Основные сведения](../README.md)
- [Особенности и приемы работы с RangeCalendarControl](../README_hints.md)