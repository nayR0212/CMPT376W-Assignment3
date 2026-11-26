# LogLens - find all your log problems fast

LogLens is a simple command-line Python script for counting number of records by log level, in a CSV log file. It is aimed for people familiar with CSV files and the terminal.

## Requirements
 - `Python 3.10` or later

## Get started

First, get the project files from GitHub with `git clone https://github.com/nayR0212/CMPT376W-Assignment3.git`

Refer to [INSTALL.md](docs/INSTALL.md) for more detailed installation instructions

## Using the program

Run the following command after you have found the correct folder:

`loglens --input mylog.csv --severity error`

The software scans your log, fixes mistakes, and shows you what went wrong. You will see a number once it is finished. You can also run it on real production files without worrying about any side effects.

## Input format

The input should be a CSV file. Log files tend to have fields describing the time and what happened, but LogLens is flexible and will work with whatever columns your monitoring system uses. A small example is included somewhere in this repository.

## Questions

If something doesn't work, you can create a GitHub issues or contact the developers directly. Please include a description of the problem and do not give private or sensitive log data.
