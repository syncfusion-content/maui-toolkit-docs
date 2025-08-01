---
layout: post
title: About Keys for Syncfusion® Controls | Syncfusion®
description: Explore key mappings for Syncfusion® controls in the documentation, detailing UI element interactions for enhanced user experience.
platform: maui-toolkit
control: General
documentation: UG
---

# Keys of Syncfusion<sup>®</sup> Controls

This page lists the keys for each control and the element to which it is mapped for all the controls.

## SfBottomSheet

<table>
    <tr>
        <th>Theme Dictionary <br/> <br/> </th>        
        <th>Keys <br/> <br/> </th>
        <th> Description <br/> <br/> </th>
    </tr>

    <tr>
        <td rowspan="3">
          SfBottomSheetStyles  <br/> <br/>
        </td>
		<td> SfBottomSheetTheme <br/> <br/>
        </td>
        <td>    
            By merging this key in application resources, you can customize the appearance of SfBottomSheet without merging common theme resource and control style resource dictionaries.
			
{% highlight xaml %}

<Application xmlns:syncTheme="clr-namespace:Syncfusion.Maui.Toolkit.Themes;assembly=Syncfusion.Maui.Toolkit"
             ...>
 <Application.Resources>
    <ResourceDictionary>
        <ResourceDictionary.MergedDictionaries>
            <syncTheme:SyncfusionThemeResourceDictionary />
            <ResourceDictionary>
                <x:String x:Key="SfBottomSheetTheme">CommonTheme</x:String>
                <Color x:Key="SfBottomSheetBackground">AliceBlue</Color>
                <Color x:Key="SfBottomSheetGrabberBackground">Black</Color>
            </ResourceDictionary>
        </ResourceDictionary.MergedDictionaries>
    </ResourceDictionary>
 </Application.Resources>
 </Application>

{% endhighlight %}
            <br/>
            <br/>
        </td>
        </tr>
     <tr>
        <td>SfBottomSheetBackground<br/><br/></td>
        <td>The background color of the bottom sheet<br/><br/></td>
    </tr>
     <tr>
        <td>SfBottomSheetGrabberBackground<br/><br/></td>
        <td>The background color of the grabber<br/><br/></td>
    </tr>
   
 </table>

## SfCartesian Chart

<table>
    <tr>
        <th>Theme Dictionary <br/> <br/> </th>        
        <th>Keys <br/> <br/> </th>
        <th> Description <br/> <br/> </th>
    </tr>

    <tr>
        <td rowspan="16">
            SfCartesianChartStyles  <br/> <br/>
        </td>
		<td> SfCartesianChartTheme <br/> <br/>
        </td>
        <td>    
            By merging this key in application resources, you can customize the appearance of SfCartesianChart without merging common theme resource and control style resource dictionaries.
			
{% highlight xaml %}

<Application xmlns:syncTheme="clr-namespace:Syncfusion.Maui.Toolkit.Themes;assembly=Syncfusion.Maui.Toolkit"
             ...>
 <Application.Resources>
    <ResourceDictionary>
        <ResourceDictionary.MergedDictionaries>
            <syncTheme:SyncfusionThemeResourceDictionary />
            <ResourceDictionary>
                <x:String x:Key="SfCartesianChartTheme">CommonTheme</x:String>
                <Color x:Key="SfCartesianChartBackground">AliceBlue</Color>
                <Color x:Key="SfCartesianChartMajorGridLineStroke">Black</Color>
            </ResourceDictionary>
        </ResourceDictionary.MergedDictionaries>
    </ResourceDictionary>
 </Application.Resources>
 </Application>

{% endhighlight %}
            <br/>
            <br/>
        </td>
        </tr>
     <tr>
        <td>SfCartesianChartBackground<br/><br/></td>
        <td>Background color of the cartesian chart<br/><br/></td>
    </tr>
    <tr>
        <td>SfCartesianChartMajorGridLineStroke<br/><br/></td>
        <td>Stoke of the axis major grid line.<br/><br/></td>
    </tr>
    <tr>
        <td>SfCartesianChartMinorGridLineStroke<br/><br/></td>
        <td>Stoke of the axis minor grid line.<br/><br/></td>
    </tr>
    <tr>
        <td>SfCartesianChartMajorTickLineStroke<br/><br/></td>
        <td>Stoke of the axis major tick line.<br/><br/></td>
    </tr>
    <tr>
        <td>SfCartesianChartMinorTickLineStroke<br/><br/></td>
        <td>Stoke of the axis minor tick line.<br/><br/></td>
    </tr>
    <tr>
        <td>SfCartesianChartAxisLineStroke<br/><br/></td>
        <td>Stoke of the axis line.<br/><br/></td>
    </tr>
    <tr>
        <td>SfCartesianChartAxisTitleTextColor<br/><br/></td>
        <td>Color of the axis title.<br/><br/></td>
    </tr>
    <tr>
        <td>SfCartesianChartAxisTitleBackground<br/><br/></td>
        <td>Background color of the axis title.<br/><br/></td>
    </tr>
    <tr>
        <td>SfCartesianChartAxisTitleStroke<br/><br/></td>
        <td>Stoke of the axis title<br/><br/></td>
    </tr>
    <tr>
        <td>SfCartesianChartAxisTitleTextFontSize<br/><br/></td>
        <td>Font size of the axis title text.<br/><br/></td>
    </tr>
    <tr>
        <td>SfCartesianChartDataPointSelectionBrush<br/><br/></td>
        <td>Color of the selected segment of the series.<br/><br/></td>
    </tr>
    <tr>
        <td>SfCartesianChartSeriesSelectionBrush<br/><br/></td>
        <td>Color of the selected series.<br/><br/></td>
    </tr>
    <tr>
        <td>SfCartesianChartTooltipBackground<br/><br/></td>
        <td>Background of the tooltip<br/><br/></td>
    </tr>
    <tr>
        <td>SfCartesianChartTooltipTextColor<br/><br/></td>
        <td>Text color of the tooltip<br/><br/></td>
    </tr>
    <tr>
        <td>SfCartesianChartTooltipTextFontSize<br/><br/></td>
        <td>Font size of the tooltip<br/><br/></td>
    </tr>   
 </table>

## SfChips

