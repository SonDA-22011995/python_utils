- [Format datetime to string](#format-datetime-to-string)
- [index of the day of the week from a date in Python](#index-of-the-day-of-the-week-from-a-date-in-python)
- [Add days to a date in Python](#add-days-to-a-date-in-python)

## Format datetime to string

```
from datetime import datetime

# Get the current date and time
now = datetime.now()

# Example 1: YYYY-MM-DD HH:MM:SS format
formatted_date_time = now.strftime("%Y-%m-%d %H:%M:%S")
print(f"Current date and time: {formatted_date_time}")

# Example 2: Month Day, Year (e.g., November 27, 2025)
formatted_date = now.strftime("%B %d, %Y")
print(f"Formatted date: {formatted_date}")

# Example 3: Abbreviated weekday and 12-hour time with AM/PM
formatted_time = now.strftime("%a %I:%M %p")
print(f"Formatted time: {formatted_time}")
```

**Common strftime() format codes:**

- %Y: Year with century (e.g., 2025)
- %m: Month as a zero-padded decimal number (01-12)
- %d: Day of the month as a zero-padded decimal number (01-31)
- %H: Hour (24-hour clock) as a zero-padded decimal number (00-23)
- %M: Minute as a zero-padded decimal number (00-59)
- %S: Second as a zero-padded decimal number (00-59)
- %B: Full month name (e.g., November)
- %a: Abbreviated weekday name (e.g., Thu)
- %A: Full weekday name (e.g., Thursday)
- %I: Hour (12-hour clock) as a zero-padded decimal number (01-12)
- %p: Locale's equivalent of AM or PM
- %j: Day of the year as a zero-padded decimal number (001-366)

## index of the day of the week from a date in Python

```
from datetime import date

# Create a date object
my_date = date(2025, 11, 27)

# Get the index of the day of the week
# Monday is 0, Tuesday is 1, ..., Sunday is 6
day_index = my_date.weekday()

print(f"The date is: {my_date}")
print(f"The index of the day of the week is: {day_index}")
```

## Add days to a date in Python

```
from datetime import datetime, timedelta

# Define a starting date
original_date = datetime(2023, 1, 15)
print(f"Original date: {original_date}")

# Add a specific number of days
days_to_add = 7
new_date = original_date + timedelta(days=days_to_add)
print(f"Date after adding {days_to_add} days: {new_date}")

# Example with a different number of days
another_date = datetime(2024, 10, 26, 10, 30, 0)
print(f"Another original date: {another_date}")

more_days = 30
future_date = another_date + timedelta(days=more_days)
print(f"Date after adding {more_days} days: {future_date}")
```
