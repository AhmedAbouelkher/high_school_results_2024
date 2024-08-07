# High School Results 2024

للغة العربية، انظر [هنا](./README_AR.md).

> Before going any further, please read the [disclaimer](#disclaimer) at the end of this document.

This is a dataset of Egyptian high school results for the year 2024. The dataset contains the following columns:

- `seat_number` int4
- `name` text
- `marks` float8
- `student_case` int4
- `student_case_desc` text
- `c_flag` int4
- `marks_percentage` float8 _(available only for `results` table)_

The dataset is available in the following formats:

- [Results in CSV format](./high_school_results_2024.csv.zip).
- [Results in SQL dump](./high_school_results_2024.sql.gz) _PostgreSQL_.
    > SQL dump can be imported using `pg_restore -v -d <database_url> high_school_results_2024.sql.gz`

Example Usage:

```sql
SELECT * FROM results WHERE marks > 90;

SELECT * FROM results ORDER BY marks DESC LIMIT 100;

SELECT * FROM results WHERE student_case=1;

SELECT student_case, COUNT(*) FROM results GROUP BY student_case;
```

## Note

These results do not include the full results for each subject. Instead, they include the total results for each student. The total results are calculated based on the student's performance in all subjects.

To access each student's high school results for 2024 in individual subjects, you will need to refer to the original mark sheets or contact the relevant authorities.
Students results are also available in multiple Egyptian websites: [youm7](https://natega.youm7.com/), and [elwatannews](https://natega.elwatannews.com/).


---

## Disclaimer

This repository contains the Egyptian high school results for the year 2024. The source of this data is not known, and its legality cannot be confirmed. This repository is intended solely for educational purposes.

Important Points:

1. **Data Source:** The origin of the data included in this repository is unknown, and it may not be legally obtained or distributed.
2. **Educational Use Only:** The content of this repository is intended for educational and informational purposes only. It is not intended for any commercial use or distribution.
3. **No Warranty:** The data provided in this repository is offered "as is" without any guarantees or warranties, express or implied. I do not guarantee the accuracy, completeness, or reliability of the data.
4. **No Liability:** I am not responsible for any damages, losses, or legal consequences that may arise from the use or misuse of the data contained in this repository. By using this repository, you agree to hold me harmless from any liability or claims.

User Responsibility:

- **Compliance with Laws:** Users are responsible for ensuring that their use of the data complies with all applicable local, national, and international laws and regulations.
- **Ethical Use:** Users should use the data ethically and responsibly, keeping in mind the potential impact on individuals whose information may be included.

If you do not agree with these terms, you are advised not to use or distribute the data contained in this repository.
