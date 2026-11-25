# LogLens - find all your log problems fast

LogLens is a tool which counts records stored in CSV log files. 

It is intended to be used by those who are already decently profficient in the use of CSV files and terminal based app development.

## Requirements

LogLense requires Python version `3.10` or newer.

It also requires basic knowledge of CSV logging and a working knowledge of terminal based application usage.

## Installation
To install, clone this repository or download its files onto your machine.

Once downloaded and extracted, move the repository into your desired location.

## Input format
The given log file must be a **CSV** file type. 

The given log file must contain three columns: `timestamp`, `level`, and `message`.
-  `timestamp`: Stores the time the record described in the log.
-  `level`: Stores the log level of the record.
-  `message`: Stores a description of the record.

Ensure you note down the path between the root of the LogLens repository and the files you want to analyze as it will be required when running the tool.

## Using the program

Once installed please open your terminal and navigate to the root of the LogLens repository.
  - You should be on the same level as the loglens.py file

**Note**: Depending on your python installation instances of `python` may need to be replaced with `python3`, or `py`

From the repository root LogLens can be run with the command: 
  - `python loglens.py --file (log file path) --level (log level)`
      - Replace `(log file path)` with the relative path from the LogLens repository root to your target log file
          - The `--file` option and `(log file path)` are required.
      - Replace `(log level)` with either `INFO`, `WARN`, or `ERROR`
          - If you want to count all records omit `--level` and `(log level)`

A full list of command line arguments can be found by running: 
  - `python loglens.py --help`

## Questions

If you encounter an error when attempting to run the loglens tool please execute `python loglense.py --help` and check that all your arguments are correct.

If you are experiencing a different issue or that previous step failed to fix your issue please see the [INSTALL](docs/INSTALL.md) file to ensure your installation was correct.

If you are still unable to fix the issue please create a issue on the original [LogLens repository](https://github.com/FraserWPKent/Cmpt-376W-Assignment3-Group-1/tree/main) so that a member of the team can help you directly. 
  - When creating your GitHub issue please sanitize or remove any any sensitive log data. GitHub issues are public and can be seen by anyone 
