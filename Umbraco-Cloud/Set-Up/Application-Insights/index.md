# Application insigths on Umbraco cloud

## Installing application insights 
This guide will instruct you how to install Application Insights (AI) for your cloud solution.

### Azure portal
First thing to have in place when installing AI is of course an AI resource on Azure, so go ahead and open your favorite browser and log onto the [Azure Portal](https://portal.azure.com) and spin up a new AI Resource.

After that, you can go ahead and grab your `instrumentation key`, from the AI Resouce overview

![alt text](images/01-Instrumentation-key.png "Instrumentation Key")

### Cloud solution
The next thing we need to look at is how to enable AI for your Umbraco solution.

The easiest way is to open your favorite Visual Studio instance, go to Package Manager Console and go

```Install-Package Microsoft.ApplicationInsights.Web ``` 

This will install application insights and all of its dependencies. It will also create an `ApplicationInsights.config` file.

Go ahead, open this file and paste in your `instrumentation key` found in the previous section.

![alt text](images/02-Insert-Instrumentation-Key.png "Insert Instrumentation Key")

Upload the changes to your solution and that is it!

## Application insights limitations on Umbraco Cloud

Unless you have opt-in for a dedicated Umbraco Cloud server, you are sharing computing power with other Umbraco Cloud users. By default Application Insights is configured to provide information about resources allocated and used by the system, do note however that these can be misrepresentative!


## Microsoft documentation

For further information check out Microsoft's own documentation of [Application Insights](https://docs.microsoft.com/en-us/azure/application-insights/app-insights-overview)