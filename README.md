# LLMDeduplicator

LLM Deduplicator
LLM Deduplicator is a Python application that combines traditional string-based methods with large language model (LLM) analysis to deduplicate records in a CSV file. It leverages the power of fuzzy string matching and the semantic understanding of LLMs to identify and remove duplicate records effectively.

Features
Deduplicates records in a CSV file using traditional string-based methods
Identifies potential complex duplicates using fuzzy string matching
Sends potential complex duplicates to an LLM (Claude) for further analysis
Combines deduplicated data from traditional methods and LLM analysis
Writes the final deduplicated data to a new CSV file
Provides a user-friendly interface for inputting the CSV file path and API key
Prerequisites
Before running the LLM Deduplicator, ensure that you have the following:

Python 3.x installed on your system
Required Python libraries: csv, fuzzywuzzy, and anthropic
An Anthropic API key for using Claude (LLM)
Installation
Clone the repository or download the source code files.
Install the required Python libraries by running the following command:

Copy code
pip install fuzzywuzzy anthropic
Usage
Prepare your CSV file containing the records you want to deduplicate. Ensure that the file has a header row specifying the column names.
Open a terminal or command prompt and navigate to the directory where the LLM Deduplicator files are located.
Run the following command to start the LLM Deduplicator:

Copy code
python llm_deduplicator.py
When prompted, enter the file path of your CSV file.
Enter your Anthropic API key when prompted. This key is required to access Claude (LLM) for advanced deduplication analysis.
The LLM Deduplicator will process the CSV file, perform deduplication using traditional string-based methods, and send potential complex duplicates to Claude for further analysis.
Once the deduplication process is complete, the LLM Deduplicator will generate a new CSV file named deduplicated_data.csv in the same directory. This file will contain the deduplicated records.
The application will display the following information:
Total number of records in the input CSV file
Number of deduplicated records (combining traditional methods and LLM analysis)
Number of duplicate pairs identified by traditional methods
Number of records deduplicated by the LLM
Configuration
The deduplicate_data function has a threshold parameter that determines the minimum similarity ratio required for records to be considered duplicates. You can adjust this threshold according to your needs. The default value is set to 90.
The send_to_llm_for_analysis function has threshold_lower and threshold_upper parameters that define the range of similarity ratios for potential complex duplicates to be sent to the LLM for analysis. You can modify these thresholds based on your requirements. The default values are set to 60 and 85, respectively.
License
This project is licensed under the MIT License.

Acknowledgments
The LLM Deduplicator relies on the following libraries:

fuzzywuzzy - For fuzzy string matching
anthropic - For accessing Claude (LLM) via the Anthropic API
