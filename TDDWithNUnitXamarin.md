TDD for Tizen App with NUnit Xamarin SDK
========================================



*by [@shulgaalexey](https://github.com/shulgaalexey)*



Are you developing Tizen Xamarin App and looking for a TDD framework?

Do you use NUnit TDD solutions on other mobile platforms and planning to integrate it on Tizen too?

Are you studying TDD for the very first time?

Read this step-by-step guide where you will find a detailed instructions on how to use nunit.xamarin test framework which is a cross-platform SDK with GUI and XML report generation features.

For the comprehensive NUnit feature coverage, please, visit the [project site](http://nunit.org/).


*Note. By the end of 2017 Tizen .NET and Tizen Xamarin Mobile and TV Apps are available in the Preview mode.*




## What is TDD?

[Test-driven development (TDD)](https://en.wikipedia.org/wiki/Test-driven_development) is a software development process that relies on the repetition of a very short development cycle: Requirements are turned into very specific test cases, then the software is improved to pass the new tests, only.
This test-first programming technique, created by [Kent Beck](https://en.wikipedia.org/wiki/Kent_Beck) is opposed to software development that allows software to be added that is not proven to meet requirements.


The sequence of steps in TDD is generally as following:

 - Add a test
 - Run all tests and see if the new one fails
 - Write some code
 - Run tests
 - Refactor code
 - Repeat


![A graphical representation of the test-driven development lifecycle](https://upload.wikimedia.org/wikipedia/commons/0/0b/TDD_Global_Lifecycle.png)


The TDD improves the quality and readability of your code, make it self documented and increase the overall productivity of the entire development process.

The proven approach declares that the test case life cycle should include phases of setup, execution, validation and cleanup.

Best practices recommend to separate set-up and teardown routines, common for a group of test cases.
You should always start unit test from a known and pre-configured state.
The ultimate target of the unit test is to ensure that the results and behaviour of the tested entitiy are correct.
On the other hand it is important to avoid complicated test cases ([KISS principle](https://en.wikipedia.org/wiki/KISS_principle)), test cases with inerdependencies (execution of one test shouldn't be interfered by another), "all-knowing oracles", slow running tests, and other "anti-patterns".


## How to get started?

First of all, we assume that you already have basic knowledge in Tizen Xamarin App development. For basic information, see [https://developer.tizen.org/development/preview/getting-started](https://developer.tizen.org/development/preview/getting-started).

For the instructions how to install Visual Studio Tools for Tizen, see [https://developer.tizen.org/development/tizen-.net-preview/getting-started/installing-visual-studio-tools-tizen](https://developer.tizen.org/development/tizen-.net-preview/getting-started/installing-visual-studio-tools-tizen).





## 1. Integrating nunit.xamarin in your project

### Code ninja way

TODO: Building nunit.xamarin out of sources from the GitHub


### You are the Boss of Continuous Integration

TODO: adding via nupkgs from the MyGet
TODO: add link to the CI article



## 2. Preparing test cases




## 3. Checking test report


### Quick glance on the GUI


### XML report






## What we learned today?

You can and, very likely, should develop your Tizen Mobile or TV App in a TDD manner.

We propose to use nunit.xamarin SDK which offers testing capcities of popular NUnit Framework together with GUI and XML reporting features.

Tizen .NET and Tizen Xamarin Mobile and TV Apps are in the Preview mode and you can try it free of charge.
Give it a try and develop your own well tested world class apps.


## What's next?

Read how you can integrate [Mobile Analytics](https://github.com/shulgaalexey/gallery-dotnet-sdk-tizen/blob/master/MobileCenterAnalytics.md) into your Tizen Xamarin App

Study how can you set up Continuous Integration of your Tizen App Development Process
TODO: add link

Check out the [Gallery of 3rd Party C# API](https://shulgaalexey.github.io/gallery-dotnet-sdk-tizen/) available for Tizen




## Reference


* Tizen Developer page: [https://developer.tizen.org/](https://developer.tizen.org/)
* Sample application used for TDD demonstration: TODO link
* TODO nunit.xamarin for Tizen GitHub
* TODO ninut.xamarin for Tizen MyGet
* TODO NUnit home page
* [TDD on Wikipedia](https://en.wikipedia.org/wiki/Test-driven_development)







