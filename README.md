# MauiWeather
# Weather Forecast API
- https://open-meteo.com/en/docs#hourly=&daily=weathercode,temperature_2m_max,temperature_2m_min&current_weather=true&timezone=auto
- API URL (Open in new tab or copy this URL into your application)

## Paste json as classes C#

    public class WeatherData
    {
        public float latitude { get; set; }
        public float longitude { get; set; }
        public float generationtime_ms { get; set; }
        public int utc_offset_seconds { get; set; }
        public string timezone { get; set; }
        public string timezone_abbreviation { get; set; }
        public float elevation { get; set; }
        public Current_Weather current_weather { get; set; }
        public Daily_Units daily_units { get; set; }
        public Daily daily { get; set; }
        public ObservableCollection<Daily2> daily2 { get; set; } = new ObservableCollection<Daily2>();
    }
    
    public class Current_Weather
    {
        public float temperature { get; set; }
        public float windspeed { get; set; }
        public float winddirection { get; set; }
        public int weathercode { get; set; }
        public int is_day { get; set; }
        public string time { get; set; }
    }
    
    public class Daily_Units
    {
        public string time { get; set; }
        public string weathercode { get; set; }
        public string temperature_2m_max { get; set; }
        public string temperature_2m_min { get; set; }
    }
    
    public class Daily
    {
        public string[] time { get; set; }
        public int[] weathercode { get; set; }
        public float[] temperature_2m_max { get; set; }
        public float[] temperature_2m_min { get; set; }
    }
    
    public class Daily2
    {
        public string time { get; set; }
        public int weathercode { get; set; }
        public float temperature_2m_max { get; set; }
        public float temperature_2m_min { get; set; }
    }


  
## Package Reference

- PropertyChanged.Fody
- SkiaSharp.Extended.UI.Maui

## Model class WeatherData

## Add this code Style into App.xaml
    <Application.Resources>
        <ResourceDictionary>
            <ResourceDictionary.MergedDictionaries>
                <ResourceDictionary Source="Resources/Styles/Colors.xaml" />
                <ResourceDictionary Source="Resources/Styles/Styles.xaml" />
                <ResourceDictionary Source="Resources/Styles/AppStyles.xaml" />
            </ResourceDictionary.MergedDictionaries>
        </ResourceDictionary>
    </Application.Resources>

## Add ResourceDictionary AppStyles into folder style then add this code
    <?xml version="1.0" encoding="utf-8" ?>
    <?xaml-comp compile="true" ?>
    <ResourceDictionary xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
                 xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml">

    <Style x:Key="MainStackLayout" TargetType="VerticalStackLayout">
        <Setter Property="Margin" Value="0,10,0,0"/>
        <Setter Property="Spacing" Value="15"/>
        <Setter Property="VerticalOptions" Value="Center"/>
    </Style>

    <Style TargetType="Label">
        <Setter Property="FontFamily" Value="Rubik"/>
        <Setter Property="HorizontalOptions" Value="Center"/>
        <Setter Property="VerticalOptions" Value="Center"/>
        <Setter Property="TextColor" Value="{StaticResource White}"/>
    </Style>

    <Style x:Key="Title" TargetType="Label">
        <Setter Property="FontAttributes" Value="Bold"/>
        <Setter Property="FontSize" Value="Large"/>
    </Style>

    <Style x:Key="WeatherTitle" TargetType="Label">
        <Setter Property="FontFamily" Value="RubikLight"/>
    </Style>

    <Style x:Key="WeatherValue" TargetType="Label">
        <Setter Property="FontAttributes" Value="Bold"/>
    </Style>

    <Style x:Key="Card" TargetType="Frame">
        <Setter Property="Padding" Value="0"/>
        <Setter Property="Opacity" Value=".1"/>
        <Setter Property="CornerRadius" Value="25"/>
        <Setter Property="WidthRequest" Value="150"/>
        <Setter Property="HeightRequest" Value="150"/>
        <Setter Property="BorderColor" Value="Transparent"/>
        <Setter Property="BackgroundColor" Value="{StaticResource CardBlue}"/>
    </Style>


    <Style x:Key="card" TargetType="Frame">
        <Setter Property="Padding" Value="0" />
        <Setter Property="Opacity" Value=".1" />
        <Setter Property="CornerRadius" Value="25" />
        <Setter Property="WidthRequest" Value="150" />
        <Setter Property="HeightRequest" Value="150" />
        <Setter Property="BorderColor" Value="Transparent" />
        <Setter Property="BackgroundColor" Value="{StaticResource CardBlue}" />

    </Style>
</ResourceDictionary>


![MainPage](https://github.com/salisou/MauiWeather/blob/main/Images/MainPage.PNG)
![MianPage2](https://github.com/salisou/MauiWeather/blob/main/Images/MianPage2.PNG)
