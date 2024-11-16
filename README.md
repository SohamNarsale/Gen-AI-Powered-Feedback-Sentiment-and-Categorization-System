# Gen-AI Powered Feedback Sentiment and Categorization System 

This project is an Gen-AI powered sentiment analysis and feedback categorization tool. It processes feedback data, classifies sentiment (positive/negative), and categorizes feedback into predefined categories such as *Time Management*, *Content Quality*, *User Experience*, and more.

## Features
- **Sentiment Classification**: Classifies feedback into positive or negative sentiment.
- **Feedback Categorization**: Assigns feedback into relevant categories like *Time Management*, *Content Quality*, *Learning Opportunity*, etc.
- **Preprocessing Pipeline**: Cleans and preprocesses raw feedback text to prepare it for analysis.
- **Large Language Model (LLM) Integration**: Leverages **Mistral AI** for text understanding and **HuggingFace embeddings** for effective indexing and similarity search.
- **Interactive Chat Engine**: Generates structured feedback analysis with sentiment and category in a tabular format.

## Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/SohamNarsale/Gen-AI-Powered-Feedback-Sentiment-and-Categorization-System
   cd Gen-AI-Powered-Feedback-Sentiment-and-Categorization-System
   ```

2. **Install Dependencies**:
   Ensure you have Python 3.10 or higher. Install necessary libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure API Keys**:
   - Obtain an API key from [Mistral AI](https://console.mistral.ai/api-keys/) and add it to the code:
     ```python
     llm = MistralAI(api_key="YOUR_API_KEY", temperature=0.01, model='open-mixtral-8x7b')
     ```
## Usage

### 1. Preprocess Feedback Data
- Cleans feedback text to remove noise such as special characters, single characters, and extra spaces.

### 2. Sentiment and Category Classification
- Leverages an LLM-based chat engine to classify sentiments and categorize feedback. The results are output in a structured markdown table format.

### 3. Save Processed Feedback
- Outputs the preprocessed and classified feedback to a CSV file for further use.

## Example Input
A sample CSV file (`sentiments.csv`):
```csv
No,FeedBack
1,"Not enough time in the math section"
2,"Please improve the UI for better understanding of the questions"
3,"Great learning material!"
```

### Example Output
Generated feedback analysis:
| Feedback                                       | Sentiment | Feedback Category  |
|------------------------------------------------|-----------|---------------------|
| Not enough time in the math section            | Negative  | Time Management     |
| Please improve the UI for better understanding | Negative  | User Experience (UX)|
| Great learning material!                       | Positive  | Content Quality     |

## Code Workflow
1. **Data Preprocessing**: Cleans the feedback data.
2. **Indexing**: Uses LlamaIndex to create a vector store index for feedback.
3. **Chat Engine Configuration**: Customizes prompt templates for sentiment and category classification.
4. **Feedback Analysis**: Queries the LLM to generate structured sentiment and category output.

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/SohamNarsale/Gen-AI-Powered-Feedback-Sentiment-and-Categorization-System/blob/main/LICENSE) file for details.
