# Smart Bill Automation with AWS textract

- This project automates bill processing and reminders using **Amazon Web Services (AWS)**. 
- It extracts data from uploaded bills, stores them securely, and sends smart email notifications — all through a **serverless architecture**.

---

## **Architecture Overview**

- **Amazon S3**: Stores uploaded bills.
- **Amazon Textract**: Extracts text and structured data (amount, due date, provider) from bills.
- **AWS Lambda**: Handles logic for processing, extracting, storing, and triggering notifications.
- **DynamoDB**: Stores bill metadata for fast retrieval.
- **Amazon SES**: Sends reminder emails based on due dates.
- **IAM**: Manages secure access to AWS resources.

<img width="643" alt="image" src="https://github.com/user-attachments/assets/bbfcdc15-8c1d-471e-80f0-817a1b172a4d" />

## **How It Works**

1. **Upload PDF Bill to S3**  
   → Automatically triggers a Lambda function

2. **Text Extraction via Textract**  
   → Parses due date, amount, and provider info

3. **Data Stored in DynamoDB**  
   → Bill metadata is indexed and available for query

4. **Email Notification Sent via SES**  
   → Alerts for upcoming due dates or unusual spending

---

## **Tech Stack**

- AWS Lambda (Python)
- Amazon S3
- Amazon Textract
- DynamoDB
- Amazon SES
- IAM (for secure roles and policies)


