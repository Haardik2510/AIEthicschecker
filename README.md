# AIEthicschecke
from textblob import TextBlob

def analyze_text(text):
    # Create a TextBlob object
    blob = TextBlob(text)
    
    # Perform sentiment analysis
    sentiment = blob.sentiment

    # Determine sentiment polarity (positive, negative, or neutral)
    polarity = sentiment.polarity

    if polarity > 0:
        return "Positive"
    elif polarity < 0:
        return "Negative"
    else:
        return "Neutral"

if __name__ == "__main__":
    input_text = input("Enter text for analysis: ")
    result = analyze_text(input_text)
    print(f"Sentiment: {result}")
