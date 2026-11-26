# How to install LogLens and use it

These instructions are for everyone. They should work the same way on every machine, so read through them and do what they say.

Edited: These are the instructions on how to install LogLens.

## Things you need

* Python 3.8 or newer, plus pip.
* A network connection so LogLens can upload your files for checking.
* A file containing logs from your computer or a work system.

Edited:
* Python 3.10 or newer

## Input format
The CSVs' column headers must be named `timestamp`, `level`, and `message`.

## Getting the program

Get LogLens from the GitHub website. Look for the green button and download a ZIP. Then extract it. Make sure you are in the right place in the terminal, because you will need that later. Once everything is done, you can install it.

Run this command:

pip install loglens

Then move on to the next step.

Edited:
Clone the LogLens repository to get the required project files with `git clone https://github.com/nayR0212/CMPT376W-Assignment3.git`.

## Running a check

First, take a CSV file from your logging system and put it in the project directory. It needs the columns `date`, `severity`, and `details` or the tool might fail. Running it is easy:

python loglens.py data/sample_logs.csv

For your own files, type `python loglens.py --file /Users/alex/Desktop/system-log.csv --level error`. This will print results when the analysis is over. You can find the example data in the project somewhere.

Edited:
The `--file` argument is required, and `--level` argument is optional, when omitted, it counts all records. Accepted log levels are `INFO`, `WARN`, and `ERROR` (uppercase).
The commands in examples use `python`, some computers use `python3` or `py` instead.

To run the sample, ensure you are in the repository root and enter:
`python loglens.py --file data/sample_logs.csv --level ERROR`

Expected result:
`Records matching ERROR: 2`

Omitted optional level:
`python loglens.py --file data/sample_logs.csv`

Expected result:
`Records matching ALL: 6`

For more options:
`python loglens.py --help`

For your own files, an example can be:
`python loglens.py --file /Users/alex/Desktop/system-log.csv --level ERROR`

## Problems and fixes

If you see a "file not found" error, reinstall Python and try again. If the software complains about the CSV, there might be something wrong with your system. If none of this works, open a public GitHub issue and attach your entire original CSV so the team can investigate. Please do not waste the maintainers' time with problems caused by skipped steps.

Edited:
If you:
* see a "File not found" or "Cannot read file" error, ensure you are in the repository root and the path to your CSV is correct.
* get an error about the CSV itself, please ensure the column headers match required input format.
* still run into errors, please open a GitHub issue and describe the problem you are seeing and provide a minimal example. Do not upload sensitive log data publicly.
