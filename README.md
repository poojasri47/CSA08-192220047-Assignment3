Directory Structure
Q1/ – Q7/: Contains the Python source files (.py), input data, and output screenshots for each task.

requirements.txt: Lists the environment dependencies (standard library only).

README.md: Documentation, run commands, and summary of results.

Tasks Covered
Q1: Lists and Slicing: Daily Rainfall Records (Q1/q1_rainfall.py)

Q2: Tuples, Mutability and Copying: City Bus-Stop Map (Q2/q2_tuples_copying.py)

Q3: Dictionaries: Farmer Helpline Complaint Analysis (Q3/q3_complaints.py)

Q4: Sets: Elective Registration Clash Detection (Q4/q4_electives.py)

Q5: List Comprehension: Cleaning Sensor Readings (Q5/q5_sensor_cleaning.py)

Q6: Nested Data: A Railway Timetable (Q6/q6_timetable.py)

Q7: Design a Contact-Merging Program from First Principles (Q7/q7_contact_merger.py)

How to Run
Run each file directly via Python to view the operation counts, benchmarks, and outputs:

python Q1/q1_rainfall.py
python Q2/q2_tuples_copying.py
python Q3/q3_complaints.py
python Q4/q4_electives.py
python Q5/q5_sensor_cleaning.py
python Q6/q6_timetable.py
python Q7/q7_contact_merger.py


Summary of Results
Q1: Computed weekly totals via slicing, wettest/driest weeks, dry days, and verified that the O(n) running-sum 7-day moving average (168.57 ms for 365,000 readings) outperforms the O(7n) naive method (578.88 ms).

Q2: Resolved the [[0]*cols]*rows shared-row bug using a list comprehension, demonstrated aliasing vs. shallow/deep copy, verified (lat, lon) tuple keys vs. unhashable lists, and compared list/tuple memory (8,000,056 B vs. 8,000,040 B for 1M items).

Q3: Counted filtered word frequencies with dict.get(), grouped complaints by district/crop with setdefault(), ranked top-k words with tie-breaking, and showed O(n) dict/Counter outperforms O(n⋅d) list.count() up to 100,000 complaints.

Q4: Identified elective clashes (&), single-elective students (^), and unregistered students (-), verified set methods match operators, and measured O(1) set membership (8.13 µs) vs. O(n) list scan (20.95 ms) at 1,000,000 IDs.

Q5: Filtered valid [-50°C, 50°C] readings and converted to °F across loops, comprehensions, and map/filter, flagged 2–8°C alarm minutes via enumerate(), and confirmed generator expressions use 104 B (O(1)) vs. 5,933,720 B (O(n)) for lists.

Q6: Built a nested timetable (dict → list of tuples + set of days), sorted departures with key=lambda, and demonstrated a ~10x speedup using a station index (1,615 µs vs. 15,612 µs for 10,000 trains).

Q7: Normalized phone numbers and names, merged duplicates in O(n) average time using a phone-keyed dictionary with sets for numbers and emails, and deduplicated 100,000 contacts into 30,000 records in ~1.59 
