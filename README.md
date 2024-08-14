Real Estate Project Analysis

Overview

This project provides a comprehensive analysis of real estate projects in a specified location. It identifies competitive projects, gathers key details using Google APIs, and compares amenities using advanced summarization techniques. The final result is a detailed comparison of competing real estate projects, helping potential buyers make informed decisions.

Table of Contents

- Prerequisites
- Setup and Installation
- Functionality
- Usage
- Deployment
- Testing

##Prerequisites

- Python 3.8 or higher
- API keys for Google Places and Hugging Face
- Required Python libraries:
   - requests
   - pandas

Setup and Installation

1.Clone the Repository:

git clone https://github.com/yourusername/real-estate-analysis.git

cd real-estate-analysis

1.Install Dependencies:

pip install requests pandas

1. Add Your API Keys: Replace "YOUR\_GOOGLE\_PLACES\_API\_KEY" and "YOUR\_HUGGINGFACE\_API\_KEY" in the analyze\_real\_estate function with your actual API keys.

Functionality

1. Identify Competitive Real Estate Projects

Fetch competitive real estate projects within a specified radius from a given location using the Google Places API.

1. Obtain Key Details

Retrieve detailed information about each project using Google Places API.

1. Compare Amenities

Use Hugging Face’s BART model to summarize the amenities of each project. This step involves:

- Generating summaries of amenities.
- Comparing these summaries to identify key differences and advantages.

4\. Modular Function

The analyze\_real\_estate function performs the entire analysis process and returns a DataFrame with the summarized comparison of real estate projects.

Usage

1. Define API Keys and Parameters: Ensure you have the correct API keys and set up the parameters, including location coordinates and radius.
1. Run the Analysis:

api\_keys = {

"google\_places": "YOUR\_GOOGLE\_PLACES\_API\_KEY",

"huggingface": "YOUR\_HUGGINGFACE\_API\_KEY"

}

location\_coords = "12.902111609527427,77.63996575110015"

radius = 10000

project\_details\_df = pd.DataFrame()  # Your DataFrame with project details

amenities\_df = pd.DataFrame()  # Your DataFrame with amenities details

results = analyze\_real\_estate(location\_coords, radius, api\_keys, project\_details\_df, amenities\_df)

print(results)

1. Review Results: The function will output a DataFrame with the summarized details of competing real estate projects.

Deployment

1. Serverless Deployment: Deploy the analyze\_real\_estate function as a serverless function using AWS Lambda, Google Cloud Function, or Azure Function.
1. API Integration: Optionally, use an API Gateway to expose the function as a web service.

Testing

1. Unit Testing: Test the analyze\_real\_estate function with different inputs and validate the output.
1. Performance Testing: Ensure the function performs efficiently with large datasets.






