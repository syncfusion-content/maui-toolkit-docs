---
layout: post
title: How to Customize Theming in Syncfusion® Controls
description: Learn how to switch between light and dark themes in Syncfusion® Maui controls, along with additional feature details.
platform: maui-toolkit
control: General
documentation: UG
---

# Switching Between Light Theme and Dark Theme

Refer to the following example code to switch between light and dark themes in Syncfusion<sup>®</sup> MAUI controls.

{% highlight C# %} 
void UpdateTheme(object sender, System.EventArgs e)
{
    ICollection<ResourceDictionary> mergedDictionaries = Application.Current.Resources.MergedDictionaries;
    if (mergedDictionaries != null)
    {
        var theme = mergedDictionaries.OfType<SyncfusionThemeResourceDictionary>().FirstOrDefault();
        if (theme != null)
        {
            if (theme.VisualTheme is SfVisuals.MaterialDark)
            {
                theme.VisualTheme = SfVisuals.MaterialLight;
            }
            else
            {
                theme.VisualTheme = SfVisuals.MaterialDark;
            }
        }
     }
}

{% endhighlight %}

The complete theme switch sample is available in this [link](https://github.com/SyncfusionExamples/maui-toolkit-samples/tree/master/Theme/SyncfusionThemeSample).