---
layout: post
title: Container Type in .NET MAUI Text Input Layout control | Syncfusion®
description: Learn here all about Container Type support in Syncfusion® .NET MAUI Text Input Layout (SfTextInputLayout) control and more.
platform: maui-toolkit
control: SfTextInputLayout
documentation: ug
keywords: .net maui text input layout, syncfusion text input layout, text input layout maui.
---

# Container Type in .NET MAUI Text Input Layout (SfTextInputLayout)

Containers improve the discoverability of input view by creating a contrast between the input view and assistive elements.

## Filled

The background of the input view will be filled with container color, and its stroke (at the bottom edge) color and thickness will be changed based on its states. It can be enabled by setting the [ContainerType](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.SfTextInputLayout.html#Syncfusion_Maui_Toolkit_TextInputLayout_SfTextInputLayout_ContainerType) property to [Filled](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.ContainerType.html#Syncfusion_Maui_Toolkit_TextInputLayout_ContainerType_Filled).

{% tabs %} 

{% highlight xaml %} 

<inputLayout:SfTextInputLayout Hint="Name"
                               ContainerType="Filled">
    <Entry Text="John"/>
</inputLayout:SfTextInputLayout>  

{% endhighlight %}

{% highlight C# %} 

var inputLayout = new SfTextInputLayout();
inputLayout.Hint = "Name";
inputLayout.ContainerType = ContainerType.Filled;
inputLayout.Content = new Entry() { Text = "John" }; 

{% endhighlight %}

{% endtabs %}

![.NET MAUI TextInputLayout with Filled container type.](images/ContainerType/Filled_Focused.jpg)

## Outlined

When setting the [ContainerType](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.SfTextInputLayout.html#Syncfusion_Maui_Toolkit_TextInputLayout_SfTextInputLayout_ContainerType) property to [Outlined](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.ContainerType.html#Syncfusion_Maui_Toolkit_TextInputLayout_ContainerType_Outlined), the container will be covered with a rounded-corner border.

{% tabs %} 

{% highlight xaml %} 

<inputLayout:SfTextInputLayout Hint="Name"
                               ContainerType="Outlined">
    <Entry Text="John" />
</inputLayout:SfTextInputLayout>  
 
{% endhighlight %}

{% highlight C# %} 

var inputLayout = new SfTextInputLayout();
inputLayout.Hint = "Name";
inputLayout.ContainerType = ContainerType.Outlined;
inputLayout.Content = new Entry() { Text = "John" }; 

{% endhighlight %}

{% endtabs %}

![.NET MAUI TextInputLayout with Outlined container type.](images/ContainerType/Outlined.png)

### Customize the corner radius of the outline border 

When setting the [OutlineCornerRadius](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.SfTextInputLayout.html#Syncfusion_Maui_Toolkit_TextInputLayout_SfTextInputLayout_OutlineCornerRadius) property to double value, the corner radius of the container will be changed.

{% tabs %}

{% highlight xaml %}

<inputLayout:SfTextInputLayout Hint="Name" 
                               ContainerType="Outlined"
                               OutlineCornerRadius="8">
    <Entry />
</inputLayout:SfTextInputLayout>  
			
{% endhighlight %}

{% highlight c# %}

var inputLayout = new SfTextInputLayout();
inputLayout.Hint = "Name";
inputLayout.ContainerType = ContainerType.Outlined;
inputLayout.OutlineCornerRadius = 8;
inputLayout.Content = new Entry(); 

{% endhighlight %}

{% endtabs %}

![.NET MAUI TextInputLayout with OutlineCornerRadius.](images/ContainerType/CornerRadius.png)

>**NOTE**
It is applicable for the outline border when setting the container type to `Outlined`.

### Custom Padding

Spaces around the input view can be customized by setting the [InputViewPadding](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.SfTextInputLayout.html#Syncfusion_Maui_Toolkit_TextInputLayout_SfTextInputLayout_InputViewPadding) property to [Thickness](https://learn.microsoft.com/en-us/dotnet/api/microsoft.maui.thickness?view=net-maui-8.0) value.

{% tabs %} 

{% highlight xaml %} 

<inputLayout:SfTextInputLayout Hint="Padding"
                               InputViewPadding="0,5,0,5" 
                               ContainerType="Outlined"
                               HelperText="Top and bottom padding is 5">
    <Entry />
 </inputLayout:SfTextInputLayout> 

{% endhighlight %}

{% highlight C# %} 

var inputLayout = new SfTextInputLayout();
inputLayout.Hint = "Padding";
inputLayout.InputViewPadding = new Thickness(0,5,0,5);
inputLayout.ContainerType = ContainerType.Outlined;
inputLayout.HelperText = "Top and bottom padding is 5";
inputLayout.Content = new Entry(); 

{% endhighlight %}

{% endtabs %}

![Padding customization around the text input view.](images/ContainerType/padingg.png)

## None

When setting the [ContainerType](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.SfTextInputLayout.html#Syncfusion_Maui_Toolkit_TextInputLayout_SfTextInputLayout_ContainerType) property to [None](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.ContainerType.html#Syncfusion_Maui_Toolkit_TextInputLayout_ContainerType_None), the container will have an empty background and enough spacing.

{% tabs %} 

{% highlight xaml %} 

<inputLayout:SfTextInputLayout Hint="Name" 
                               ContainerType="None">
    <Entry Text="John" />
</inputLayout:SfTextInputLayout>  
 
{% endhighlight %}

{% highlight C# %} 

var inputLayout = new SfTextInputLayout();
inputLayout.Hint = "Name";
inputLayout.ContainerType = ContainerType.None;
inputLayout.Content = new Entry() { Text = "John" }; 

{% endhighlight %}

{% endtabs %}

![.NET MAUI TextInputLayout without container background.](images/ContainerType/None_focused.jpg)