<table>
    <tr>
        <th>Theme Dictionary<br/>
            <br/></th>        
        <th>
          Keys
            <br/>
            <br/>
        </th>
        <th>
            Description
            <br/>
            <br/>
        </th>
    </tr>

    <tr>
        <td rowspan="32">
            SfChipStyles 
            <br/>
            <br/>
        </td>
		<td>
           SfChipTheme 
            <br/>
            <br/>
        </td>
        <td>    
            By merging this key in application resources, you can customize the appearance of SfChips without merging common theme resource and control style resource dictionaries.
			
{% highlight xaml %}

<Application xmlns:syncTheme="clr-namespace:Syncfusion.Maui.Toolkit.Themes;assembly=Syncfusion.Maui.Toolkit"
             ...>
 <Application.Resources>
    <ResourceDictionary>
        <ResourceDictionary.MergedDictionaries>
            <syncTheme:SyncfusionThemeResourceDictionary />
            <ResourceDictionary>
                <x:String x:Key="SfChipTheme">CommonTheme</x:String>
                <Color x:Key="SfChipNormalBackground">Purple</Color>
                <Color x:Key="SfChipNormalTextColor">YellowGreen</Color>
            </ResourceDictionary>
        </ResourceDictionary.MergedDictionaries>
    </ResourceDictionary>
 </Application.Resources>
 </Application>

{% endhighlight %}
            <br/>
            <br/>
        </td>
        </tr>
    <tr>
        <td>
            SfChipNormalStrokeThickness
            <br/>
            <br/>
        </td>
        <td>
            StrokeThickness of the SfChips.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipNormalFontSize
            <br/>
            <br/>
        </td>
        <td>
            FontSize of the SfChips.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipNormalCornerRadius
            <br/>
            <br/>
        </td>
        <td>
            CornerRadius of the SfChips.
            <br/>
            <br/>
        </td>
    </tr>
        <tr>
        <td>
            SfChipNormalBackground 
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChips Background.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipNormalTextColor  
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChip TextColor.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipNormalClearButtonIconColor  
            <br/>
            <br/>
        </td>
        <td>
            Color of the clear button icon.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipNormalStroke 
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChips stroke.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipNormalSelectionIndicatorColor
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChips selection indicator.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipDisabledBackground
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChips background in disabled state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipDisabledTextColor
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChips text in disabled state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipDisabledClearButtonIconColor
            <br/>
            <br/>
        </td>
        <td>
            Color of the clear button icon in disabled state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipDisabledStroke
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChips stroke in disabled state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipDisabledSelectionIndicatorColor
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChips selection indicator in disabled state.
            <br/>
            <br/>
        </td>
    </tr>
        <tr>
        <td>
           SfChipGroupTheme 
            <br/>
            <br/>
        </td>
        <td>    
            By merging this key in application resources, you can customize the appearance of SfChipGroup without merging common theme resource and control style resource dictionaries.
			
{% highlight xaml %}

<Application xmlns:syncTheme="clr-namespace:Syncfusion.Maui.Toolkit.Themes;assembly=Syncfusion.Maui.Toolkit"
             ...>
 <Application.Resources>
    <ResourceDictionary>
        <ResourceDictionary.MergedDictionaries>
            <syncTheme:SyncfusionThemeResourceDictionary />
            <ResourceDictionary>
                <x:String x:Key="SfChipGroupTheme">CommonTheme</x:String>
                <Color x:Key="SfChipGroupNormalSelectionBackground">Purple</Color>
                <Color x:Key="SfChipGroupNormalSelectedTextColor">YellowGreen</Color>
            </ResourceDictionary>
        </ResourceDictionary.MergedDictionaries>
    </ResourceDictionary>
 </Application.Resources>
 </Application>

{% endhighlight %}
            <br/>
            <br/>
        </td>
        </tr>
    <tr>
        <td>
            SfChipGroupNormalStrokeThickness
            <br/>
            <br/>
        </td>
        <td>
            StrokeThickness of the SfChipGroup.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipGroupNormalCornerRadius
            <br/>
            <br/>
        </td>
        <td>
            CornerRadius of the SfChipGroup.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipGroupNormalSelectedTextColor  
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChipGroup selected text in normal state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipGroupNormalClearButtonIconColor
            <br/>
            <br/>
        </td>
        <td>
            Color of the clear button icon.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipGroupNormalBackground  
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChipGroup background.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipGroupNormalTextColor
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChipGroup text.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipGroupNormalStroke  
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChipGroup stroke in normal state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipGroupNormalSelectionBackground
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChipGroup selection background.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipGroupNormalSelectionIndicatorColor
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChipGroup selection indicator.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipGroupPressedStroke  
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChipGroup stroke in pressed state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipGroupDisabledBackground  
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChipGroup background in disabled state.
            <br/>
            <br/>
        </td>
    </tr>
      <tr>
        <td>
            SfChipGroupDisabledTextColor
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChipGroup text in disabled state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipGroupDisabledStroke
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChipGroup stroke in disabled state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipGroupSelectedDisabledBackground
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChipGroup selected background in disabled state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfChipGroupSelectedDisabledTextColor
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChipGroup selected text in disabled state.
            <br/>
            <br/>
        </td>
    </tr>
     <tr>
        <td>
            SfChipGroupDisabledSelectionIndicatorColor
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfChipGroup selection indicator in disabled state.
            <br/>
            <br/>
        </td>
    </tr>
</table>

