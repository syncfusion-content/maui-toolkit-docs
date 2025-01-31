---
layout: post
title: Set Sliding Panel Content in .NET MAUI Navigation Drawer | Syncfusion®
description: Learn here all about Setting Sliding Panel Content support in Syncfusion® .NET MAUI Navigation Drawer (SfNavigationDrawer) control and more.
platform: maui-toolkit
control: NavigationDrawer
documentation: ug
---

# Set Sliding Panel Content in .NET MAUI Navigation Drawer

The drawer pane content is only viewable when the drawer is in the open state. Its content can be set as:

*	Header Content

*	Drawer Content

*	Footer Content

N> Header and Footer content is optional, but the Drawer content is mandatory to allocate space for the drawer.
		
## Header Content

As the name suggests, it is displayed at the top of the drawer. The [DrawerHeaderView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.DrawerSettings.html#Syncfusion_Maui_Toolkit_NavigationDrawer_DrawerSettings_DrawerHeaderView) property is used to set the header content of the drawer.

{% tabs %}

{% highlight xaml %}

<navigationdrawer:SfNavigationDrawer x:Name="navigationDrawer">
    <navigationdrawer:SfNavigationDrawer.DrawerSettings>
        <navigationdrawer:DrawerSettings>
            <navigationdrawer:DrawerSettings.DrawerHeaderView>
                <Grid BackgroundColor="#6750A4">
                    <Label Text="Header View"
                            TextColor="White"
                            HorizontalOptions="Center"
                            VerticalOptions="Center"/>
                </Grid>
            </navigationdrawer:DrawerSettings.DrawerHeaderView>
        </navigationdrawer:DrawerSettings>
    </navigationdrawer:SfNavigationDrawer.DrawerSettings>
</navigationdrawer:SfNavigationDrawer>

{% endhighlight %}

{% highlight c# %}

SfNavigationDrawer navigationDrawer = new SfNavigationDrawer();
DrawerSettings drawerSettings = new DrawerSettings();

Grid headerGrid = new Grid()
{
    BackgroundColor = Color.FromArgb("#6750A4"),
};

Label headerLabel = new Label()
{
    Text = "Header View",
    TextColor = Colors.White,
    HorizontalOptions = LayoutOptions.Center,
    VerticalOptions = LayoutOptions.Center,
};

headerGrid.Children.Add(headerLabel);
drawerSettings.DrawerHeaderView = headerGrid;
navigationDrawer.DrawerSettings = drawerSettings;
this.Content = navigationDrawer;
  
{% endhighlight %}

{% endtabs %}

![Header](Images/panel-content/navigation_drawer_header.png)

## Header Height

The height of the drawer header content can be adjusted using the [DrawerHeaderHeight](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.DrawerSettings.html#Syncfusion_Maui_Toolkit_NavigationDrawer_DrawerSettings_DrawerHeaderHeight) property.

N> The [DrawerHeaderView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.DrawerSettings.html#Syncfusion_Maui_Toolkit_NavigationDrawer_DrawerSettings_DrawerHeaderView) can be removed by setting the [DrawerHeaderHeight](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.DrawerSettings.html#Syncfusion_Maui_Toolkit_NavigationDrawer_DrawerSettings_DrawerHeaderHeight) to zero.

{% tabs %}

{% highlight xaml %}
    
<navigationdrawer:SfNavigationDrawer x:Name="navigationDrawer">
    <navigationdrawer:SfNavigationDrawer.DrawerSettings>
        <navigationdrawer:DrawerSettings DrawerHeaderHeight="150">
            <navigationdrawer:DrawerSettings.DrawerHeaderView>
                <Grid BackgroundColor="#6750A4">
                    <Label Text="Header View"
                            TextColor="White"
                            HorizontalOptions="Center"
                            VerticalOptions="Center"/>
                </Grid>
            </navigationdrawer:DrawerSettings.DrawerHeaderView>
        </navigationdrawer:DrawerSettings>
    </navigationdrawer:SfNavigationDrawer.DrawerSettings>
</navigationdrawer:SfNavigationDrawer>

{% endhighlight %}

{% highlight c# %}

SfNavigationDrawer navigationDrawer = new SfNavigationDrawer();
DrawerSettings drawerSettings = new DrawerSettings()
{
    DrawerHeaderHeight = 150,
};

Grid headerGrid = new Grid()
{
    BackgroundColor = Color.FromArgb("#6750A4"),
};

Label headerLabel = new Label()
{
    Text = "Header View",
    TextColor = Colors.White,
    HorizontalOptions = LayoutOptions.Center,
    VerticalOptions = LayoutOptions.Center,
};

headerGrid.Children.Add(headerLabel);
drawerSettings.DrawerHeaderView = headerGrid;
navigationDrawer.DrawerSettings = drawerSettings;
this.Content = navigationDrawer;

{% endhighlight %}

{% endtabs %}

![Header height](Images/panel-content/navigation_drawer_header_height.png)

## Footer Content

As the name suggests, it is displayed at the bottom of the drawer. The [DrawerFooterView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.DrawerSettings.html#Syncfusion_Maui_Toolkit_NavigationDrawer_DrawerSettings_DrawerFooterView) property is used to set the footer content of the drawer.

{% tabs %}

{% highlight xaml %}

<navigationdrawer:SfNavigationDrawer x:Name="navigationDrawer">
    <navigationdrawer:SfNavigationDrawer.DrawerSettings>
        <navigationdrawer:DrawerSettings>
            <navigationdrawer:DrawerSettings.DrawerFooterView>
                <Grid BackgroundColor="#6750A4">
                    <Label Text="Footer View"
                        TextColor="White"
                        HorizontalOptions="Center"
                        VerticalOptions="Center"/>
                </Grid>
            </navigationdrawer:DrawerSettings.DrawerFooterView>
        </navigationdrawer:DrawerSettings>
    </navigationdrawer:SfNavigationDrawer.DrawerSettings>
</navigationdrawer:SfNavigationDrawer>

{% endhighlight %}

{% highlight c# %}

SfNavigationDrawer navigationDrawer = new SfNavigationDrawer();
DrawerSettings drawerSettings = new DrawerSettings();

Grid footerGrid = new Grid()
{
    BackgroundColor = Color.FromArgb("#6750A4"),
};

Label footerLabel = new Label()
{
    Text = "Footer View",
    TextColor = Colors.White,
    HorizontalOptions = LayoutOptions.Center,
    VerticalOptions = LayoutOptions.Center,
};

footerGrid.Children.Add(footerLabel);
drawerSettings.DrawerFooterView = footerGrid;
navigationDrawer.DrawerSettings = drawerSettings;
this.Content = navigationDrawer;

{% endhighlight %}

{% endtabs %}

![Footer](Images/panel-content/navigation_drawer_footer.png)

## Footer Height

The height of the drawer footer content can be adjusted using the [DrawerFooterHeight](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.DrawerSettings.html#Syncfusion_Maui_Toolkit_NavigationDrawer_DrawerSettings_DrawerFooterHeight) property.

N> The [DrawerFooterView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.DrawerSettings.html#Syncfusion_Maui_Toolkit_NavigationDrawer_DrawerSettings_DrawerFooterView) can be removed by setting the [DrawerFooterHeight](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.DrawerSettings.html#Syncfusion_Maui_Toolkit_NavigationDrawer_DrawerSettings_DrawerFooterHeight) to zero.

{% tabs %}

{% highlight xaml %}

<navigationdrawer:SfNavigationDrawer x:Name="navigationDrawer">
    <navigationdrawer:SfNavigationDrawer.DrawerSettings>
        <navigationdrawer:DrawerSettings DrawerFooterHeight="150">
            <navigationdrawer:DrawerSettings.DrawerFooterView>
                <Grid BackgroundColor="#6750A4">
                    <Label Text="Footer View"
                           TextColor="White"
                           HorizontalOptions="Center"
                           VerticalOptions="Center"/>
                </Grid>
            </navigationdrawer:DrawerSettings.DrawerFooterView>
        </navigationdrawer:DrawerSettings>
    </navigationdrawer:SfNavigationDrawer.DrawerSettings>
</navigationdrawer:SfNavigationDrawer>
	
{% endhighlight %}

{% highlight c# %}
        
SfNavigationDrawer navigationDrawer = new SfNavigationDrawer();
DrawerSettings drawerSettings = new DrawerSettings()
{
    DrawerFooterHeight = 150,
};

Grid footerGrid = new Grid()
{
    BackgroundColor = Color.FromArgb("#6750A4"),
};

Label footerLabel = new Label()
{
    Text = "Footer View",
    TextColor = Colors.White,
    HorizontalOptions = LayoutOptions.Center,
    VerticalOptions = LayoutOptions.Center,
};

footerGrid.Children.Add(footerLabel);
drawerSettings.DrawerFooterView = footerGrid;
navigationDrawer.DrawerSettings = drawerSettings;
this.Content = navigationDrawer;
  
{% endhighlight %}

{% endtabs %}

![Footer height](Images/panel-content/navigation_drawer_footer_height.png)

## Drawer Content

The main content of the drawer is displayed between the header and footer content. It can be set using the [DrawerContentView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.DrawerSettings.html#Syncfusion_Maui_Toolkit_NavigationDrawer_DrawerSettings_DrawerContentView) property. The content view occupies the remaining space left by the header and footer content.

{% tabs %}

{% highlight xaml %}

<navigationdrawer:SfNavigationDrawer x:Name="navigationDrawer">
    <navigationdrawer:SfNavigationDrawer.DrawerSettings>
        <navigationdrawer:DrawerSettings>
            <navigationdrawer:DrawerSettings.DrawerContentView>
                <Grid BackgroundColor="#6750A4">
                    <Label Text="Drawer Content"
                           TextColor="White"
                           HorizontalOptions="Center"
                           VerticalOptions="Center"/>
                </Grid>
            </navigationdrawer:DrawerSettings.DrawerContentView>
        </navigationdrawer:DrawerSettings>
    </navigationdrawer:SfNavigationDrawer.DrawerSettings>
</navigationdrawer:SfNavigationDrawer>
	
{% endhighlight %}

{% highlight c# %}
        
SfNavigationDrawer navigationDrawer = new SfNavigationDrawer();
DrawerSettings drawerSettings = new DrawerSettings();

Grid contentGrid = new Grid()
{
    BackgroundColor = Color.FromArgb("#6750A4"),
};

Label contentLabel = new Label()
{
    Text = "Drawer Content",
    TextColor = Colors.White,
    HorizontalOptions = LayoutOptions.Center,
    VerticalOptions = LayoutOptions.Center,
};

contentGrid.Children.Add(contentLabel);
drawerSettings.DrawerContentView = contentGrid;
navigationDrawer.DrawerSettings = drawerSettings;
this.Content = navigationDrawer;
  
{% endhighlight %}

{% endtabs %}

![content](Images/panel-content/navigation_drawer_content.png)