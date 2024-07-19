# CAN Log Parser

This repository contains a Python-based tool to parse DBC formatted CAN log files and plot the signals. It leverages `cantools` for parsing DBC files and `matplotlib` for plotting signals, providing an easy way to visualize CAN signal data.

## Features

- Parse DBC files to extract signal definitions
- Read and parse CAN log files
- Decode signals from CAN messages
- Plot the decoded signals

## Requirements

All required packages are listed in the `requirements.txt` file.

- Python 3.6 or higher
- cantools
- matplotlib

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/kiranj26/CAN-Log-Parser.git
    cd CAN-Log-Parser
    ```

2. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. Place your DBC file and log file in the `data/` directory.

2. Run the main script with the appropriate arguments:

    ```bash
    python src/main.py test SAF_SpeedTest
    ```

    or

    ```bash
    python src/main.py test SAF_SpeedTest 43.2 45.6
    ```

## Repository Structure

- `src/`: Contains the main script and related files.
  - `main.py`: Main script to run the tool.
- `data/`: Directory to place your DBC and log files.
- `requirements.txt`: List of dependencies.

## Script Description

### parse_dbc(file_path)

Parses the DBC file located at `file_path`.

### parse_log(db, log_file_path)

Parses the log file located at `log_file_path` using the parsed DBC data.

### process_message(db, message_lines, parsed_data)

Processes a single CAN message and extracts the signals.

### print_parsed_data(parsed_data)

Prints the parsed CAN data.

### plot_signals(parsed_data, signal_name, start_time, end_time)

Plots the specified CAN signal within the given time range.

## Example

To run the script, navigate to the directory containing `main.py` and execute the following commands:

```bash
python src/main.py test SAF_SpeedTest
OR
python src/main.py test SAF_SpeedTest 43.2 45.6
```

These commands will parse the test.dbc and test_log.txt files located in the data/ directory, process the CAN messages, and generate a plot for the SAF_SpeedTest signal.

## Output Screenshots

# Contact

You can download this README file by copying the content above and saving it as `README.md` in your repository folder. Make sure to replace the placeholder paths for the screenshots with the actual paths once you have the images ready.