## SfCircular Chart
 <table>
     <tr>
         <th>Theme Dictionary <br/> <br/> </th>        
         <th>Keys <br/> <br/> </th>
         <th> Description <br/> <br/> </th>
     </tr>
     <tr>
         <td rowspan="6">
             SfCircularChartStyles  <br/> <br/>
         </td>
         <td> SfCircularChartTheme <br/> <br/>
         </td>
         <td>    
             By merging this key in application resources, you can customize the appearance of SfCircularChart without merging common theme resource and control style resource dictionaries.
             
 {% highlight xaml %}
 <Application xmlns:syncTheme="clr-namespace:Syncfusion.Maui.Toolkit.Themes;assembly=Syncfusion.Maui.Toolkit"
              ...>
  <Application.Resources>
     <ResourceDictionary>
         <ResourceDictionary.MergedDictionaries>
             <syncTheme:SyncfusionThemeResourceDictionary />
             <ResourceDictionary>
                 <x:String x:Key="SfCircularChartTheme">CommonTheme</x:String>
                 <Color x:Key="SfCircularChartBackground">LightYellow</Color>
                 <Color x:Key="SfCircularChartTooltipBackground">Gray</Color>
             </ResourceDictionary>
         </ResourceDictionary.MergedDictionaries>
     </ResourceDictionary>
  </Application.Resources>
  </Application>
 {% endhighlight %}
             <br/>
             <br/>
         </td>
         </tr>
     <tr>
        <td>SfCircularChartBackground<br/><br/></td>
        <td>Background of the circular chart<br/><br/></td>
    </tr>
    <tr>
        <td>SfCircularChartSelectionBrush<br/><br/></td>
        <td>Color of the selected segment of the series.<br/><br/></td>
    </tr>
    <tr>
        <td>SfCircularChartTooltipBackground<br/><br/></td>
        <td>Background of the tooltip<br/><br/></td>
    </tr>
    <tr>
        <td>SfCircularChartTooltipTextColor<br/><br/></td>
        <td>Text color of the tooltip<br/><br/></td>
    </tr>
    <tr>
        <td>SfCircularChartTooltipTextFontSize<br/><br/></td>
        <td>Font size of tooltip text<br/><br/></td>
    </tr>
  </table>  

## SfEffectsView

<table>
    <tr>
        <th>Theme Dictionary<br/>
            <br/></th>        
        <th>
          Keys
            <br/>
            <br/>
        </th>
        <th>
            Description
            <br/>
            <br/>
        </th>
    </tr>

    <tr>
        <td rowspan="5">
            SfEffectsViewStyles 
            <br/>
            <br/>
        </td>
		<td>
           SfEffectsViewTheme 
            <br/>
            <br/>
        </td>
        <td>    
            By merging this key in application resources, you can customize the appearance of SfEffectsView without merging common theme resource and control style resource dictionaries.
			
{% highlight xaml %}

<Application xmlns:syncTheme="clr-namespace:Syncfusion.Maui.Toolkit.Themes;assembly=Syncfusion.Maui.Toolkit"
             ...>
 <Application.Resources>
    <ResourceDictionary>
        <ResourceDictionary.MergedDictionaries>
            <syncTheme:SyncfusionThemeResourceDictionary />
            <ResourceDictionary>
                <x:String x:Key="SfEffectsViewTheme">CommonTheme</x:String>
                <Color x:Key="SfEffectsViewRippleBackground">Yellow</Color>
                <Color x:Key="SfEffectsViewHighlightBackground">Red</Color>
            </ResourceDictionary>
        </ResourceDictionary.MergedDictionaries>
    </ResourceDictionary>
 </Application.Resources>
 </Application>

{% endhighlight %}
            <br/>
            <br/>
        </td>
        </tr>
        <tr>
        <td>
            SfEffectsViewRippleBackground  
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfEffectsView ripple background.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfEffectsViewSelectionBackground  
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfEffectsView selection background
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfEffectsViewHighlightBackground  
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfEffectsView highlight background.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfEffectsViewRippleAnimationDuration  
            <br/>
            <br/>
        </td>
        <td>
            Duration of the SfEffectsView ripple animation.
            <br/>
            <br/>
        </td>
    </tr>
    </table>

## SfFunnel Chart

<table>
     <tr>
         <th>Theme Dictionary <br/> <br/> </th>         
         <th>Keys <br/> <br/> </th>
         <th> Description <br/> <br/> </th>
     </tr>
     <tr>
         <td rowspan="6">
             SfFunnelStyles  <br/> <br/>
         </td>
         <td> SfFunnelChartTheme <br/> <br/>
         </td>
         <td>    
             By merging this key in application resources, you can customize the appearance of SfFunnelChart without merging common theme resource and control style resource dictionaries.
             
 {% highlight xaml %}
 <Application xmlns:syncTheme="clr-namespace:Syncfusion.Maui.Toolkit.Themes;assembly=Syncfusion.Maui.Toolkit"
              ...>
  <Application.Resources>
     <ResourceDictionary>
         <ResourceDictionary.MergedDictionaries>
             <syncTheme:SyncfusionThemeResourceDictionary />
             <ResourceDictionary>
                 <x:String x:Key="SfFunnelChartTheme">CommonTheme</x:String>
                 <Color x:Key="SfFunnelChartBackground">LightYellow</Color>
                 <Color x:Key="SfFunnelChartTooltipBackground">Gray</Color>
             </ResourceDictionary>
         </ResourceDictionary.MergedDictionaries>
     </ResourceDictionary>
  </Application.Resources>
  </Application>
 {% endhighlight %}
             <br/>
             <br/>
         </td>
         </tr>
    <tr>
        <td>SfFunnelChartBackground<br/><br/></td>
        <td>Background of the funnel chart<br/><br/></td>
    </tr>
    <tr>
        <td>SfFunnelChartSelectionBrush<br/><br/></td>
        <td>Color of the selected segment.<br/><br/></td>
    </tr>
    <tr>
        <td>SfFunnelChartTooltipBackground<br/><br/></td>
        <td>Background of the tooltip<br/><br/></td>
    </tr>
    <tr>
        <td>SfFunnelChartTooltipTextColor<br/><br/></td>
        <td>Text color of the tooltip<br/><br/></td>
    </tr>
    <tr>
        <td>SfFunnelChartTooltipTextFontSize<br/><br/></td>
        <td>Font size of the tooltip text<br/><br/></td>
    </tr>
  </table>

## SfNavigationDrawer

<table>
    <tr>
        <th>Theme Dictionary<br/>
            <br/></th>        
        <th>
          Keys
            <br/>
            <br/>
        </th>
        <th>
            Description
            <br/>
            <br/>
        </th>
    </tr>

    <tr>
        <td rowspan="3">
            SfNavigationDrawerStyles 
            <br/>
            <br/>
        </td>
		<td>
           SfNavigationDrawerTheme 
            <br/>
            <br/>
        </td>
        <td>    
            By merging this key in application resources, you can customize the appearance of SfNavigationDrawer without merging common theme resource and control style resource dictionaries.
			
{% highlight xaml %}

