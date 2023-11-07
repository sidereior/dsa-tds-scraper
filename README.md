# dsa-tds-scraper
## Features
- **Multiple Divisions**
- **Batch and Unbatched Processing**
- **Logging**
- **Customizable Output**
## Requirements
- Python 3.x
- Pandas
- lxml
- argparse

## Installation
1. Ensure that Python 3.x is installed on your system and copy repo.
2. Install the required packages (see each package's webpage for other details or run pip install package_name )

## Usage
Navigate to the project directory in your terminal or command prompt, and run the script using the following command format:

``` python processing.py <division> <batched> ```
- <division>: The soccer division you want to process. Choose from:
    - d1: Division 1
    - d2: Division 2
    - d3: Division 3
    - naia: NAIA
    - njcaa: NJCAA
    - all: All divisions

<batched>:
True: Output in batched format (separate files for each week and division).
False: All data consolidated in a single file.

## Examples
Process all weeks and divisions, and save in batched format:

``` python processing.py all True ```

Process all weeks of division d1, and save in a single file:

```python processing.py d1 False ```

## Output
The processed data is saved in the outputs directory. The naming convention of the output files depends on your specified options:

Batched: <division>_week<week_number>_data_batch_<batch_id>.csv
Unbatched: <division>_unbatched_<batch_id>.csv for specific divisions or all_unbatched_<batch_id>.csv for all divisions.
Each CSV file contains the following columns:

Home Team
Away Team
Home Goals
Away Goals
Home Team Conference
Away Team Conference
Week
Division