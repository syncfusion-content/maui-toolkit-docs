---
layout: post
title: Swiping in .NET MAUI Bottom Sheet | Syncfusion
description: Learn here all about swiping support in Syncfusion .NET MAUI Bottom Sheet (SfBottomSheet) control and more.
platform: maui-toolkit
control: BottomSheet
documentation: ug
---
# Swiping in .NET MAUI Bottom Sheet (SfBottomSheet)

The BottomSheet supports the swiping for expanding the sheet. 

## Enable Swiping

The `EnableSwiping` property allows you to enable or disable swipe functionality in the SfBottomSheet. By default, the EnableSwiping property is set to `true`.

{% tabs %}	
{% highlight xaml %}

<Grid>
     <VerticalStackLayout Padding="20">
         <Button Text="Open Bottom Sheet" WidthRequest="180" HeightRequest="40" Clicked="OpenBottomSheet"/>
     </VerticalStackLayout>
     <bottomSheet:SfBottomSheet x:Name="bottomSheet" ShowGrabber="True" EnableSwiping="True">
         <bottomSheet:SfBottomSheet.BottomSheetContent>
             <Grid BackgroundColor="#6750A4">
                 <Label Text="BottomSheet Content"  TextColor="White" VerticalOptions="Center" HorizontalOptions="Center"/>
             </Grid>
         </bottomSheet:SfBottomSheet.BottomSheetContent>
     </bottomSheet:SfBottomSheet>
</Grid>
	
{% endhighlight %}
{% highlight c# %}

var button = new Button
{
    WidthRequest = 180,
    HeightRequest = 40,
    Text= "Open Bottom Sheet"
};

button.Clicked += OpenBottomSheet;
var verticalStackLayout = new VerticalStackLayout
{
    Padding = new Thickness(20),
    Children = { button }
};

bottomSheet = new SfBottomSheet
{
    ShowGrabber = true,
};

var bottomSheetContent = new Grid
{
    BackgroundColor = Color.FromArgb("#6750A4")
};

var label = new Label
{
    Text = "BottomSheet Content",
    TextColor = Colors.White,
    VerticalOptions = LayoutOptions.Center,
    HorizontalOptions = LayoutOptions.Center
};

bottomSheetContent.Children.Add(label);
bottomSheet.BottomSheetContent = bottomSheetContent;
bottomSheet.EnableSwiping = true;
Grid grid = new Grid();
grid.Children.Add(verticalStackLayout);
grid.Children.Add(bottomSheet);
Content = grid;

{% endhighlight %}
{% endtabs %}

{% highlight c# %}

private void OpenBottomSheet(object sender, EventArgs e)
{
    bottomSheet.Show();
}

{% endhighlight %}

![Swiping Image for BottomSheet](images/swiping.gif)