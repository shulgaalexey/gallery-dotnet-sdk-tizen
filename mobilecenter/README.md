Tracking Tizen Mobile App Analytics
===================================


Do you want to know how many users launch you App daily, weekly, monthly?

How long do the stay with you app on?

Where are they coming from and which smartphones are they on?

What features do they use the most?

In other words, did you consider adding Continuous Monitoring and Analytics into you Tizen Mobile App?
Let’s see how we can do it.

In this article we will show how to track Analytics of your Tizen Mobile App by using [Microsoft Visual Studio Mobile Center Analytics](https://docs.microsoft.com/en-us/mobile-center/analytics/), specifically tailored for Tizen App Developers by Tizen Platform Lab in partnership with Microsoft.

*Note. By the end of 2017 Analytics service is available in Preview mode for Tizen, Android, iOS, React Native, UWP and Xamarin.*



What is Mobile App Analytics?
-----------------------------

Mobile App Analytics is a multi-modal statistical and technical data, registered in the mobile app in the running time. It lets developers understand their end-user population, such as number of daily, weekly and monthly users, session duration, top devices, as well as usage patterns: the custom event tracking feature allows collecting rich behavioral insights.

![alt text](https://github.com/shulgaalexey//gallery-dotnet-sdk-tizen/blob/raw/item/mobilecenter/mobilecenter/pics/Tracking_Tizen_Mobile_App_Analytics_1.png "Tracking Tizen Mobile App Analytics")

All that data may be collected and visualized by different mobile app measurement tools and one of them, carefully tuned for Tizen, is Microsoft Visual Studio Mobile Center Analytics. The Mobile Center .NET SDK, integrated into your app, provides a set of C# APIs to send the Analytics directly to the Mobile Center Portal where it is visualized in figures and diagrams on the online dashboard. Following chapters demonstrate the usage of both API and Web Portal in a practical example.


Prerequisites
-------------

We assume that you already have basic knowledge in Tizen Xamarin App development. For basic information, see [https://developer.tizen.org/development/preview/getting-started](https://developer.tizen.org/development/preview/getting-started).

Make sure that your project is set up in Visual Studio and you are targeting Tizen Mobile devices. The instructions how to install Visual Studio Tools for Tizen are found there:
[https://developer.tizen.org/development/tizen-.net-preview/getting-started/installing-visual-studio-tools-tizen](https://developer.tizen.org/development/tizen-.net-preview/getting-started/installing-visual-studio-tools-tizen).


The Mobile Center API requires privileges to use the Internet and onboard SQLite DB for offline data preservation, so you should add following privileges to your Tizen Mobile App manifest:

```
<privileges>
    <privilege>http://tizen.org/privilege/internet</privilege>
    <privilege>http://tizen.org/privilege/network.get</privilege>
</privileges>
```

For integrating the Mobile Center Analytics into your app it is enough to add few .NET references which include Mobile Center SDK and its dependencies, required for Internet and storage operations. Navigate to the **Project -> Manage NuGet Packages...** and add to your Tizen Mobile App the following nupkgs with specified versions.

* Tizen.Applications, version 1.5.8
* Microsoft.Rest.ClientRuntime, version 2.3.6
* Newtonsoft.Json, version 10.0.2
* sqlite-net-pcl, version 1.3.1
* SQLitePCLRaw.core, version 1.1.2
* SQLitePCLRaw.provider.sqlite3.netstandard11, version 1.1.2

Note. Temporary the Tizen-compatible SDK is not available on the Nuget Gallery, so you can build it from the source codes.

1. Clone the SDK to your computer from the GitHub [https://github.com/Microsoft/mobile-center-sdk-dotnet/tree/Tizen/Preview](https://github.com/Microsoft/mobile-center-sdk-dotnet/tree/Tizen/Preview) and switch to Tizen/Preview branch:

```
git clone https://github.com/Microsoft/mobile-center-sdk-dotnet.git
cd mobile-center-sdk-dotnet
git checkout Tizen/Preview
```

2. Open the MobileCenter-SDK-Build-Tizen.sln solution in Visual Studio and build it.

3. Add SDK libraries to your Tizen Mobile App. Navigate to the **Project -> Add Reference… -> Browse**, press **Browse** button and select following two dlls:

```
./SDK/MobileCenter/Microsoft.Azure.Mobile.Tizen/bin/Release/Microsoft.Azure.Mobile.dll
./SDK/MobileCenterAnalytics/Microsoft.Azure.Mobile.Analytics.Tizen/bin/Release/Microsoft.Azure.Mobile.Analytics.dll
```

