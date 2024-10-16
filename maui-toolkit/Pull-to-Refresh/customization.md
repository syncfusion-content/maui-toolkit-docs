---
layout: post
title: Customization in .NET MAUI PullToRefresh control | Syncfusion
description: Learn about customization features support in Syncfusion .NET MAUI PullToRefresh (SfPullToRefresh) control and more.
platform: maui-toolkit
control: SfPullToRefresh
documentation: ug
---

# Customization in .NET MAUI PullToRefresh (SfPullToRefresh)

The .NET MAUI PullToRefresh control supports customization of various features, including TransitionMode, PullingThreshold, ProgressBackground, ProgressColor, and more. The control can be personalized using the following properties.

## PullableContent

The [PullableContent](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.PullToRefresh.SfPullToRefresh.html#Syncfusion_Maui_PullToRefresh_SfPullToRefresh_PullableContent) is the main view of the [PullToRefresh](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.PullToRefresh.SfPullToRefresh.html) control on which the desired items can be placed.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="6 11" %}

<PullToRefreshControl:SfPullToRefresh x:Name="pullToRefresh"
                                      PullingThreshold="120"
                                      RefreshViewHeight="30"
                                      RefreshViewThreshold="30"
                                      RefreshViewWidth="30">
    <PullToRefreshControl:SfPullToRefresh.PullableContent>
            <Label x:Name="Monthlabel" 
                    TextColor="White" 
                    HorizontalTextAlignment="Center"   
                    VerticalTextAlignment="Start" />
    </PullToRefreshControl:SfPullToRefresh.PullableContent>
</PullToRefreshControl:SfPullToRefresh>

{% endhighlight %}
{% endtabs %}

## TransitionMode

The [TransitionMode](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.PullToRefresh.SfPullToRefresh.html#Syncfusion_Maui_PullToRefresh_SfPullToRefresh_TransitionMode) property specifies the mode of the animations. It has the following two modes:

* [SlideOnTop](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.PullToRefresh.PullToRefreshTransitionType.html#Syncfusion_Maui_PullToRefresh_PullToRefreshTransitionType_SlideOnTop)
* [Push](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.PullToRefresh.PullToRefreshTransitionType.html#Syncfusion_Maui_PullToRefresh_PullToRefreshTransitionType_Push)

The default transition is `SlideOnTop` that draws the RefreshView on top of the `PullableContent`.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="2" %}

<PullToRefreshControl:SfPullToRefresh x:Name="pullToRefresh" 
                                      TransitionMode="SlideOnTop" />

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.TransitionMode = PullToRefreshTransitionType.SlideOnTop;

{% endhighlight %}
{% endtabs %}

![.NET MAUI PullToRefresh with slide on top transition mode.](Images/customization/net-maui-pulltorefresh-getting-started.png)

The following code example shows how to set the `TransitionMode` as `Push` to PullToRefresh. This transition moves the refresh content and main content simultaneously.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="2" %}

<PullToRefreshControl:SfPullToRefresh x:Name=" pullToRefresh" 
                                      TransitionMode="Push" />

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.TransitionMode = PullToRefreshTransitionType.Push;

{% endhighlight %}
{% endtabs %}

![.NET MAUI PullToRefresh with push transition mode.](Images/customization/net-maui-pulltorefresh-getting-started-push.png)

## RefreshViewThreshold

The threshold value for the refresh view, indicating the starting position of the progress indicator within the view.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="2" %}

<PullToRefreshControl:SfPullToRefresh x:Name="pullToRefresh" 
                                      RefreshViewThreshold="50"/>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.RefreshViewThreshold = 50d;

{% endhighlight %}
{% endtabs %}

## PullingThreshold

The threshold value for the refresh view, indicating the progress indicator's maximum pulling position in view.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="2" %}

<PullToRefreshControl:SfPullToRefresh x:Name="pullToRefresh" 
                            PullingThreshold="200"/>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.PullingThreshold = 200d;

{% endhighlight %}
{% endtabs %}


## IsRefreshing

The view will get refresh while the [IsRefreshing](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.PullToRefresh.SfPullToRefresh.html#Syncfusion_Maui_PullToRefresh_SfPullToRefresh_IsRefreshing) property is set to `true,` and View refreshing will be stopped when you set the `IsRefreshing` to `false.`
 
{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="2" %}

<PullToRefreshControl:SfPullToRefresh x:Name="pullToRefresh" 
                                      IsRefreshing="True"/>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.IsRefreshing = true;

{% endhighlight %}
{% endtabs %}


## ProgressBackground

The color to the progress indicator's background.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="2" %}

<PullToRefreshControl:SfPullToRefresh x:Name="pullToRefresh" 
                                      ProgressBackground = "White"/>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.ProgressBackground = Color.White;

{% endhighlight %}
{% endtabs %}


## ProgressColor

The color to the progress indicator's arc. 

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="2" %}

<PullToRefreshControl:SfPullToRefresh x:Name="pullToRefresh" 
                                      ProgressColor = "Blue"/>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.ProgressColor = Color.Blue;

{% endhighlight %}

{% endtabs %}


## ProgressThickness

The width of the progress indicator's arc. 

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="2" %}

