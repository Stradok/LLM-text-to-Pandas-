
# Mistral 7B Fine-Tuned for Query-to-Code Conversion Using Quantized LLMs

## Overview

This project presents a fine-tuned version of the **Mistral 7B** model, designed to convert natural language queries into executable **Pandas** code. The model leverages **Unsloth's quantized LLMs** to optimize performance and efficiency, enabling effective, chatbot-style data retrieval from CSV datasets. Users can simply ask questions in plain English, and the model will generate the corresponding code to answer these queries using the uploaded dataset.

## Key Features

- **Natural Language Query Interpretation**: Allows users to input questions in everyday language, which the model then translates into relevant Pandas code.
- **CSV-Specific Information Retrieval**: Processes the structure of an uploaded CSV file to ensure that generated code aligns precisely with the dataset’s schema.
- **Optimized for Efficiency**: Utilizes quantized LLMs, enhancing performance without compromising accuracy, making it suitable for limited-resource environments.
- **Interactive Chatbot Experience**: Provides responses in a conversational format, making it accessible and intuitive for users with varying levels of technical proficiency.

## How It Works

1. **Dataset Upload**: Users upload a CSV file.
2. **Query Input**: A natural language query is provided by the user (e.g., "Show the top 10 customers by sales").
3. **Code Generation**: The model converts the query into optimized Pandas code that’s tailored to the dataset.
4. **Output Display**: The generated code is executed, and the results are displayed to the user in a readable format.

## Example Usage

**Input Query**: 
```
"List the top 5 products with the highest sales in 2023."
```

**Generated Pandas Code**:
```python
df[df['year'] == 2023].groupby('product')['sales'].sum().nlargest(5)
```

**Response**:
```
Top 5 products by sales in 2023:
1. Product A - $120,000
2. Product B - $98,000
...
```

## Future Directions

- **Enhanced Query Flexibility**: Expanding the model’s ability to interpret a wider range of query structures and vocabulary.
- **Improved Contextual Awareness**: Adding context-sensitive responses based on dataset metadata, such as date ranges or category descriptions.
- **Error Handling**: Developing feedback for unsupported queries or incorrect code interpretations, guiding users on how to phrase queries effectively.
- **Visualization Support**: Implementing basic visualizations (e.g., trend lines, bar charts) for certain data types.
  
## Technical Setup

To replicate this project, you’ll need the following:

- **Mistral 7B Model** (fine-tuned version for query-to-code)
- **Unsloth Quantized LLM Framework**
- **Python 3.8+**
- **Pandas**, **Numpy** (for data manipulation)
  
### Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/mistral-query-to-code
   ```
   
2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Upload your CSV dataset and start querying!
