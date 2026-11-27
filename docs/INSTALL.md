# How to clone LogLens and use it

These are the instructions on how to clone and use LogLens.

## Things you need

* Python 3.10 or later

* A CSV log file with column headers named exactly `timestamp`, `level`, and `message`.

## Getting the program

Clone the LogLens repository to get the required project files with 

```bash
git clone https://github.com/nayR0212/CMPT376W-Assignment3.git
```

Ensure you are in the repository root with

```bash
cd CMPT376W-Assignment3
```

## Important information before using LogLens

* The `--file` argument is required.
* The `--level` argument is optional, and it counts all records when omitted.
* Accepted log levels are `INFO`, `WARN`, and `ERROR` (uppercase).
* The commands in examples use `python`; on some computers, the Python launcher is `python3` or `py` instead.
* The example data is in `data/sample_logs.csv`.

## Running LogLens

To run the sample, ensure you are in the repository root and enter:

```bash
python loglens.py --file data/sample_logs.csv --level ERROR
```

Expected result:

```text
Records matching ERROR: 2
```

Omitted optional level:

```bash
python loglens.py --file data/sample_logs.csv
```

Expected result:

```text
Records matching ALL: 6
```

For more options:

```bash
python loglens.py --help
```

For your own files, an example can be:

```bash
python loglens.py --file /Users/alex/Desktop/system-log.csv --level ERROR
```

## Problems and fixes

Some common problems and their fixes:
* "File not found" or "Cannot read file" error: ensure you are in the repository root and the path to your CSV is correct.
* An error about the CSV itself: please ensure the column headers match required input format.

If you still run into errors, please contact the developers or open a GitHub issue and provide a description of the problem and a sanitized, minimal example. Do not upload private or sensitive log data publicly.
