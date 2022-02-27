# UiPath_FindWeekendsOfCurrYear_27Feb2022_2234

UiPath Find weekend dates for current year

https://forum.uipath.com/t/how-to-get-saturdays-and-sundays-of-whole-year/402903/2

```
Enumerable.Range(0, (DateVar.AddYears(1) - DateVar).Days).Where(Function(day) {6,0}.Contains(DateVar.AddDays(day).DayOfWeek)).Select(Function(day) DateVar.AddDays(day)).ToList
```
