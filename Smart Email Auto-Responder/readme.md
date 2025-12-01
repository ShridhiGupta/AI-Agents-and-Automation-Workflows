# 📧 Smart Email Auto-Responder

An AI-powered workflow that automatically classifies incoming emails and generates context-aware draft responses using the Google Gemini Chat Model.

## Features
- **Instant Trigger:** Activates immediately upon receiving a new email via Gmail.
- **AI-Driven Classification:** Uses a **Text Classifier** node to determine the nature of the email (e.g., 'Order,' 'Inquiry,' 'General').
- **Context-Specific Drafting:** Routes the email to a tailored AI model (`Message a model` / `Message a model 2`) based on the classification.
- **Draft Creation:** Automatically generates and saves a personalized draft response in Gmail for the user's review and final send.

## How It Works
1. A new email arrives, triggering the **Gmail Trigger** node.
2. The email content is fed into the **Text Classifier** to categorize the request (e.g., 'Order' or 'Inquiry').
3. Based on the classification, the workflow follows a specific path:
    * **Path 1 (e.g., 'Order'):** Waits for a specified duration, sends the email details to the **Google Gemini Chat Model** (via `Message a model`) with an instruction to draft an 'Order Confirmation' or 'Fulfillment' response, and then uses **Create a draft** to save it.
    * **Path 2 (e.g., 'Inquiry'):** Waits for a specified duration, sends the details to the **Google Gemini Chat Model** (via `Message a model 2`) with an instruction to draft a 'Detailed Answer' or 'Support' response, and then uses **Create a draft 1** to save it.

## Setup
Import workflow → Connect **Gmail Trigger** credentials → Connect **Google Gemini Chat Model** credentials → Configure Text Classifier labels and routing → Activate.
