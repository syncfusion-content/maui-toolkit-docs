---
layout: post
title: Events in .NET MAUI Bottom Sheet Control | Syncfusion®
description: Learn about event support in the Syncfusion® Toolkit for .NET MAUI Bottom Sheet (SfBottomSheet) control and more.
platform: maui-toolkit
control: SfBottomSheet
documentation: UG
---

# Events in .NET MAUI Bottom Sheet (SfBottomSheet)

## StateChanged event

The `StateChanged` event is triggered when the [State](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_State) property of the Bottom Sheet changes. This can occur either through user interaction, such as swiping the Bottom Sheet, or programmatically by setting the State property using XAML or C# code. The event's arguments are of type [StateChangedEventArgs](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.StateChangedEventArgs.html) and provide the following properties:

* `NewValue` : Gets the current state of the Bottom Sheet.
* `OldValue` : Gets the previous state of the Bottom Sheet.

{% tabs %}
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" StateChanged="OnStateChanged">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>

{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
this.Content = bottomSheet; 
bottomSheet.StateChanged += OnStateChanged;

{% endhighlight %}
{% endtabs %}

{% highlight c# %}

private void OnStateChanged(object sender, StateChangedEventArgs args)
{
    // Codes that need to be executed once the Sheet's state value is Changed.
}

{% endhighlight %}