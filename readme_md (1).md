
## Repository Structure

```
CSA08-<RegisterNumber>-Assignment3/
├── README.md
├── requirements.txt
├── Q1/
│   ├── q1_rainfall.py
│   └── output_q1.png
├── Q2/
│   ├── q2_tuples_copying.py
│   └── output_q2.png
├── Q3/
│   ├── q3_complaints.py
│   └── output_q3.png
├── Q4/
│   ├── q4_electives.py
│   └── output_q4.png
├── Q5/
│   ├── q5_sensor_cleaning.py
│   └── output_q5.png
├── Q6/
│   ├── q6_timetable.py
│   └── output_q6.png
└── Q7/
    ├── q7_contact_merger.py
    └── output_q7.png

```

## How to Run Each Task & Result Summary

| Task | Source File | Command to Run | Summary of Result | 
| ----- | ----- | ----- | ----- | 
| **Q1** | `Q1/q1_rainfall.py` | `python Q1/q1_rainfall.py` | Computes weekly totals via list slicing (`[7:14]`, `[-7:]`, `[::7]`), identifies wettest/driest weeks, max/min rainfall days, dry days (`0 mm`), and verifies that the running-sum 7-day moving average ($O(n)$, \~`168.57 ms` for `365,000` days) outperforms the naive nested sum ($O(7n)$, \~`578.88 ms`). | 
| **Q2** | `Q2/q2_tuples_copying.py` | `python Q2/q2_tuples_copying.py` | Fixes the `[[0]*cols]*rows` shared-reference bug using a list comprehension, verifies `TypeError` when using a list as a dict key vs. valid `(lat, lon)` tuple keys, demonstrates aliasing vs. shallow/deep copy, and compares memory (`8,000,056 B` list vs. `8,000,040 B` tuple for `1,000,000` items). | 
| **Q3** | `Q3/q3_complaints.py` | `python Q3/q3_complaints.py` | Counts complaint word frequencies with `dict.get()` while filtering stop words, groups records by district and crop with `setdefault()`, ranks top-$k$ words with tie-breaking, and shows `dict` (`220.63 ms`) / `Counter` (`57.16 ms`) scale linearly ($O(n)$) up to `100,000` complaints compared to $O(n \cdot d)$ `list.count()`. | 
| **Q4** | `Q4/q4_electives.py` | `python Q4/q4_electives.py` | Uses set operators (`&`, `^`, `-`, \` | 
| **Q5** | `Q5/q5_sensor_cleaning.py` | `python Q5/q5_sensor_cleaning.py` | Filters out sensor errors outside `[-50°C, 50°C]`, converts valid readings to Fahrenheit across loop, list comprehension, and `map`/`filter`, records out-of-range (`2–8°C`) alarm minutes via `enumerate()`, and shows generator expressions use `104 B` ($O(1)$) vs. `5,933,720 B` ($O(n)$) for a list comprehension. | 
| **Q6** | `Q6/q6_timetable.py` | `python Q6/q6_timetable.py` | Models a nested railway timetable (`dict` $\rightarrow$ `list` of `tuple`s + `set` of days), filters stops by station and day, sorts departures via `key=lambda`, and confirms station indexing cuts query time by \~`10x` (`1,615 us` vs. `15,612 us` for `10,000` trains). | 
| **Q7** | `Q7/q7_contact_merger.py` | `python Q7/q7_contact_merger.py` | Normalizes phone numbers (`+91`/leading `0`/spaces) and names, deduplicates contacts in $O(n)$ average time using a phone-keyed dictionary with `set`s for numbers and emails, merging `100,000` contacts into `30,000` unique records in `~1.59 s`. | 
