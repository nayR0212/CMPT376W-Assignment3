# LogLens - find all your log problems fast

LogLens is a simple command-line Python script for counting records by log level, in a CSV log file. LogLens only reads the input CSV, it does not repair, rewrite or modify the input CSV. It is aimed for people familiar with CSV files and the terminal.

## Requirements
 - `Python 3.10` or later

## Get started

First, get the project files from GitHub with 
```bash
git clone https://github.com/nayR0212/CMPT376W-Assignment3.git
```

Refer to [INSTALL.md](docs/INSTALL.md) for more detailed installation instructions

## Input format

The input must be a CSV file with the exact column headers `timestamp`, `level` and `message`. 

An example log file can be found at [data/sample_logs.csv](data/sample_logs.csv)

## Using the program

Run the following command from the repository root:

```bash
python loglens.py --file data/sample_logs.csv --level ERROR
```

Expected output:

```bash
Records matching ERROR: 2
```

Change the CSV file with the `--file` flag. 

Count different log levels with the `--level` flag. Accepted levels are `INFO`, `WARN`, and `ERROR`. Omitting the `--level` flag will count all records.

## Questions

If something doesn't work, please create a GitHub issues or contact the developers directly. Include a description of the problem and do not give private or sensitive log data.
