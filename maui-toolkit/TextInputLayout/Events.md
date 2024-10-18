---
layout: post
title: Events in MAUI TextInputLayout control | Syncfusion
description: Learn about Events support in Syncfusion Toolkit for .NET MAUI TextInputLayout control, its elements, and more.
platform: maui-toolkit
control: SfTextInputLayout
documentation: ug
keywords: .net maui text input layout, syncfusion text input layout, text input layout maui.
---

# Events in MAUI TextInputLayout

## PasswordVisibilityToggled Event

The [PasswordVisibilityToggled](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.SfTextInputLayout.html#Syncfusion_Maui_Toolkit_TextInputLayout_SfTextInputLayout_PasswordVisibilityToggled) event will be triggered whenever you toggle the password toggle icon in the `SfTextInputLayout`. The event arguments are of type [PasswordVisibilityToggledEventArgs](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.PasswordVisibilityToggledEventArgs.html) and expose the following property:

* [IsPasswordVisible](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.PasswordVisibilityToggledEventArgs.html#Syncfusion_Maui_Toolkit_TextInputLayout_PasswordVisibilityToggledEventArgs_IsPasswordVisible): Its value is defined based on the visibility of the password.

N> Ensure that [EnablePasswordVisibilityToggle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TextInputLayout.SfTextInputLayout.html#Syncfusion_Maui_Toolkit_TextInputLayout_SfTextInputLayout_EnablePasswordVisibilityToggle) property is enabled for the `PasswordVisibilityToggled` event to function as expected.

{% tabs %} 
{% highlight xaml %}

<inputLayout:SfTextInputLayout  Hint="Password" 
                                EnablePasswordVisibilityToggle="True"
                                PasswordVisibilityToggled="OnPasswordVisibilityToggled">
    <Entry Text="1234"/>
</inputLayout:SfTextInputLayout>  
 
{% endhighlight %}

{% highlight C# %}

var inputLayout = new SfTextInputLayout();
inputLayout.Hint = "Password";
inputLayout.EnablePasswordVisibilityToggle = true;
inputLayout.PasswordVisibilityToggled += OnPasswordVisibilityToggled;
inputLayout.Content = new Entry() { Text = "1234" }; 

{% endhighlight %}

{% endtabs %}

{% tabs %}
{% highlight c# %}
    
private void OnPasswordVisibilityToggled(object sender, PasswordVisibilityToggledEventArgs e)
{
   	bool passwordVisbility = e.IsPasswordVisible;
}

{% endhighlight %}
{% endtabs %}