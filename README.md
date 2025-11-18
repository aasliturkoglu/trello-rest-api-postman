# 📋 trello-rest-api-postman

This project demonstrates how to create boards, lists, card, checklist, and label using the Trello API via Postman.

## 📑 Content

- [Requirements](#-requirements)
- [Getting API Key and Token](#-getting-api-key-and-token)
- [Postman Setting Environment and Global Variables](#%EF%B8%8F-postman-setting-environment-and-global-variables)
- [API Operations](#--api-operations)
  - [Create a Board](#1%EF%B8%8F⃣-create-a-board)
  - [Create a new List](#2%EF%B8%8F⃣-create-a-new-list)
  - [Create a new Card](#3%EF%B8%8F⃣-create-a-new-card)
  - [Create a Checklist](#4%EF%B8%8F⃣-create-a-checklist)
  - [Create a Label](#5%EF%B8%8F⃣-create-a-label)
- [Collection Runner](#%EF%B8%8F-collection-runner)
- [Dynamic Variables](#-dynamic-variables)
- [Pre-request Scripts](#-pre-request-scripts)

## 📋 Requirements 

- [Postman](https://www.postman.com/downloads/) (Web or Desktop)
- [Trello](https://trello.com) (Web or Desktop)
- Trello API Key and Token
- [Trello Rest API Documentation](https://developer.atlassian.com/cloud/trello/rest/api-group-actions/#api-group-actions)

## 🔑 Getting API Key and Token

1. Create an Account on [Trello](https://id.atlassian.com/signup?application=trello&continue=https%3A%2F%2Ftrello.com%2Fauth%2Fatlassian%2Fcallback%3FreturnUrl%3D%252Fpower-ups%252Fadmin%26display%3DeyJ2ZXJpZmljYXRpb25TdHJhdGVneSI6InNvZnQifQ%253D%253D%26aaOnboarding%3D%26updateEmail%3D%26traceId%3D%26ssoVerified%3D%26createMember%3Dtrue%26jiraInviteLink%3D&display=eyJ2ZXJpZmljYXRpb25TdHJhdGVneSI6InNvZnQifQ%3D%3D)

2. Create a Workspace on Trello

3. Activate the [Power-Up](https://trello.com/power-ups/admin)

4. Click the New button in the upper right corner

5. Fill in the new power-up field and select workspace then click the Create button

6. Click the Generate a new API Key button

7. Then API Key is created and final step click the Token button

## ⚙️ Postman Setting Environment and Global Variables

1. Create a Collection on Trello
<img height="400" src="https://github.com/user-attachments/assets/46b5e98b-e0ce-4ac2-bbae-e6d4d5f01d26" />

2. Create a Collection on Trello

3. Click the Variables in this Request button in the upper right corner
<img height="400" src="https://github.com/user-attachments/assets/185314d4-21ee-4f45-9d1d-15038c796bc7" />

4. Click the Enviroment button
<img height="400" src="https://github.com/user-attachments/assets/8f454f8d-461e-43dc-9c00-4d7405e33199" />

5. Give names for key and token and enter the token and key values
<img height="400" src="https://github.com/user-attachments/assets/1b352ee9-7c15-4ebe-9c41-787d121b5ec2" />

6. Repeat step 3.

7. Click the Globals

8. Add the baseURL portion of the url from the REST API documentation.
<img height="400" src="https://github.com/user-attachments/assets/d8126d0f-5e6c-40da-a110-cca51b6ff504" />

For example, in this URL, 
https://api.trello.com/1/actions/{id}?key=APIKey&token=APIToken ---> the BaseURL is https://api.trello.com/

## 🌐 🔗 API Operations

### 1️⃣ Create a Board

  1. Open the [Trello Rest API Documentation](https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-post)
  2. Copy the URL in the [Trello Rest API Documentation](https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-post)
  3. Go to Postman
  4. Create a new request and give a name (Create a Board). The method type for this operation is POST. Choose POST. Paste the URL and Convert the BaseURL part of URL to the global variable we created for BaseURL. Use enviroment variables we created for API Key and Token. Then give a name for new board.
<img height="400" src="https://github.com/user-attachments/assets/ef053232-96ce-4838-a662-bb0561d95a1c" />

 5. Write test to check the response status code.
<img  height="400" src="https://github.com/user-attachments/assets/a2f1dcb0-e4fc-4aa1-9f3c-b228b35664b5" />

6. Send the request. Response status code should be 200.
7. Check the Trello.
<img height="400" src="https://github.com/user-attachments/assets/47e07081-9232-44ad-83e8-d5446ee719d7" />

### 2️⃣ Create a new List

  1. Open the [Trello Rest API Documentation](https://developer.atlassian.com/cloud/trello/rest/api-group-lists/#api-lists-post)
  2. Copy the URL in the [Trello Rest API Documentation](https://developer.atlassian.com/cloud/trello/rest/api-group-lists/#api-lists-post)
  3. Go to Postman. Create a new request and give a name (Create a new List). The method type for this operation is POST. Choose POST. Paste the URL and Convert the BaseURL part of URL to the global variable we created for BaseURL. Use enviroment variables we created for API Key and Token.
  4. Give a name for new list.
  5. To determine which board to add the list to, copy the id of the board we created in the previous step and paste it into the value field opposite the idBoard parameter.
  6. Write test to check the response status code. Send the request. Response status code should be 200.
<img height="400" src="https://github.com/user-attachments/assets/26ce9f4c-b7a4-4ba1-85f7-1286db46bc62" />
  
  7. Check the Trello.
<img height="400" src="https://github.com/user-attachments/assets/c5b82d93-6247-4c1d-ab4d-1a5294364ba2" />

### 3️⃣ Create a new Card

  1. Open the [Trello Rest API Documentation](https://developer.atlassian.com/cloud/trello/rest/api-group-lists/#api-lists-post)
  2. Copy the URL in the [Trello Rest API Documentation](https://developer.atlassian.com/cloud/trello/rest/api-group-lists/#api-lists-post)
  3. Go to Postman. Create a new request and give a name (Create a new Card). The method type for this operation is POST method. Choose POST method. Paste the URL and Convert the BaseURL part of URL to the global variable we created for BaseURL. Use enviroment variables we created for API Key and Token.
  4. Paste "&name=" to end of the URL. This will create the name parameter.
  5. Give a name for new card.
  6. To determine which list to add the card to, copy the id of the list we created in the previous step and paste it into the value field opposite the idList parameter.
  7. Write test to check the response status code. Send the request. Response status code should be 200.
<img height="400" src="https://github.com/user-attachments/assets/673f781f-aeed-4d6e-b822-47f72eef9cdb" />

  8. Check the Trello.
<img height="400" src="https://github.com/user-attachments/assets/c01e3fca-a7fe-4cb6-80f0-69d334d0be72" />

### 4️⃣ Create a Checklist

  1. Open the [Trello Rest API Documentation](https://developer.atlassian.com/cloud/trello/rest/api-group-checklists/#api-checklists-post)
  2. Copy the URL in the [Trello Rest API Documentation](https://developer.atlassian.com/cloud/trello/rest/api-group-checklists/#api-checklists-post)
  3. Go to Postman. Create a new request and give a name (Create a Checklist). The method type for this operation is POST method. Choose POST method. Paste the URL and Convert the BaseURL part of URL to the global variable we created for BaseURL. Use enviroment variables we created for API Key and Token.
  4. Paste "&name=" to end of the URL. This will create the name parameter.
  5. Give a name for checklist.
  6. To determine which card to add the checklist to, copy the id of the card we created in the previous step and paste it into the value field opposite the idCard parameter.
  7. Write test to check the response status code. Send the request. Response status code should be 200.
<img height="400" src="https://github.com/user-attachments/assets/142c416a-e11f-45a6-98ad-c5220c6510f5" />

  8. Check the Trello.
<img height="400" src="https://github.com/user-attachments/assets/78aba438-b6c1-49da-bc26-900552e16e48" />

### 5️⃣ Create a Label

  1. Open the [Trello Rest API Documentation](https://developer.atlassian.com/cloud/trello/rest/api-group-labels/#api-labels-post)
  2. Copy the URL in the [Trello Rest API Documentation](https://developer.atlassian.com/cloud/trello/rest/api-group-labels/#api-labels-post)
  3. Go to Postman. Create a new request and give a name (Create a Label). The method type for this operation is POST. Choose POST method. Paste the URL and Convert the BaseURL part of URL to the global variable we created for BaseURL. Use enviroment variables we created for API Key and Token.
  4. Give a name for label and choose a color from among the valid colors. Valid values: yellow, purple, blue, red, green, orange, black, sky, pink, lime for color parameter.
  5. To determine which board to add the label to, copy the id of the board we created in the first step and paste it into the value field opposite the idBoard parameter.
  6. Write test to check the response status code. Send the request. Response status code should be 200.
<img height="400" src="https://github.com/user-attachments/assets/5b8a409b-71b1-43cf-8c2e-9c3fd9bb81db" />

  7. Check the Trello.
<img height="400" src="https://github.com/user-attachments/assets/d7f6b415-f0ba-409f-8692-5d72793e483c" />

## ▶️ Collection Runner

  1. Click the name of the collection. Then click the Runs button.
<img height="400" src="https://github.com/user-attachments/assets/0c8de1c8-a134-4f0c-98b8-480fbc7138fe" />

  2. Click the Run Project button.
<img height="400" src="https://github.com/user-attachments/assets/8274dfe5-a97d-4a69-8236-6c2527bb1712" />

  3. View the Result
<img height="400" src="https://github.com/user-attachments/assets/0e6fc577-3a15-464d-aa7c-c92ea9d0474a" />
    
  4. View the Summary
<img height="400" src="https://github.com/user-attachments/assets/f878d309-a3e8-4641-b985-346c3855c92f" />

## 🔁 Dynamic Variables

By storing values returned from the API—such as id or name—in a variable, we can reuse them in subsequent requests. This eliminates the need for manual copy-paste and allows Postman to automatically pass data from one response to the next request. As a result, dependent operations can be executed in a seamless, chained, and dynamic workflow.

  1. Saving the ID in the Post-request Script
    Firstly, In the Tests (Post-request Script) section, we extract the response body and store a specific value (such as an ID) in an environment variable:
    let response = pm.response.json();
    pm.environment.set("idboard", response.id);
  <img height="400" src="https://github.com/user-attachments/assets/25978be8-f416-44b9-83c2-79f2d2549205" />
  <img height="400" src="https://github.com/user-attachments/assets/7452de83-ebd1-403d-abd2-8b64cdd50eca" />

  The idboard variable we set here will be automatically created and stored in the Environments section. This allows Postman to reuse it in other requests without any manual input.

  2. Using the idboard Variable in Create a List Request

  <img height="400" src="https://github.com/user-attachments/assets/c808946d-940c-478b-8cae-83edb4f72fde" />

  Apply the same process we used in the previous step to save the list ID. After creating the list, extract the response and store the returned id value as an environment variable (e.g., idlist). This will allow us to reuse the list ID in the following requests just like we did with idboard.

  <img height="400" src="https://github.com/user-attachments/assets/a077216e-2319-4012-a636-66302a499d90" />

  You can apply these steps to all operations in the project. By saving each returned ID (board, list, card, checklist, label) as an environment variable, you can easily reuse them in subsequent requests and create fully connected, automated API workflows.
  
  Using the Collection Runner, you can run the project multiple times in succession without errors. Since all IDs are dynamically stored and reused via environment variables, the requests remain fully connected and automated, allowing for seamless repeated execution.

## 📝 Pre-request Scripts

Pre-request scripts are executed before sending an API request. They allow us to:

  * Set or update environment and global variables dynamically

  * Generate timestamps, tokens, or random data required for the request

  * Prepare any data or configuration needed for the request to run successfully

Essentially, they let us automate setup tasks so that each request has the correct data and context before execution.

  1. pm.environment.set("nameBoard", "udemy " + parseInt(Math.random()*1000));  in the Pre-request field for nameBoard

<img height="400" src="https://github.com/user-attachments/assets/f7fb6868-a81d-4758-b6d7-95420d88644f" />

  2. Use this nameBoard variable in the request

<img height="400" src="https://github.com/user-attachments/assets/33106ab3-1aba-4fc2-b907-8ef33417072b" />

  3. Write a Test and Check

  let response = pm.response.json(); // we wrote this already
  pm.test("response name is equal to expected name", function () {
    pm.expect(response.name).is.eql(pm.environment.get("nameBoard"));
    console.log("response name: ", response.name);
    console.log("expected name: ", pm.environment.get("nameBoard"));

});

<img height="400" src="https://github.com/user-attachments/assets/887dc807-911c-47ab-93b3-f1ac11352d19" />