<Application xmlns:syncTheme="clr-namespace:Syncfusion.Maui.Toolkit.Themes;assembly=Syncfusion.Maui.Toolkit"
             ...>
 <Application.Resources>
    <ResourceDictionary>
        <ResourceDictionary.MergedDictionaries>
            <syncTheme:SyncfusionThemeResourceDictionary />
            <ResourceDictionary>
                <x:String x:Key="SfNavigationDrawerTheme">CommonTheme</x:String>
                <Color x:Key="SfNavigationDrawerContentBackground">Yellow</Color>
                <Color x:Key="SfNavigationDrawerGreyLayoutBackground">Red</Color>
            </ResourceDictionary>
        </ResourceDictionary.MergedDictionaries>
    </ResourceDictionary>
 </Application.Resources>
 </Application>

{% endhighlight %}
            <br/>
            <br/>
        </td>
        </tr>
        <tr>
        <td>
            SfNavigationDrawerContentBackground  
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfNavigationDrawer background.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfNavigationDrawerGreyLayoutBackground 
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfNavigationDrawer layout background.
            <br/>
            <br/>
        </td>
    </tr>
    </table>

## SfOtpInput

<table>
    <tr>
        <th>Theme Dictionary<br/>
            <br/></th>        
        <th>
          Keys
            <br/>
            <br/>
        </th>
        <th>
            Description
            <br/>
            <br/>
        </th>
    </tr>

    <tr>
        <td rowspan="15">
            SfOtpInputStyles 
            <br/>
            <br/>
        </td>
		<td>
           SfOtpInputTheme 
            <br/>
            <br/>
        </td>
        <td>    
            By merging this key in application resources, you can customize the appearance of SfOtpInput without merging common theme resource and control style resource dictionaries.
			
{% highlight xaml %}

<Application xmlns:syncTheme="clr-namespace:Syncfusion.Maui.Toolkit.Themes;assembly=Syncfusion.Maui.Toolkit"
             ...>
 <Application.Resources>
    <ResourceDictionary>
        <ResourceDictionary.MergedDictionaries>
            <syncTheme:SyncfusionThemeResourceDictionary />
            <ResourceDictionary>
                <x:String x:Key="SfOtpInputTheme">CommonTheme</x:String>
                <Color x:Key="SfOtpInputTextColor">Yellow</Color>
                <Color x:Key="SfOtpInputFilledBackground">Red</Color>
            </ResourceDictionary>
        </ResourceDictionary.MergedDictionaries>
    </ResourceDictionary>
 </Application.Resources>
 </Application>

{% endhighlight %}
            <br/>
            <br/>
        </td>
        </tr>
        <tr>
        <td>
            SfOtpInputTextColor  
            <br/>
            <br/>
        </td>
        <td>
            Text color of the OTP Input.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfOtpInputFilledBackground 
            <br/>
            <br/>
        </td>
        <td>
            The background color of the OTP Input on filled state.
            <br/>
            <br/>
        </td>
    </tr>

   <tr>
        <td> SfOtpInputBorderDefault <br/><br/></td>
        <td>Border color of the OTP Input.<br/><br/>
        </td>
    </tr>

    <tr>
        <td> SfOtpInputPlaceholderColor <br/><br/></td>
        <td> Placeholder color of the OTP Input.<br/><br/>
        </td>
    </tr>

    <tr>
        <td> SfOtpInputSuccessStroke <br/><br/></td>
        <td>Border color when OTP Input is successfully validated.<br/><br/>
        </td>
    </tr>

    <tr>
        <td> SfOtpInputWarningStroke <br/><br/></td>
        <td> Border color when there's a warning state in OTP Input.<br/><br/>
        </td>
    </tr>

    <tr>
        <td> SfOtpInputErrorStroke <br/><br/></td>
        <td> Border color when there's an error state in OTP Input.<br/><br/>
        </td>
    </tr>

    <tr>
        <td> SfOtpInputDefaultBackground <br/><br/></td>
        <td> Default background color of the OTP Input.<br/><br/>
        </td>
    </tr>

    <tr>
        <td> SfOtpInputHoveredBackground <br/><br/></td>
        <td> Background color when hovered over OTP Input.<br/><br/>
        </td>
    </tr>

    <tr>
        <td> SfOtpInputBorderHovered <br/><br/></td>
        <td> Border color when hovered over OTP Input.<br/><br/>
        </td>
    </tr>

    <tr>
        <td> SfOtpInputBorderPressed <br/><br/></td>
        <td> Border color when OTP Input is pressed.<br/><br/>
        </td>
    </tr>

    <tr>
        <td> SfOtpInputBorderDisabled <br/><br/></td>
        <td> Border color when OTP Input is disabled.<br/><br/>
        </td>
    </tr>

    <tr>
        <td> SfOtpInputBackgroundDisabled <br/><br/></td>
        <td> Background color when OTP Input is disabled.<br/><br/>
        </td>
    </tr>
    
    <tr>
        <td> SfOtpInputDisabledTextColor <br/><br/></td>
        <td> Text color when OTP Input is disabled.<br/><br/>
        </td>
    </tr>

    </table>

## SfPopup

<table>
    <tr>
        <th>Theme Dictionary<br/>
            <br/></th>        
        <th>
          Keys
            <br/>
            <br/>
        </th>
        <th>
            Description
            <br/>
            <br/>
        </th>
    </tr>

    <tr>
        <td rowspan="23">
            SfPopupStyles  
            <br/>
            <br/>
        </td>
        <td>
           SfPopupTheme 
            <br/>
            <br/>
        </td>
        <td>    
            By merging this key in application resources, you can customize the appearance of SfPopup without merging common theme resource and control style resource dictionaries.
			
{% highlight xaml %}

<Application xmlns:syncTheme="clr-namespace:Syncfusion.Maui.Toolkit.Themes;assembly=Syncfusion.Maui.Toolkit"
             ...>
 <Application.Resources>
    <ResourceDictionary>
        <ResourceDictionary.MergedDictionaries>
            <syncTheme:SyncfusionThemeResourceDictionary />
            <ResourceDictionary>
                <x:String x:Key="SfPopupTheme">CommonTheme</x:String>
                <Color x:Key="SfPopupNormalHeaderTextColor">Black</Color>
                <Color x:Key="SfPopupHoverFooterButtonBackground">Gray</Color>
            </ResourceDictionary>
        </ResourceDictionary.MergedDictionaries>
    </ResourceDictionary>
 </Application.Resources>

