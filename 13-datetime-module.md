# Working with datetime in Python

The `datetime` module is used to work with dates and time in Python.

It is widely used in:

- applications (forms, logs)
- backend systems
- data analysis
- scheduling tasks

---

# Importing datetime

```python
from datetime import datetime, date, time, timedelta
```

---

# Current Date and Time

```python
print(date.today())
print(datetime.now())
```

### Note

- `date.today()` → current date  
- `datetime.now()` → current date + time  

---

# Creating Date and Time Manually

```python
print(date(2026, 4, 2))
print(time(14, 30, 0))
print(datetime(2026, 4, 2, 14, 30))
```

---

# Accessing Parts

```python
now = datetime.now()

print(now.year)
print(now.month)
print(now.day)
print(now.hour)
print(now.minute)
print(now.second)
```

### Note

Useful in:

- age calculation  
- time-based filtering  

---

# Date and Time Format

Python uses:

```text
Date → YYYY-MM-DD
Time → HH:MM:SS
```

---

# Time Arithmetic (timedelta)

```python
now = datetime.now()

print(now + timedelta(hours=5))
```

### Note

Used in:

- adding deadlines  
- scheduling events  

---

# Real-World Example

Example: Netflix analysis

- track login time  
- track movie start time  
- calculate time difference  

---

# Formatting Date (strftime)

```python
now = datetime.now()

print(now.strftime("%Y-%m-%d"))
print(now.strftime("%d/%m/%Y"))
print(now.strftime("%A"))
print(now.strftime("%B"))
print(now.strftime("%H:%M:%S"))
```

### Note

Used in:

- databases  
- reports  
- UI display  

---

# String to Date (strptime)

```python
date_str = "02-04-2026"

date_obj = datetime.strptime(date_str, "%d-%m-%Y")
print(date_obj)
```

### Note

- `strptime()` → string → datetime  
- `strftime()` → datetime → string  

---

# Time Difference

```python
today = date.today()

future = today + timedelta(days=10)
past = today - timedelta(days=5)

print(future)
print(past)
```

---

# Difference Between Dates

```python
date1 = date(2026, 4, 10)
date2 = date(2026, 4, 2)

diff = date1 - date2
print(diff.days)
```

---

# Timestamp

```python
now = datetime.now()

print(now.timestamp())

dt = datetime.fromtimestamp(1710000000)
print(dt)
```

### Note

Used in:

- APIs  
- backend systems  

---

# Replace Values

```python
now = datetime.now()

new_date = now.replace(year=2030)
print(new_date)
```

---

# Mini Project: Reminder System

```python
from datetime import datetime, timedelta, timezone
import time

reminder_text = input("Enter reminder message: ")
reminder_time_str = input("Enter UTC time (HH:MM:SS): ")

try:
    now_utc = datetime.now(timezone.utc)

    target_time = datetime.strptime(reminder_time_str, "%H:%M:%S")

    reminder_datetime = now_utc.replace(
        hour=target_time.hour,
        minute=target_time.minute,
        second=target_time.second,
        microsecond=0,
        tzinfo=timezone.utc
    )

    if reminder_datetime < now_utc:
        reminder_datetime += timedelta(days=1)

    print(f"Reminder set for: {reminder_datetime}")

    while True:
        if datetime.now(timezone.utc) >= reminder_datetime:
            print(f"Reminder: {reminder_text}")
            break

        time.sleep(1)

except ValueError:
    print("Invalid time format")
```

---

# Summary

- `datetime` handles date and time operations  
- `timedelta` helps with time calculations  
- `strftime` and `strptime` handle formatting  
- used in real-world applications like scheduling, logging, analytics
- https://drive.google.com/file/d/11mjEQ9k-gZ9lO7CifOK-FiJWRTjwjh6-/view?usp=sharing
