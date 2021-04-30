# log4netAppInsights

this is a sample ASP.NET core app showing how to send data to App Insights and leveraging Log4net

Not much was required as it leveraged the nuget package https://www.nuget.org/packages/Microsoft.Extensions.Logging.Log4Net.AspNetCore/. This configures log4net as a logging handler.

the log4net associated code and config was taken from https://github.com/huorswords/Microsoft.Extensions.Logging.Log4Net.AspNetCore/blob/develop/doc/CONFIG.md

to get the additional information sent (besides errors) the following json was added to appsettings.json

```json
"ApplicationInsights": {
      "LogLevel": {
        "Default": "Information"
      }
 ```     
      
The full appsettings.json

```json
{
  "Logging": {
    "LogLevel": {
      "Default": "Trace",
      "Microsoft": "Trace",
      "Microsoft.Hosting.Lifetime": "Trace"
    },
    "ApplicationInsights": {
      "LogLevel": {
        "Default": "Information"
      }
    }
    },
    "AllowedHosts": "*",
    "ApplicationInsights": {
      "ConnectionString": "InstrumentationKey=YOURAPPINSIGHTSKEY"
    }
  }
```