....

</Application>

{% endhighlight %}
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td> SfPopupHoverFooterButtonBackground <br/><br/></td>
        <td> Hover Background color of the SfPopup Footer button.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupFooterButtonRippleBackground <br/><br/></td>
        <td> Ripple Background Color of the Sfpopup Footer button.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupNormalHeaderBackground <br/><br/></td>
        <td> Background color of the SfPopup Header.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupNormalHeaderTextColor <br/><br/></td>
        <td> Text color of the SfPopup Header.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupNormalMessageBackground <br/><br/></td>
        <td> Background color of the SfPopup Message.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupNormalMessageTextColor <br/><br/></td>
        <td> Text color of the SfPopup Message.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupNormalFooterBackground <br/><br/></td>
        <td> Background color of the SfPopup Footer.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupNormalAcceptButtonBackground <br/><br/></td>
        <td> Background color of the SfPopup AcceptButton.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupNormalAcceptButtonTextColor <br/><br/></td>
        <td> Text color of the SfPopup AcceptButton.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupNormalDeclineButtonBackground <br/><br/></td>
        <td> Background color of the SfPopup DeclineButton.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupNormalDeclineButtonTextColor <br/><br/></td>
        <td> Text color of the SfPopup DeclineButton.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupNormalStroke <br/><br/></td>
        <td> Stroke color of the SfPopup.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupNormalHeaderFontSize <br/><br/></td>
        <td> Font Size of the SfPopup Header.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupNormalMessageFontSize <br/><br/></td>
        <td> Font Size of the SfPopup Message.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupNormalFooterFontSize <br/><br/></td>
        <td> Font Size of the SfPopup Footer.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupNormalStrokeThickness <br/><br/></td>
        <td> Stroke Thickness of the SfPopup.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupNormalOverlayBackground <br/><br/></td>
        <td> Background color of the SfPopup Overlay.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupHoverCloseButtonIconBackground <br/><br/></td>
        <td> Hover Background color of the SfPopup CloseButtonIcon.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupPressedCloseButtonIconBackground <br/><br/></td>
        <td> Pressed Background color of the SfPopup CloseButtonIcon.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupNormalCloseButtonIconStroke <br/><br/></td>
        <td> Stroke color of the SfPopup CloseButtonIcon.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupNormalBackground <br/><br/></td>
        <td> Background color of the SfPopup.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPopupNormalCloseButtonIconStrokeThickness <br/><br/></td>
        <td> Stroke Thickness of the SfPopup CloseButtonIcon.<br/><br/></td>
    </tr>
</table>

## SfPullToRefresh

<table>
    <tr>
        <th>Theme Dictionary<br/>
            <br/></th>        
        <th>
          Keys
            <br/>
            <br/>
        </th>
        <th>
            Description
            <br/>
            <br/>
        </th>
    </tr>

    <tr>
        <td rowspan="4">
            SfPullToRefreshStyles  
            <br/>
            <br/>
        </td>
        <td>
           SfPullToRefreshTheme 
            <br/>
            <br/>
        </td>
        <td>    
            By merging this key in application resources, you can customize the appearance of SfPullToRefresh without merging common theme resource and control style resource dictionaries.
			
{% highlight xaml %}

<Application xmlns:syncTheme="clr-namespace:Syncfusion.Maui.Toolkit.Themes;assembly=Syncfusion.Maui.Toolkit"
             ...>
 <Application.Resources>
    <ResourceDictionary>
        <ResourceDictionary.MergedDictionaries>
            <syncTheme:SyncfusionThemeResourceDictionary />
            <ResourceDictionary>
                <x:String x:Key="SfPullToRefreshTheme">CommonTheme</x:String>
                <Color x:Key="SfPullToRefreshProgressBackground">Black</Color>
                <Color x:Key="SfPullToRefreshProgressColor">White</Color>
            </ResourceDictionary>
        </ResourceDictionary.MergedDictionaries>
    </ResourceDictionary>
 </Application.Resources>

....

</Application>

{% endhighlight %}
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td> SfPullToRefreshProgressBackground <br/><br/></td>
        <td> Background color of the progress circle view.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPullToRefreshProgressColor <br/><br/></td>
        <td> Color of the progress indicator.<br/><br/></td>
    </tr>
    <tr>
        <td> SfPullToRefreshProgressThickness <br/><br/></td>
        <td> Thickness of the progress indicator.<br/><br/></td>
    </tr>
</table>

## SfPyramid Chart
  <table>
      <tr>
          <th>Theme Dictionary <br/> <br/> </th>        
          <th>Keys <br/> <br/> </th>
          <th> Description <br/> <br/> </th>
      </tr>
      <tr>
          <td rowspan="6">
              SfPyramidChartStyles  <br/> <br/>
          </td>
          <td> SfPyramidChartTheme <br/> <br/>
          </td>
          <td>    
              By merging this key in application resources, you can customize the appearance of SfPyramidChart without merging common theme resource and control style resource dictionaries.
              
  {% highlight xaml %}
  <Application xmlns:syncTheme="clr-namespace:Syncfusion.Maui.Toolkit.Themes;assembly=Syncfusion.Maui.Toolkit"
               ...>
   <Application.Resources>
      <ResourceDictionary>
          <ResourceDictionary.MergedDictionaries>
              <syncTheme:SyncfusionThemeResourceDictionary />
              <ResourceDictionary>
                  <x:String x:Key="SfPyramidChartTheme">CommonTheme</x:String>
                  <Color x:Key="SfPyramidChartBackground">LightYellow</Color>
                  <Color x:Key="SfPyramidChartTooltipBackgrounds">Gray</Color>
              </ResourceDictionary>
          </ResourceDictionary.MergedDictionaries>
      </ResourceDictionary>
   </Application.Resources>
   </Application>
  {% endhighlight %}
              <br/>
              <br/>
          </td>
          </tr>
    <tr>
        <td>SfPyramidChartBackground<br/><br/></td>
        <td>Background color of the pyramid chart<br/><br/></td>
    </tr>
    <tr>
        <td>SfPyramidChartSelectionBrush<br/><br/></td>
        <td>Color of the selected segment of the series.<br/><br/></td>
    </tr>
    <tr>
        <td>SfPyramidChartTooltipBackgrounds<br/><br/></td>
        <td>Background of the tooltip<br/><br/></td>
    </tr>
    <tr>
        <td>SfPyramidChartTooltipTextColor<br/><br/></td>
        <td>Text color of the tooltip<br/><br/></td>
    </tr>
    <tr>
        <td>SfPyramidChartTooltipTextFontSize<br/><br/></td>
        <td>Font size of the tooltip text<br/><br/></td>
    </tr>
   </table>

