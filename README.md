
# Excel Data Query with Google Generative AI

This project allows users to query data from an Excel file using Google Generative AI. The code loads an Excel file, formats the data, and sends it along with a question to a generative AI model, which then returns an answer based on the data context.

## Overview

This Python script integrates Google Generative AI to answer questions based on data from an Excel file. It uses `pandas` to read and format the data and the google.generativeai library to interact with a generative AI model. 

## Setup

1. API Key Configuration: This script requires a valid Google Generative AI API key. Please ensure you have access to this API and update the API key in the script.

2. Library Dependencies: Make sure the following libraries are installed:
 
   pip install google-generativeai pandas openpyxl

3. Excel Data: Prepare an Excel file containing the data you wish to query. Ensure it is formatted correctly and accessible by the script.

## Usage

1. Place your Excel file in the directory and update the `file_path` variable with the path to your file.

2. Modify the `question` variable with the question you want to ask based on the Excel data.

3. Run the script to receive an answer based on the context of the Excel data and the question provided.

file_path = "/path/to/your/Excel_file.xlsx"  # Update with your file path
question = "What is the name of the Country for City Lisbon?"
ask_model_with_excel(file_path, question)

### Functions

load_excel_data(file_path): Loads the Excel file and formats it for the AI prompt.
`send_request(chat, context, question): Sends the formatted data and question to the AI model and returns the response.
ask_model_with_excel(file_path, question): Main function to load data, interact with the AI model, and display the answer.

## Example

Suppose your Excel file contains city and country data, and you want to know which country the city "Lisbon" belongs to. Set up the file path and question as follows:

file_path = "/path/to/Travel_Agency_Offers.xlsx"
question = "What is the name of the Country for City Lisbon?"
ask_model_with_excel(file_path, question)

The script will print the answer based on the data in the file.
