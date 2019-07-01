# timesheet for date

fork from GitHub repo [timesheet.js](https://github.com/sbstjn/timesheet.js)

## codeing cause

The repo [timesheet.js](https://github.com/sbstjn/timesheet.js)'s time is just support until a month. Therefore I satisfy the demand to modify some original js code.

## how to use

Reference original code

You have to include `/dist/timesheet.min.js` and `./dist/timesheet.min.css` in your HTML and initialize it.

```
<div id="timesheet-default"></div>
```

```
new Timesheet("timesheet-default", 2014, 2025, [
        ["2014/5/12", "2014/09/14", "date to date", "lorem"],
        ["2014/02/03", "2018", "date to year", "lorem"],
        ["2014/06/15", "2018/09", "date to month", "ipsum"],
        ["2018/01", "2019", "month to year", "lorem"],
        ["2018/10", "2019/01", "month to month", "dolor"],
        ["2014/12", "2018/05/16", "month to date", "lorem"],
        ["2016", "2018", "year to year", "dolor"],
        ["2016", "2018/05", "year to month", "ipsum"],
        ["2018", "2020/09/2", "year to date", "dolor"],
        ["2014/09", "without end date(until now)", "default"]
      ]);
```

Your HTML file probable like it

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>timesheet for date</title>
    <link rel="stylesheet" href="./dist/timesheet.min.css" />
    <script type="text/javascript" src="./dist/timesheet.min.js"></script>
  </head>
  <body>
    <div id="timesheet-default"></div>


    <script>
      new Timesheet("timesheet-default", 2014, 2025, [
        ["2014/5/12", "2014/09/14", "date to date", "lorem"],
        ["2014/02/03", "2018", "date to year", "lorem"],
        ["2014/06/15", "2018/09", "date to month", "ipsum"],
        ["2018/01", "2019", "month to year", "lorem"],
        ["2018/10", "2019/01", "month to month", "dolor"],
        ["2014/12", "2018/05/16", "month to date", "lorem"],
        ["2016", "2018", "year to year", "dolor"],
        ["2016", "2018/05", "year to month", "ipsum"],
        ["2018", "2020/09/2", "year to date", "dolor"],
        ["2014/09", "without end date(until now)", "default"]
      ]);
    </script>
  </body>
</html>
```

![timesheetForDate](https://github.com/HiDana/timesheet_fordate.js/blob/master/example/images/timesheetForDate.png)

## Object Timesheet

```
new Timesheet(html's id(string), start year(number) , end year(number), [
        [start date((string)), end date((string)), info(string), category like "lorem"、"ipsum"、"dolor" and "default"(string)]
      ]);
```

your timesheet object probable like this

```
new Timesheet("timesheet-default", 2014, 2025, [
        ["2014/5/12", "2014/09/14", "date to date", "lorem"],
        ["2014/02/03", "2018", "date to year", "lorem"],
        ["2014/06/15", "2018/09", "date to month", "ipsum"],
        ["2018/01", "2019", "month to year", "lorem"],
        ["2018/10", "2019/01", "month to month", "dolor"],
        ["2014/12", "2018/05/16", "month to date", "lorem"],
        ["2016", "2018", "year to year", "dolor"],
        ["2016", "2018/05", "year to month", "ipsum"],
        ["2018", "2020/09/2", "year to date", "dolor"],
        ["2014/09", "without end date(until now)", "default"]
      ]);
```

in timeSheet with have many types to display

### note

If your date without day number it will start the first day of this month or this year. But don't worry the info of date will display with your original date

example:

if your date is start or end "2019/02" .The line will display "2019/02/01"

![date only with year and month](https://github.com/HiDana/timesheet_fordate.js/blob/master/example/images/untilMonth.png)

if your date is start or end "2019" .The line will display "2019/01/01"

![date only with](https://github.com/HiDana/timesheet_fordate.js/blob/master/example/images/untilYear.png)

### date to date

```
["2014/5/12", "2014/09/14", "date to date", "lorem"]
```

### date to year

```
["2014/02/03", "2018", "date to year", "lorem"]
```

### date to month

```
["2014/06/15", "2018/09", "date to month", "ipsum"]
```

### month to year

```
["2018/01", "2019", "month to year", "lorem"]
```

### month to month

```
["2018/10", "2019/01", "month to month", "dolor"]
```

### month to date

```
["2014/12", "2018/05/16", "month to date", "lorem"]
```

### year to year

```
["2016", "2018", "year to year", "dolor"]
```

### year to month

```
["2016", "2018/05", "year to month", "ipsum"]
```

### year to date

```
["2018", "2020/09/2", "year to date", "dolor"]
```

### without end

```
["2014/09", "without end date(until now)", "default"]
```

## postscript

Because the width of the month is very small. You would be not to see the obvious difference between month and date.

## todo in the future

- Support auto update category and different color

  We only have four categories "lorem"、"ipsum"、"dolor" and "default" in the original code.

- Auto-extend width and scroll overflow

  If your distance of year is too long. It maybe will overflow the initial width.

# License

Timesheet_fordate.js is licensed under MIT License.
