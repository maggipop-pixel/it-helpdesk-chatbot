# 📚 How to Add New FAQs

## Overview
The knowledge base lives in Pinecone as vector embeddings. To add new FAQs you need to upload them via the Make.com scenario.

## Steps

### 1. Prepare your FAQ
Format your new FAQ as:
- **Question:** The user question
- **Answer:** The detailed response

### 2. Add to Pinecone
1. Go to your Make.com scenario
2. Run the FAQ upload module with your new question/answer pair
3. Pinecone will generate the embedding automatically

### 3. Test the new FAQ
1. Open the chatbot: https://maggipop-pixel.github.io/it-helpdesk-chatbot/
2. Ask the new question
3. Verify Status = `Resolved` in Airtable with score ≥ 0.6

## Tips
- Use natural language for questions
- Keep answers clear and step-by-step
- Test variations of the same question
