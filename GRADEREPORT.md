# Grading Report

**Final Grade: 9.5/10.00**

## Rubric

| Criterion | Points |
|-----------|--------|
| `extract_data` correctly slices, title-cases names, int conversion, extracts grades, and leaves input untouched | **3** |
| `curve_grades` applies the curve (while loop) and caps values at 100 | **2.5** |
| `print_top_performers` prints only qualifying `Name: Score` lines (>= 95) | **3** |
| Code quality (required loop choices, clear logic) | **1** |

## General Comments

extract_data and print_top_performers look correct, but curve_grades fails because it never assigns the incremented value back to each list element and uses an invalid clamp check. Update each grades[i] inside the while loop and then cap that element at 100 before advancing the index.

## Functionality

- tests/test_grader.py::RosterHelperTests::test_curve_grades_values_and_clamping: Failed (0.0 points)
   Error:         TypeError: '>' not supported between instances of 'list' and 'int'

- tests/test_grader.py::RosterHelperTests::test_extract_data_parses_names_and_grades_title_case: Passed (10.0 points)

- tests/test_grader.py::RosterHelperTests::test_extract_data_returns_new_lists: Passed (10.0 points)

- tests/test_grader.py::RosterHelperTests::test_print_top_performers_prints_name_and_score_for_ge_95: Passed (10.0 points)



