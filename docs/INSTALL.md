# Installation and Tutorial

The tutorial runs the script using `python`. Other operating systems may use `python3` or `py`. Please check the Python launcher installed on your system before running any command. 

## Requirements

* Python `3.10` or newer

Pip or other third-party dependencies are not required.

## Installation

Download the repository as a ZIP file and extract.

## Usage

Open the command-line in the repository root, the same location as `LogLens.py`. Run using `python`, `python3`, or `py` depending on your operating system.

The `--file` argument is required and expects a path to a CSV log file. Ensure that CSV column headers are named exacly as `timestamp`, `level`, and `message` or the script will fail.

The `--level` argument is optional and counts every record if omitted. Accepted log levels are `INFO`, `WARN`, and `ERROR`.

Sample input with `--level` argument:
```bash
python loglens.py --file data/sample_logs.csv --level ERROR
```
Expected output:
```bash
Records matching ERROR: 2
```

Sample input without `--level` argument:
```bash
python loglens.py --file data/sample_logs.csv
```
Expected output:
```bash
Records matching ALL: 6
```

To view all valid command-line options, run:
```bash
python loglens.py --help
```

## Problems and fixes

* `CSV must contain timestamp, level, and message columns`: Ensure that column headers are named exactly `timestamp`, `level`, and `message`.
* `File not found`: Ensure that the file path name is correct or that the file exists before trying again.
* `Cannot read file`: Ensure the file has sufficient access permissions before trying again. 

For further support, open a [public issue on GitHub](https://github.com/FraserWPKent/Cmpt-376W-Assignment3-Group-1/issues) with a description of the problem and steps to reproduce it. Do **not** attach private or sensitive log data with your report. If CSV log data is needed, post a sanitized, minimal example.