<PullToRefreshControl:SfPullToRefresh x:Name="pullToRefresh" 
                                      ProgressThickness="5"/>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.ProgressThickness = 5d;

{% endhighlight %}
{% endtabs %}


## RefreshViewWidth

The width of the refresh view.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="2" %}

<PullToRefreshControl:SfPullToRefresh x:Name="pullToRefresh" 
                                      RefreshViewWidth="50"/>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.RefreshViewWidth = 50d;

{% endhighlight %}

{% endtabs %}


## RefreshViewHeight

The height to the refresh View.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="2" %}

<PullToRefreshControl:SfPullToRefresh x:Name="pullToRefresh" 
                                      RefreshViewHeight="50"/>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.RefreshViewHeight = 50d;

{% endhighlight %}
{% endtabs %}


## Programmatic Support 

### StartRefreshing()

The [StartRefreshing](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.PullToRefresh.SfPullToRefresh.html#Syncfusion_Maui_PullToRefresh_SfPullToRefresh_StartRefreshing) method is used to refresh the content without interaction in pullable content. When you invoke this StartRefreshing() method,then the Progress indicator will be shown. 

{% tabs %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.StartRefreshing();

{% endhighlight %}
{% endtabs %}

### EndRefreshing()

The [EndRefreshing](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.PullToRefresh.SfPullToRefresh.html#Syncfusion_Maui_PullToRefresh_SfPullToRefresh_EndRefreshing) method is used to end the progress animation of the `PullToRefresh`.

{% tabs %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.EndRefreshing();

{% endhighlight %}
{% endtabs %}



The `PullToRefresh` allows you to set a template for pulling and refreshing the view. The pulling and refreshing a template can be set using the [SfPullToRefresh.PullingViewTemplate](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.PullToRefresh.SfPullToRefresh.html#Syncfusion_Maui_PullToRefresh_SfPullToRefresh_PullingViewTemplate) and [SfPullToRefresh.RefreshingViewTemplate](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.PullToRefresh.SfPullToRefresh.html#Syncfusion_Maui_PullToRefresh_SfPullToRefresh_RefreshingViewTemplate) properties, respectively.

Refer to the following code example in which a [SfCircularProgressBar](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.ProgressBar.SfCircularProgressBar.html?tabs=tabid-1) is loaded in the pulling view template and refreshing view template.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="23 24 36 37" %}

    <ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             x:Class="PullToRefreshTemplate.MainPage"
             xmlns:sfgrid="clr-namespace:Syncfusion.Maui.DataGrid;assembly=Syncfusion.Maui.DataGrid"
             xmlns:pulltoRefresh="clr-namespace:Syncfusion.Maui.PullToRefresh;assembly=Syncfusion.Maui.PullToRefresh"
             xmlns:local="clr-namespace:PullToRefreshTemplate">

        <ContentPage.Behaviors>
            <local:PullToRefreshTemplateBehavior />
        </ContentPage.Behaviors>

        <ContentPage.Content>
            <Grid>
                <pulltoRefresh:SfPullToRefresh x:Name="pullToRefresh"
                                            RefreshViewHeight="50"
                                            RefreshViewThreshold="30"
                                            PullingThreshold="150"
                                            RefreshViewWidth="50"
                                            ProgressThickness='{OnPlatform Android="3", Default="2"}'
                                            TransitionMode="SlideOnTop"
                                            Margin="{StaticResource margin}"
                                            IsRefreshing="False">
                    <pulltoRefresh:SfPullToRefresh.PullableContent>
                        <sfgrid:SfDataGrid x:Name="dataGrid"
                                        HeaderRowHeight="52"
                                        RowHeight="48"
                                        SortingMode="Single"
                                        ItemsSource="{Binding OrdersInfo}"
                                        AutoGenerateColumnsMode="None"
                                        ColumnWidthMode="Fill"
                                        HorizontalScrollBarVisibility="Always"
                                        VerticalScrollBarVisibility="Always">
                            . . .
                            . . . .

                        </sfgrid:SfDataGrid>
                    </pulltoRefresh:SfPullToRefresh.PullableContent>
                </pulltoRefresh:SfPullToRefresh>
            </Grid>
        </ContentPage.Content>
    </ContentPage>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

    public class PullToRefreshTemplateBehavior : Behavior<ContentPage>
    {        
        protected override void OnAttachedTo(ContentPage bindable)
        {
            this.viewModel = new OrderInfoViewModel();
            this.progressbar = new SfCircularProgressBar();
            this.frame = new Frame();
            this.progressContent = new Label();

            this.progressContent.TextColor = Color.FromRgb(0, 124, 238);
            this.progressContent.FontSize = 9;
            this.progressContent.WidthRequest = 20;
            this.progressContent.HorizontalTextAlignment = TextAlignment.Center;

            this.frame.BorderColor = Colors.LightGray;
            this.frame.BackgroundColor = Colors.White;
            this.frame.CornerRadius = 30;
            this.frame.Content = this.progressbar;
            this.frame.Padding = 0;
            this.frame.HasShadow = false;

            this.progressbar.SegmentCount = 10;
            this.progressbar.ProgressThickness = 6;
            this.progressbar.ProgressRadiusFactor = 0.7;
            this.progressbar.SegmentGapWidth = 1;
            this.progressbar.WidthRequest = 55;
            this.progressbar.HeightRequest = 55;
            this.progressbar.IndeterminateAnimationDuration = 750;
            this.progressbar.Content = this.progressContent;

            bindable.BindingContext = this.viewModel;
            this.pullToRefresh = bindable.FindByName<Syncfusion.Maui.PullToRefresh.SfPullToRefresh>("pullToRefresh");
            this.dataGrid = bindable.FindByName<SfDataGrid>("dataGrid");
            this.dataGrid.ItemsSource = this.viewModel.OrdersInfo;
            this.pullToRefresh.Refreshing += this.PullToRefresh_Refreshing;
            this.pullToRefresh.Pulling += this.PullToRefresh_Pulling;

            var pullingTemplate = new DataTemplate(() =>
            {
                return new ViewCell { View = this.frame };
            });

            this.pullToRefresh.PullingViewTemplate = pullingTemplate;
            this.pullToRefresh.RefreshingViewTemplate = pullingTemplate;

            base.OnAttachedTo(bindable);
        }

        private void PullToRefresh_Pulling(object? sender, PullingEventArgs e)
        {
            this.progressbar!.TrackThickness = 0.8;
            this.progressbar.TrackRadiusFactor = 0.1;
            this.progressbar.IsIndeterminate = false;
            this.progressbar.ProgressFill = Color.FromRgb(0, 124, 238);
            this.progressbar.TrackFill = Colors.White;

            var absoluteProgress = Convert.ToInt32(Math.Abs(e.Progress));
            this.progressbar.Progress = absoluteProgress;
            this.progressbar.SetProgress(absoluteProgress, 1, Easing.CubicInOut);
            this.progressContent!.Text = e.Progress.ToString();
        }

        private async void PullToRefresh_Refreshing(object? sender, EventArgs e)
        {
            this.progressContent!.IsVisible = false;
            this.pullToRefresh!.IsRefreshing = true;
            await Task.Delay(10);
            await this.AnimateRefresh();
            this.viewModel!.RefreshItemsource(10);
            await Task.Delay(10);
            this.pullToRefresh.IsRefreshing = false;
            this.progressContent.IsVisible = true;
        }

        private async Task AnimateRefresh()
        {
            this.progressbar!.Progress = 0;
            this.progressbar.IsIndeterminate = true;

            await Task.Delay(750);
            this.progressbar.ProgressFill = Colors.Red;

            await Task.Delay(750);
            this.progressbar.ProgressFill = Colors.Green;

            await Task.Delay(750);
            this.progressbar.ProgressFill = Colors.Orange;

            await Task.Delay(750);
        }

    }

{% endhighlight %}
{% endtabs %}

![.NET MAUI PullToRefresh view Template.](Images/customization/net-maui-template-slideontop.gif)

N> [View sample in GitHub](https://github.com/SyncfusionExamples/load-datagrid-as-pullable-content-of-.net-maui-pull-to-refresh).