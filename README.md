# Task 25: Basic Data Validation (Excel / Google Sheets)

**Internship:** Veda Technology, Data Analytics Track (Level 1, Day 25)
**Intern:** Rathod Harshvardhansinh J

## Objective
Improve spreadsheet data quality by building a data-entry sheet that uses dropdowns and validation rules, so invalid values cannot be entered.

## Tools Used
- Microsoft Excel
- Google Sheets (the same file can be imported)

## Deliverables
| File | Description |
|------|-------------|
| `Data_Validation_Template.xlsx` | Validated template with 10 sample entries |

The workbook has three sheets:
1. **Data Entry** - the main sheet with validation rules and clear column labels (rows 2-500 are protected by rules).
2. **Lists** - source values for all dropdown menus.
3. **Instructions** - summary of every rule.

## Dataset
Synthetic employee data (no real personal information).

## Validation Rules
| Column | Rule | Type |
|--------|------|------|
| Employee ID | `EMP` + 3 digits, must be unique | Custom formula |
| Full Name | 3-50 characters | Text length |
| Department | HR, Finance, IT, Sales, Marketing, Operations | Dropdown |
| Job Title | 2-40 characters | Text length |
| Employment Type | Full-time, Part-time, Contract, Intern | Dropdown |
| Location | Ahmedabad, Mumbai, Bengaluru, Delhi, Pune | Dropdown |
| Joining Date | 01-Jan-2000 to today (no future dates) | Date |
| Salary (INR / month) | Whole number, 10,000 - 500,000 | Whole number |
| Email | Must contain `@` and a dot, no spaces | Custom formula |
| Performance Rating | Whole number 1-5 | Whole number |
| Status | Active, On Leave, Resigned | Dropdown |

Every rule shows an **input prompt** when the cell is selected and a **stop alert** with a clear message when an invalid value is typed.

## Approach
1. Designed a clear column structure with descriptive headers.
2. Stored dropdown options on a separate `Lists` sheet so they are easy to maintain.
3. Applied Data Validation (Data > Data Validation) to each column with input and error messages.
4. Added synthetic sample entries covering all dropdown values.
5. Froze the header row and added filters for easy use.

## Outcome
Invalid entries (wrong ID format, duplicate IDs, future dates, out-of-range salary, malformed emails, ratings outside 1-5, or values outside the dropdowns) are rejected at entry time, which improves data consistency and quality.

## How to Use
1. Open `Data_Validation_Template.xlsx` in Excel (or import it into Google Sheets).
2. Go to the **Data Entry** sheet and add rows below the samples.
3. Use the dropdowns and follow the prompts. Invalid input will be blocked.

## Interview Questions
**Why use data validation?**
It enforces consistent, correct data at the point of entry, reducing cleaning effort later and preventing errors in analysis and reports.

**What problems can dropdowns prevent?**
Typos, inconsistent spellings (e.g. "HR" vs "H.R."), invalid categories, and duplicate variants of the same value that break filters, pivots and counts.

## Author
Rathod Harshvardhansinh J