## SfSegmentedControl

<table>
    <tr>
        <th>Theme Dictionary<br/>
            <br/></th>        
        <th>
          Keys
            <br/>
            <br/>
        </th>
        <th>
            Description
            <br/>
            <br/>
        </th>
    </tr>

    <tr>
        <td rowspan="16">
            SfSegmentedControlStyles
            <br/>
            <br/>
        </td>
		<td>
           SfSegmentedControlTheme 
            <br/>
            <br/>
        </td>
        <td>    
            By merging this key in application resources, you can customize the appearance of SfSegmentedControl without merging common theme resource and control style resource dictionaries.
			
{% highlight xaml %}

<Application xmlns:syncTheme="clr-namespace:Syncfusion.Maui.Toolkit.Themes;assembly=Syncfusion.Maui.Toolkit"
             ...>
 <Application.Resources>
    <ResourceDictionary>
        <ResourceDictionary.MergedDictionaries>
            <syncTheme:SyncfusionThemeResourceDictionary />
            <ResourceDictionary>
                <x:String x:Key="SfSegmentedControlTheme">CommonTheme</x:String>
                <Color x:Key="SfSegmentedControlNormalStroke">Red</Color>
                <Color x:Key="SfSegmentedControlNormalBackground">Green</Color>
            </ResourceDictionary>
        </ResourceDictionary.MergedDictionaries>
    </ResourceDictionary>
 </Application.Resources>

....

</Application>

{% endhighlight %}
            <br/>
            <br/>
        </td>
	</tr>
    
    <tr>
    <td>
            SfSegmentedControlNormalStroke    
            <br/>
            <br/>
        </td>
        <td>
            Color of border in the segmented control.
            <br/>
            <br/>
        </td>
    </tr>

    <tr>
    <td>
            SfSegmentedControlNormalTextColor     
            <br/>
            <br/>
        </td>
        <td>
            Color of text in the segmented control.
            <br/>
            <br/>
        </td>
    </tr>

	<tr>
    <td>
            SfSegmentedControlNormalBackground      
            <br/>
            <br/>
        </td>
        <td>
            Background color of the segmented control.
            <br/>
            <br/>
        </td>
    </tr>

	<tr>
    <td>
            SfSegmentedControlDisabledSegmentBackground       
            <br/>
            <br/>
        </td>
        <td>
            Background Color of segment when it is disabled. 
            <br/>
            <br/>
        </td>
    </tr>

	<tr>
    <td>
            SfSegmentedControlDisabledSegmentTextColor        
            <br/>
            <br/>
        </td>
        <td>
            Color of segment item text when it is disabled.  
            <br/>
            <br/>
        </td>
    </tr>

	<tr>
    <td>
            SfSegmentedControlSelectionBackground         
            <br/>
            <br/>
        </td>
        <td>
            Background color of segment when it is selected.   
            <br/>
            <br/>
        </td>
    </tr>

	<tr>
    <td>
            SfSegmentedControlSelectionTextColor          
            <br/>
            <br/>
        </td>
        <td>
            Color of segmented items text when it is selected. 
            <br/>
            <br/>
        </td>
    </tr>

	<tr>
    <td>
            SfSegmentedControlSelectionStroke           
            <br/>
            <br/>
        </td>
        <td>
            Color of segmented item border when it is selected.   
            <br/>
            <br/>
        </td>
    </tr>

	<tr>
    <td>
            SfSegmentedControlHoveredBackground            
            <br/>
            <br/>
        </td>
        <td>
            Background color of segment when it is hovered.   
            <br/>
            <br/>
        </td>
    </tr>

	<tr>
    <td>
            SfSegmentedControlKeyboardFocusStroke             
            <br/>
            <br/>
        </td>
        <td>
            Segmented controls border color when it is focused using the keyboard navigation keys.
            <br/>
            <br/>
        </td>
    </tr>

	<tr>
    <td>
            SfSegmentedControlNormalStrokeThickness              
            <br/>
            <br/>
        </td>
        <td>
            Thickness of the border stroke in the segmented control.    
            <br/>
            <br/>
        </td>
    </tr>

	<tr>
    <td>
            SfSegmentedControlNormalCornerRadius               
            <br/>
            <br/>
        </td>
        <td>
            Corner radius of the segmented control.     
            <br/>
            <br/>
        </td>
    </tr>

	<tr>
    <td>
            SfSegmentedControlNormalSegmentCornerRadius                
            <br/>
            <br/>
        </td>
        <td>
            Corner radius of segment in the segmented control.      
            <br/>
            <br/>
        </td>
    </tr>

	<tr>
    <td>
            SfSegmentedControlNormalFontSize                 
            <br/>
            <br/>
        </td>
        <td>
            Font size of the segment item in the segmented control.   
            <br/>
            <br/>
        </td>
    </tr>

	<tr>
    <td>
            SfSegmentedControlBorderSelectionStrokeThickness                  
            <br/>
            <br/>
        </td>
        <td>
            Thickness of the border stroke in the segmented control, when it is selected.     
            <br/>
            <br/>
        </td>
    </tr>
</table>

## SfShimmer

<table>
    <tr>
        <th>Theme Dictionary<br/>
            <br/></th>        
        <th>
          Keys
            <br/>
            <br/>
        </th>
        <th>
            Description
            <br/>
            <br/>
        </th>
    </tr>
    <tr>
        <td rowspan="14">
            SfShimmerStyles  
            <br/>
            <br/>
        </td>
		<td>
           SfShimmerTheme 
            <br/>
            <br/>
        </td>
        <td>    
            By merging this key in application resources, you can customize the appearance of SfShimmer without merging common theme resource and control style resource dictionaries.

{% highlight xaml %}

