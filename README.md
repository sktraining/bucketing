# Bucketing
Application to perform bucketing on date ranges.

### Project Objective
Write a Ruby module that will consume a date range and ouput a collection of buckets. Let's keep it all Ruby for now (instead of Rails), and use Rspec for testing.

### Follow these steps to submit your code:

1. Ask to have a folder created in the repo with your name.
1. [**Clone**](ref-clone) the repository to your computer.
1. Modify the files and [**commit**](ref-commit) changes to complete your solution (_in your folder_).
1. [**Push**](ref-push)/sync the changes up to GitHub.
1. [Create a **pull request**](pull-request) on the original repository to turn in the assignment.

---

### Phase 1 Objective
Given a date range range (start_date, end_date), return an array of hourly buckets.

Assumptions:
  1. Dates will just be properly formatted string. - e.g. '2016-04-18_15:35'
  1. We can ignore timezones for now (or assume UTC).
  1. Start_date is inclusive and end_data is exclusive.
  1. Start_date is rounded down to the beginning of the hour.

#### Examples
('2016-04-18_01:35', '2016-04-18_03:42') --> ['2016-04-18_01', '2016-04-18_02']


---

### Phase 2 Objective
Given a date range range (start_date, end_date), return an array of daily buckets.

Assumptions are the same as stated above, plus:
  1. Start_date is always rounded down to the beginning of the day (e.g. - '2016-04-18_15:35' --> '2016-04-18_00:00').

#### Examples
('2016-04-18_15:35', '2016-04-20_17:42') --> ['2016-04-18', '2016-04-19']

---

### Phase 3 Objective
Given a date range range (start_date, end_date), return an array of  the minimum daily buckets and hourly required to cover the entire range.
Assumptions are the same as stated above.

#### Examples
('2016-04-18_15:35', '2016-04-20_02:42') --> ['2016-04-18', '2016-04-19', '2016-04-20_00', '2016-04-20_01']

---

### Phase 4 Objective
Given a date range range (start_date, end_date), return an array of  the minimum daily buckets and hourly required to cover the entire range.

Assumptions are the same as stated above with one exception:
  1. Start_date is no longer rounded down to the beginning of the day. 
  1. Start_date is again rounded down to the beginning of the hour.

#### Examples
('2016-04-17_22:35', '2016-04-20_02:42') --> ['2016-04-17_22', '2016-04-17_23', '2016-04-18', '2016-04-19', '2016-04-20_00', '2016-04-20_01']
