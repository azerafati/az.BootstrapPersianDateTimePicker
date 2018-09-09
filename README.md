# MD.BootstrapPersianDateTimePicker
#### Bootstrap 4+ Persian And Gregorian Date Time Picker jQuery 3+ Plugin

![MD.BootstrapPersianDateTimePicker](https://raw.githubusercontent.com/Mds92/MD.BootstrapPersianDateTimePicker/Bootstrap4/src/MdPersianDateTimePicker.jpg)

`MD.BootstrapPersianDateTimePicker` uses bootstrap [Popovers](https://getbootstrap.com/docs/4.1/components/popovers/), so it has flexibility of bootstrap's popover.
<hr>

### Installing:
First you have to install `Bootstrap 4+` and `jQuery 3+` and link them to your html file.
Then you can install latest version of the plugin via npm or nuget:

***Install-Package MD.BootstrapPersianDateTimePicker***

***npm install md.bootstrappersiandatetimepicker@latest***

Now add these files to you html:
```html
<link href="/Content/MdBootstrapPersianDateTimePicker/jquery.Bootstrap-PersianDateTimePicker.css" rel="stylesheet"/>
<script src="/Scripts/MdBootstrapPersianDateTimePicker/jquery.Bootstrap-PersianDateTimePicker"></script>
```
I suggest to add scripts at the end of  `body`  tag and after  `jQuery`  library.
### How to use:
```javascript
$('#id').MdPersianDateTimePicker({ targetSelector: '#inputDate2' });
```

<hr>

### Options:
Default values are into `[ ]`

Name | Values | Description | Sample
------------- | ------------- | ------------- |-------------
**englishNumber** | [false], true | Switch between English number or Persian number 
**placement** | top, right, [bottom], left | Position of date time picker 
**trigger** | [click], mousedown, focus, ... | Event to show date time picker 
**enableTimePicker** | [false], true | Time picker visibility 
**targetSelector** | String | CSS selector to show selected date into it | '#YousElementId'
**toDate** | [false], true | When you want to set date picker as `toDate` to enable date range selecting 
**fromDate** | [false], true | When you want to set date picker as `fromDate` to enable date range selecting
**groupId** | String | When you want to use `toDate`, `fromDate` you have to enter a group id to specify date time pickers| 'dateRangeSelector1'
**disabled** | [false], true | Disable date time picker 
**format** | String | date selecting string format | 'yyyy/MM/dd HH:mm:ss'
**isGregorian** | [false], true | Is calendar Gregorian 
**inLine** | [false], true | Is date time picker in line 
**selectedDate** | [undefined], new Date() | Selected date as JavaScript Date object 
**monthsToShow** | Numeric array with 2 items, [0 ,0] | To show, number of month before and after selected date in date time picker, first item is for before month, second item is for after month | [1, 1]
**yearOffset** | Number | Number of years to select in year selector | 30
**holiDays** | Array: Date[] | Array of holidays to show in date time picker as holiday | [new Date(), new Date(2017, 3, 2)]
**disabledDates** | Array: Date[] | Array of disabled dates to prevent user to select them | [new Date(2017, 1, 1), new Date(2017, 1, 2)] 
**disableBeforeToday** | [false], true | Disable days before today 
**disableAfterToday** | [false], true | Disable days after today 
**disableBeforeDate** | Date | Disable days before this Date | new Date(2018, 11, 12) 
**disableAfterDate** | Date | Disable days after this Date | new Date(2018, 12, 11) 

<hr>

### String format:

Format | English Description | Persian Description 
------------- | ------------- | -------------
**yyyy** | Year, 4 digits | سال چهار رقمی
**yy** | Year, 2 digits | سال دو رقمی
**MMMM** | Month name | نام ماه
**MM** | Month, 2 digits | عدد دو رقمی ماه
**M** | Month, 1 digit | عدد تک رقمی ماه
**dddd** | Week day name | نام روز هفته
**dd** | Month's day, 2 digits | عدد دو رقمی روز 
**d** | Month's day, 1 digit | عدد تک رقمی روز 
**HH** | Hour, 2 digits - 0 - 24 | عدد دو رقمی ساعت با فرمت 0 تا 24
**H** | Hour, 1 digit - 0 - 24 | عدد تک رقمی ساعت با فرمت 0 تا 24
**hh** | Hour, 2 digits - 0 - 12 | عدد دو رقمی ساعت با فرمت 0 تا 12
**h** | Hour, 1 digit - 0 - 12 | عدد تک رقمی ساعت با فرمت 0 تا 12
**mm** | Minute, 2 digits | عدد دو رقمی دقیقه
**m** | Minute, 1 digit | عدد تک رقمی دقیقه
**ss** | Second, 2 digits | ثانیه دو رقمی
**s** | Second, 1 digit | ثانیه تک رقمی
**tt** | AM / PM | ب.ظ یا ق.ظ
**t** |  | حرف اول از ب.ظ یا ق.ظ

<hr>

### Functions:

Name | Return | Description | Sample
------------- | ------------- | ------------- |-------------
**getText** | string | Get selected date text | $('#id').MdPersianDateTimePicker('getText');
**getDate** | Date | Get selected date | $('#id').MdPersianDateTimePicker('getDate');
**getDateRange** | [fromDate, toDate]: Date[] | Get selected date range | $('#id').MdPersianDateTimePicker('getDateRange');
**setDate** | void | Set selected datetime with Date object argument | $('#id').MdPersianDateTimePicker('setDate', new Date(2018, 11, 12));
**setDatePersian** | void | Set selected datetime with persian json argument | $('#id').MdPersianDateTimePicker('setDatePersian', {year: 1397, month: 1, day: 1, hour: 0, minute: 0, second: 0});
**hide** | void | Hide date time picker | $('#id').MdPersianDateTimePicker('hide');
**show** | void | Show date time picker | $('#id').MdPersianDateTimePicker('show');
**disable** | void | Disable or enable date time picker | $('#id').MdPersianDateTimePicker('disable', /*isDisable*/ true);
**changeType** | void | Switch between Persian or Gregorian calendar | $('#id').MdPersianDateTimePicker('changeType', /*isGregorian*/ true, /* englishNumber */ true);