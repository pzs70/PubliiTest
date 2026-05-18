---
title: Python Cheatsheet
type: docs
weight: 3
---
# 🐍 AI-901 Python Cheatsheet - Azure AI SDK alapok

A vizsgán fontos az alapvető kódstruktúrák felismerése. Íme a leggyakoribb minták:

## 1. Hitelesítés és Konfiguráció
Minden Azure AI szolgáltatáshoz szükség van egy **Endpoint**-ra és egy **Key**-re.

```python
# Alapvető importok és hitelesítés
from azure.core.credentials import AzureKeyCredential

endpoint = "https://YOUR_SERVICE_NAME.cognitiveservices.azure.com/"
key = "YOUR_SUBSCRIPTION_KEY"
credential = AzureKeyCredential(key)
```

## 2. Azure OpenAI (Generatív AI)
```python
from openai import AzureOpenAI

client = AzureOpenAI(
    azure_endpoint = endpoint, 
    api_key = key,  
    api_version = "2023-05-15"
)

response = client.chat.completions.create(
    model = "gpt-35-turbo", # deployment name
    messages = [
        {"role": "system", "content": "You are a helpful assistant."},
        {"role": "user", "content": "What is Azure AI?"}
    ]
)
print(response.choices[0].message.content)
```

## 3. Computer Vision (Képelemzés)
```python
from azure.ai.vision.imageanalysis import ImageAnalysisClient

client = ImageAnalysisClient(endpoint=endpoint, credential=credential)

with open("image.jpg", "rb") as f:
    result = client.analyze(
        image_data=f,
        visual_features=["Caption", "Read", "Tags"]
    )

print(result.caption.text)
```

## 4. Text Analytics (NLP)
```python
from azure.ai.textanalytics import TextAnalyticsClient

client = TextAnalyticsClient(endpoint=endpoint, credential=credential)

documents = ["I love using Azure AI Services!"]
response = client.analyze_sentiment(documents=documents)

for doc in response:
    print(f"Sentiment: {doc.sentiment}")
```

## 5. Leggyakoribb adattípusok felismerése
*   **`response.choices[0].message`**: OpenAI válasz kinyerése.
*   **`AzureKeyCredential(key)`**: A standard mód a kulcsos hitelesítésre.
*   **`.json()`**: API válaszok gyakori formátuma.
*   **Dictionary-k kezelése**: `{"role": "user", "content": "..."}` - a promptok struktúrája.

## 6. Hibakezelés (Exception Handling)
```python
from azure.core.exceptions import HttpResponseError

try:
    # API hívás
    pass
except HttpResponseError as e:
    print(f"Error: {e.message}")
```
