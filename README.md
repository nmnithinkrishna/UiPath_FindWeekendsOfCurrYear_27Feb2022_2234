# UiPath_FindWeekendsOfCurrYear_27Feb2022_2234

UiPath Find weekend dates for current year

https://forum.uipath.com/t/how-to-get-saturdays-and-sundays-of-whole-year/402903/2

```
Enumerable.Range(0, (DateVar.AddYears(1) - DateVar).Days) //Creating a day collection eq to the number of days in Curr yr

.Where(Function(day) {6,0}.Contains(DateVar.AddDays(day).DayOfWeek)) //Check and filter if the day is weekend

.Select(Function(day) DateVar.AddDays(day)).ToList //Format and output the dates in a list
```

Day of week Enum Reference [^1]

[^1]: https://docs.microsoft.com/en-us/dotnet/api/system.dayofweek?view=net-6.0 