<Application xmlns:syncTheme="clr-namespace:Syncfusion.Maui.Toolkit.Themes;assembly=Syncfusion.Maui.Toolkit"
             ...>
 <Application.Resources>
    <ResourceDictionary>
        <ResourceDictionary.MergedDictionaries>
            <syncTheme:SyncfusionThemeResourceDictionary />
            <ResourceDictionary>
                <x:String x:Key="SfShimmerTheme">CommonTheme</x:String>
                <Color x:Key="SfShimmerFillColor">Pink</Color>
                <Color x:Key="SfShimmerWaveColor">Purple</Color>
            </ResourceDictionary>
        </ResourceDictionary.MergedDictionaries>
    </ResourceDictionary>
 </Application.Resources>

....

</Application>

{% endhighlight %}
            <br/>
            <br/>
        </td>
        <tr>
        <td>
            SfShimmerFillColor  
            <br/>
            <br/>
        </td>
        <td>
            Fill color of the shimmer.
            <br/>
            <br/>
        </td>
    </tr>
	</tr>
    <tr>
        <td>
            SfShimmerWaveColor 
            <br/>
            <br/>
        </td>
        <td>
            Wave color of the shimmer.
        <br/>
        <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfShimmerNormalBackground  
            <br/>
            <br/>
        </td> 
        <td>
            Background color of the shimmer.
            <br/>
            <br/>
        </td>
    </tr>
</table>

## SfTabView

<table>
    <tr>
        <th>Theme Dictionary<br/>
            <br/></th>        
        <th>
          Keys
            <br/>
            <br/>
        </th>
        <th>
            Description
            <br/>
            <br/>
        </th>
    </tr>

    <tr>
        <td rowspan="42">
            SfTabViewStyles 
            <br/>
            <br/>
        </td>
		<td>
           SfTabViewTheme 
            <br/>
            <br/>
        </td>
        <td>    
            By merging this key in application resources, you can customize the appearance of SfTabView without merging common theme resource and control style resource dictionaries.
			
{% highlight xaml %}

<Application xmlns:syncTheme="clr-namespace:Syncfusion.Maui.Toolkit.Themes;assembly=Syncfusion.Maui.Toolkit"
             ...>
 <Application.Resources>
    <ResourceDictionary>
        <ResourceDictionary.MergedDictionaries>
            <syncTheme:SyncfusionThemeResourceDictionary />
            <ResourceDictionary>
                <x:String x:Key="SfTabViewTheme">CommonTheme</x:String>
                <Color x:Key="SfTabViewActiveMouseHoveredIndicatorBackground">DarkBlue</Color>
                <Color x:Key="SfTabViewNormalTabBarBackground">Gold</Color>
            </ResourceDictionary>
        </ResourceDictionary.MergedDictionaries>
    </ResourceDictionary>
 </Application.Resources>
 </Application>

{% endhighlight %}
            <br/>
            <br/>
        </td>
        </tr>
    <tr>
        <td>
            SfTabViewDisabledTextColor  
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfTabView text in disabled state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
		<td>
			SfTabViewActiveDisabledBackground  
			<br/>
			<br/>
		</td>
		<td>
			Background color of the active SfTabView when disabled.
			<br/>
			<br/>
		</td>
	</tr>
	<tr>
        <td>
            SfTabViewActiveIndicatorBackground  
            <br/>
            <br/>
        </td>
        <td>
            BackgroundColor of the active indicator in a SfTabView.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewActiveMouseHoveredIndicatorBackground  
            <br/>
            <br/>
        </td>
        <td>
            BackgroundColor of the active indicator in a SfTabView when hovered.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewActiveDisabledIndicatorBackground  
            <br/>
            <br/>
        </td>
        <td>
            BackgroundColor of the active indicator in a SfTabView when disabled. 
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewNormalTextColor 
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfTabView text.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewActiveNormalBackground  
            <br/>
            <br/>
        </td>
        <td>
            BackgroundColor of the active SfTabView. 
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewInActiveNormalTextColor 
            <br/>
            <br/>
        </td>
        <td>
            TextColor of the inactive SfTabView. 
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewActivePressedBackground  
            <br/>
            <br/>
        </td>
        <td>
            BackgroundColor of the active SfTabView in pressed state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewInActiveTextColor
            <br/>
            <br/>
        </td>
        <td>
            TextColor of the inactive SfTabView.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewInActivePressedBackground
            <br/>
            <br/>
        </td>
        <td>
            BackgroundColor of the inactive SfTabView in pressed state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewActiveTextColor
            <br/>
            <br/>
        </td>
        <td>
            TextColor of the active SfTabView. 
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewInActiveNormalBackground 
            <br/>
            <br/>
        </td>
        <td>
            BackgroundColor of the inactive SfTabView.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewSelectedTextColor
            <br/>
            <br/>
        </td>
        <td>
            TextColor of the selected SfTabView.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewInActiveDisabledBackground
            <br/>
            <br/>
        </td>
        <td>
            BackgroundColor of the inactive SfTabView in disabled state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewInActiveHoveredBackground
            <br/>
            <br/>
        </td>
        <td>
            BackgroundColor of the inactive SfTabView in hover state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewNormalFilledTextColor
            <br/>
            <br/>
        </td>
        <td>
            Color of the filled SfTabView text.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewActiveFilledNormalBackground
            <br/>
            <br/>
        </td>
        <td>
            Color of the active fill SfTabView background.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewActiveHoveredFilledTextColor
            <br/>
            <br/>
        </td>
        <td>
            Color of the active hovered fill SfTabView text.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewActiveHoveredBackground 
            <br/>
            <br/>
        </td>
        <td>
            BackgroundColor of the active SfTabView in hover state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewInActiveHoveredFilledTextColor 
            <br/>
            <br/>
        </td>
        <td>
            TextColor of the inactive SfTabView in hover state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewInActiveHoveredFilledBackground 
            <br/>
            <br/>
        </td>
        <td>
            BackgroundColor of the inactive fill SfTabView in hover state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewActivePressedFilledTextColor 
            <br/>
            <br/>
        </td>
        <td>
            TextColor of the active filled SfTabView in pressed state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewActivePressedFilledBackground
            <br/>
            <br/>
        </td>
        <td>
            BackgroundColor of the active filled SfTabView in pressed state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewInActivePressedFilledTextColor
            <br/>
            <br/>
        </td>
        <td>
            TextColor of the inactive filled SfTabView in pressed state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewInActivePressedFilledBackground
            <br/>
            <br/>
        </td>
        <td>
            BackgroundColor of the inactive filled SfTabView in pressed state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewActiveFocusedFilledTextColor
            <br/>
            <br/>
        </td>
        <td>
            TextColor of the active filled SfTabView in focus state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewActiveFocusedFilledBackground
            <br/>
            <br/>
        </td>
        <td>
            BackgroundColor of the active filled SfTabView in focus state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewSelectedFilledTextColor
            <br/>
            <br/>
        </td>
        <td>
            TextColor of the selected filled SfTabView.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewSelectedFilledBackground
            <br/>
            <br/>
        </td>
        <td>
            BackgroundColor of the selected filled SfTabView.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTabViewDisabledFilledTextColor
            <br/>
            <br/>
        </td>
        <td>
            TextColor of the disabled filled SfTabView.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
		<td>
			SfTabViewActiveHoveredFilledBackground  
			<br/>
			<br/>
		</td>
		<td>
			Background color of the active filled SfTabView in hover state.
			<br/>
			<br/>
		</td>
	</tr>
	<tr>
		<td>
			SfTabViewDisabledTabBarBackground  
			<br/>
			<br/>
		</td>
		<td>
			Background color of the SfTabView tab bar when disabled.
			<br/>
			<br/>
		</td>
	</tr>
	<tr>
		<td>
			SfTabViewInActiveFocusedBackground  
			<br/>
			<br/>
		</td>
		<td>
			Background color of the inactive SfTabView in focus state.
			<br/>
			<br/>
		</td>
	</tr>
	<tr>
		<td>
			SfTabViewNormalFontSize  
			<br/>
			<br/>
		</td>
		<td>
			Font size of the text in the SfTabView when in normal state.
			<br/>
			<br/>
		</td>
	</tr>
	<tr>
		<td>
			SfTabViewNormalTabBarBackground  
			<br/>
			<br/>
		</td>
		<td>
			Background color of the SfTabView tab bar in normal state.
			<br/>
			<br/>
		</td>
	</tr>
	<tr>
		<td>
			SfTabViewScrollButtonBackground  
			<br/>
			<br/>
		</td>
		<td>
			Background color of the SfTabView scroll button.
			<br/>
			<br/>
		</td>
	</tr>
	<tr>
		<td>
			SfTabViewScrollButtonDisabledIconColor  
			<br/>
			<br/>
		</td>
		<td>
			Icon color of the SfTabView scroll button when disabled.
			<br/>
			<br/>
		</td>
	</tr>
	<tr>
		<td>
			SfTabViewScrollButtonIconColor  
			<br/>
			<br/>
		</td>
		<td>
			Icon color of the SfTabView scroll button.
			<br/>
			<br/>
		</td>
	</tr>
	<tr>
		<td>
			SfTabViewInActiveNormalTextColor  
			<br/>
			<br/>
		</td>
		<td>
			Text color of the inactive SfTabView in normal state.
			<br/>
			<br/>
		</td>
	</tr>
	<tr>
        <td>
            SfTabViewDisabledFilledBackground
            <br/>
            <br/>
        </td>
        <td>
            BackgroundColor of the disabled filled SfTabView.
            <br/>
            <br/>
        </td>
    </tr>
