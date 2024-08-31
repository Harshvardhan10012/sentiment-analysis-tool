# sentiment-analysis-tool
This project is a simple Sentiment Analysis tool built using Python and the TextBlob library. The tool is designed to determine the sentiment of a given text, classifying it as Positive, Negative, or Neutral. It's a great introduction to working with text data and learning how to use pre-built models for natural language processing (NLP).
steps
Step 1: Set Up the Environment
Make sure you have Python installed on your machine. You'll also need to install the textblob library, which can be done using pip:
pip install textblob
Step 2: Import the Required Libraries
from textblob import TextBlob
Step 3: Create a Function for Sentiment Analysis
Here’s a simple function that takes a text input and returns the sentiment (positive, negative, or neutral) along with the polarity score:
def analyze_sentiment(text):
    # Create a TextBlob object
    blob = TextBlob(text)
    
    # Get the sentiment polarity (-1 to 1)
    polarity = blob.sentiment.polarity
    
    # Determine sentiment
    if polarity > 0:
        sentiment = "Positive"
    elif polarity < 0:
        sentiment = "Negative"
    else:
        sentiment = "Neutral"
    
    return sentiment, polarity
Step 4: Test the Sentiment Analysis Tool
You can test this function with various sentences:
if __name__ == "__main__":
    text = input("Enter a sentence to analyze: ")
    sentiment, polarity = analyze_sentiment(text)
    print(f"Sentiment: {sentiment}, Polarity: {polarity}")
Step 5: Expand the Tool
You can expand this tool by adding more features, such as:

Batch Processing: Analyze multiple sentences or reviews at once.
Visualization: Create a visual representation of sentiment distribution.
User Interface: Build a simple GUI using libraries like Tkinter for user interaction.
