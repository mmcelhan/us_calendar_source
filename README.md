# us__calendar_source
The United States Calendar package contains two modules:

1. federal_holiday: module that has functions for United States Federal Holiday
2. market_open: module that has functions for if the United States Stock Markets are open

## Federal Holiday Functions

### federal_holiday.is_federal_holiday(date)

returns True if day is a federal holiday

### federal_holiday.holiday_name(date)

returns name of holiday given a date, None if there is no holiday

### federal_holiday.is_weekend(date)

returns True if day is on a weekend

### federal_holiday.is_weekday(date)

returns True if day is on a weekday

### federal_holiday.is_working_day(date)

returns True if it's a working day for federal employees

### federal_holiday.is_off_day(date)

returns True if it's an off day for federal employees

## Market Open Functions

### Sunday
marketopen.market_open('2021-11-28')
Returns False

### Monday
marketopen.market_open('2021-11-29)
Returns True

### Thanksgiving 2023
marketopen.market_open('2023-11-23')
Returns True

#### Fourth of July
marketopen.market_open('2021-07-04')
Returns False

## Installing as a package:
pip install git+https://github.com/mmcelhan/federalholiday.git#egg=federalholiday


## Source Code
source code is here:
https://github.com/mmcelhan/federal_holiday_calendar_source

The testing file shows all Federal Holidays through 2030 are correctly applied

## Examples

from uscalendar import federalholiday as fh

fh.is_federal_holiday(‘2030-01-01’) # New Years Day, 2030

Returns True

fh.is_federal_holiday(‘2030-1-1’) # to test date formatting

Returns True

fh.is_federal_holiday(‘2030-1-2’) # not a holiday

Returns False

fh.holiday_name(‘2030-01-01’)

Returns ‘New Years Day’

fh.is_day_off(‘2030-01-01’)

Returns True

fh.is_off_day(‘2030-01-01’)

Returns True