</table>

## SfTextInputLayout

<table>
    <tr>
        <th>Theme Dictionary<br/> 
            <br/></th>        
        <th>
          Keys
            <br/>
            <br/>
        </th>
        <th>
            Description
            <br/>
            <br/>
        </th>
    </tr>

    <tr>
        <td rowspan="11">
            SfTextInputLayoutStyles 
            <br/>
            <br/>
        </td>
		<td>
           SfTextInputLayoutTheme 
            <br/>
            <br/>
        </td>
        <td>    
            By merging this key in application resources, you can customize the appearance of SfTextInputLayout without merging common theme resource and control style resource dictionaries.
			
{% highlight xaml %}

<Application xmlns:syncTheme="clr-namespace:Syncfusion.Maui.Toolkit.Themes;assembly=Syncfusion.Maui.Toolkit"
             ...>
 <Application.Resources>
    <ResourceDictionary>
        <ResourceDictionary.MergedDictionaries>
            <syncTheme:SyncfusionThemeResourceDictionary />
            <ResourceDictionary>
                <x:String x:Key="SfTextInputLayoutTheme">CommonTheme</x:String>
                <Color x:Key="SfTextInputLayoutStroke">Yellow</Color>
                <Color x:Key="SfTextInputLayoutContainerBackground">Pink</Color>
            </ResourceDictionary>
        </ResourceDictionary.MergedDictionaries>
    </ResourceDictionary>
 </Application.Resources>
 </Application>

{% endhighlight %}
            <br/>
            <br/>
        </td>
        </tr>
    <tr>
        <td>
            SfTextInputLayoutNormalContainerBackground  
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfTextInputLayout background in normal state.
            <br/>
            <br/>
        </td>
    </tr>
        <tr>
        <td>
            SfTextInputLayoutStroke  
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfTextInputLayout stroke.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTextInputLayoutMouseHoveredContainerBackground
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfTextInputLayout background text in hover state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTextInputLayoutContainerBackground  
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfTextInputLayout background.
            <br/>
            <br/>
        </td>
    </tr>
     <tr>
        <td>
            SfTextInputLayoutHoveredStroke
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfTextInputLayout stroke in hover state.
            <br/>
            <br/>
        </td>
    </tr>
      <tr>
        <td>
            SfTextInputLayoutFocusedContainerBackground
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfTextInputLayout background in focused state.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTextInputLayoutCommonStroke 
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfTextInputLayout common stroke.
            <br/>
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            SfTextInputLayoutDisabledContainerBackground
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfTextInputLayout background in disabled state.
            <br/>
            <br/>
        </td>
    </tr>
     <tr>
        <td>
            SfTextInputLayoutDisabledStroke
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfTextInputLayout stroke in disabled state.
            <br/>
            <br/>
        </td>
    </tr>
     <tr>
        <td>
            SfTextInputLayoutErrorStroke
            <br/>
            <br/>
        </td>
        <td>
            Color of the SfTextInputLayout error stroke.
            <br/>
            <br/>
        </td>
    </tr>
</table> 