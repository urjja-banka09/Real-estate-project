Real Estate Project Analysis


Overview

This project provides a comprehensive analysis of real estate projects in a specified location. It identifies competitive projects, gathers key details using Google APIs, and compares amenities using advanced summarization techniques. The final result is a detailed comparison of competing real estate projects, helping potential buyers make informed decisions.

Table of Contents
Prerequisites
Setup and Installation
Functionality
Usage
Deployment
Testing


Prerequisites
Python 3.8 or higher
API keys for Google Places and Hugging Face

Required Python libraries:
requests
pandas

Setup and Installation
Clone the Repository:
git clone https://github.com/yourusername/real-estate-analysis.git
cd real-estate-analysis

Install Dependencies:
pip install requests pandas
Add Your API Keys:
Replace "YOUR_GOOGLE_PLACES_API_KEY" and "YOUR_HUGGINGFACE_API_KEY" in the analyze_real_estate function with your actual API keys.

Functionality
1. Identify Competitive Real Estate Projects
Fetch competitive real estate projects within a specified radius from a given location using the Google Places API.

2. Obtain Key Details
Retrieve detailed information about each project using Google Places API.

3. Compare Amenities
Use Hugging Face’s BART model to summarize the amenities of each project. This step involves:

Generating summaries of amenities.
Comparing these summaries to identify key differences and advantages.

4. Modular Function
The analyze_real_estate function performs the entire analysis process and returns a DataFrame with the summarized comparison of real estate projects.

Usage
Define API Keys and Parameters:
Ensure you have the correct API keys and set up the parameters, including location coordinates and radius.

Run the Analysis:

python
Copy code
api_keys = {
    "google_places": "YOUR_GOOGLE_PLACES_API_KEY",
    "huggingface": "YOUR_HUGGINGFACE_API_KEY"
}
location_coords = "12.902111609527427,77.63996575110015"
radius = 10000
project_details_df = pd.DataFrame()  # Your DataFrame with project details
amenities_df = pd.DataFrame()  # Your DataFrame with amenities details

results = analyze_real_estate(location_coords, radius, api_keys, project_details_df, amenities_df)
print(results)
Review Results:
The function will output a DataFrame with the summarized details of competing real estate projects.

Deployment
Serverless Deployment:
Deploy the analyze_real_estate function as a serverless function using AWS Lambda, Google Cloud Function, or Azure Function.

API Integration:
Optionally, use an API Gateway to expose the function as a web service.

Testing
Unit Testing:
Test the analyze_real_estate function with different inputs and validate the output.

Performance Testing:
Ensure the function performs efficiently with large datasets.
