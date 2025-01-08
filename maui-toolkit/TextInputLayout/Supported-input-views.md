---
layout: post
title: Supported Input Views in .NET MAUI Text Input Layout | Syncfusion<sup>®</sup>
description: Learn here all about Supported Input Views support in the Syncfusion<sup>®</sup> .NET MAUI Text Input Layout (SfTextInputLayout) control and more.
platform: maui-toolkit
control: SfTextInputLayout
documentation: ug
keywords: .net maui text input layout, syncfusion text input layout, text input layout maui.
---

# Supported Input Views in .NET MAUI TextInputLayout (SfTextInputLayout)

Input views can be added to the text input layout control by setting the [Content](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SfContentView.html#Syncfusion_Maui_Toolkit_SfContentView_Content) property.

## Entry

To enter a single line text input, add [`Entry`](https://learn.microsoft.com/en-us/dotnet/maui/user-interface/controls/entry).

{% tabs %} 

{% highlight xaml %} 

<inputLayout:SfTextInputLayout Hint="Name"
                               HelperText="Enter your name"
                               ContainerType="Outlined">
   <Entry />
</inputLayout:SfTextInputLayout>  

{% endhighlight %}

{% highlight C# %} 

var inputLayout = new SfTextInputLayout();
inputLayout.Hint = "Name"; 
inputLayout.HelperText = "Enter your name";
inputLayout.ContainerType = ContainerType.Outlined;
inputLayout.Content = new Entry(); 

{% endhighlight %}

{% endtabs %}

![Entry in .NET MAUI TextInputLayout.](images/SupportedInputViews/Entry.png)

## Editor

To enter multi-line text input, add [`Editor`](https://learn.microsoft.com/en-us/dotnet/maui/user-interface/controls/editor), then set the [AutoSize](https://learn.microsoft.com/en-us/dotnet/api/microsoft.maui.controls.editor.autosize?view=net-maui-8.0#microsoft-maui-controls-editor-autosize) property to `TextChanges`.

{% tabs %} 

{% highlight xaml %} 

<inputLayout:SfTextInputLayout Hint="About TextInputLayout" 
                               HelperText="Enter the brief description of the text input layout"
                               ContainerType="Outlined">
   <Editor />
</inputLayout:SfTextInputLayout>  

{% endhighlight %}

{% highlight C# %} 

var inputLayout = new SfTextInputLayout();
inputLayout.Hint = "About TextInputLayout";
inputLayout.HelperText = "Enter the brief description of the text input layout";
inputLayout.Content = new Editor(); 

{% endhighlight %}

{% endtabs %}

![Editor in .NET MAUI TextInputLayout.](images/SupportedInputViews/Editor.jpg)

## Picker

To initialize the [Picker](https://learn.microsoft.com/en-us/dotnet/maui/user-interface/controls/picker) control and launch it in each platform, refer to the `getting started with picker` documentation.

{% tabs %}
{% highlight XAML %}

<inputLayout:SfTextInputLayout Hint="Fruit" 
                               HelperText="Select a fruit"
                               ContainerType="Outlined"
                               ContainerBackground="Transparent">
   <Picker SelectedItem="Apple">
        <Picker.ItemsSource>
            <x:Array Type="{x:Type x:String}">
                <x:String>Apple</x:String>
                <x:String>Orange</x:String>
                <x:String>Strawberry</x:String>
            </x:Array>
        </Picker.ItemsSource>
   </Picker>
</inputLayout:SfTextInputLayout> 

{% endhighlight %}
{% highlight C# %}

var inputLayout = new SfTextInputLayout();
inputLayout.Hint = "Fruit"; 
inputLayout.HelperText = "Select a fruit";
inputLayout.ContainerType = ContainerType.Outlined;
inputLayout.ContainerBackground = Colors.Transparent;
var picker = new Picker();
picker.Items.Add("Apple");
picker.Items.Add("Orange");
picker.Items.Add("Strawberry");
picker.SelectedItem = "Apple";
inputLayout.Content = picker;

{% endhighlight %}
{% endtabs %}

![Picker in .NET MAUI TextInputLayout.](images/SupportedInputViews/Picker.jpg)

N> Windows platform will not support `.NET MAUI Picker` as input view of the text input layout.

## TimePicker

To initialize the [TimePicker](https://learn.microsoft.com/en-us/dotnet/maui/user-interface/controls/timepicker) control and launch it in each platform, refer to the `getting started with time picker` documentation.

{% tabs %}
{% highlight XAML %}

 <inputLayout:SfTextInputLayout Hint="Time" 
                               HelperText="Select a start time"
                               ContainerType="Outlined"
                               ContainerBackground="Transparent">
    <TimePicker/>
 </inputLayout:SfTextInputLayout>

{% endhighlight %}
{% highlight C# %}

var inputLayout = new SfTextInputLayout();
inputLayout.Hint = "Time"; 
inputLayout.HelperText = "Select a start time";
inputLayout.ContainerType = ContainerType.Outlined;
inputLayout.ContainerBackground = Colors.Transparent;
inputLayout.Content = new TimePicker(); 

{% endhighlight %}
{% endtabs %}

![TimePicker in .NET MAUI TextInputLayout.](images/SupportedInputViews/TimePicker.jpg)

N> Windows platform will not support `.NET MAUI TimePicker` as input view of the text input layout.

## DatePicker

To initialize the [DatePicker]( https://learn.microsoft.com/en-us/dotnet/maui/user-interface/controls/DatePicker) control and launch it in each platform, refer to the `getting started with date picker` documentation.

{% tabs %}
{% highlight XAML %}

<inputLayout:SfTextInputLayout Hint="Date of Birth" 
                               HelperText="Select birth date"
                               ContainerType="Outlined"
                               ContainerBackground="Transparent">
    <DatePicker/>
</inputLayout:SfTextInputLayout> 

{% endhighlight %}
{% highlight C# %}

var inputLayout = new SfTextInputLayout();
inputLayout.Hint = "Date of Birth"; 
inputLayout.HelperText = "Select birth date";
inputLayout.ContainerType = ContainerType.Outlined;
inputLayout.ContainerBackground = Colors.Transparent;
inputLayout.Content = new DatePicker(); 

{% endhighlight %}
{% endtabs %}

![DatePicker in .NET MAUI TextInputLayout.](images/SupportedInputViews/DatePicker.jpg)

N> Windows platform will not support `.NET MAUI DatePicker` as input view of the text input layout.

