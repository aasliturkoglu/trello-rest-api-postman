# 📋 trello-rest-api-postman

This project demonstrates how to create boards, lists, card, checklist, and label using the Trello API via Postman.

## 📑 Content

- [Requirements](#requirements)
- [Getting API Key and Token](#getting-api-key-and-token)
- [Postman Setting Environment Variables](#postman-setting-environment-variables)
- [API Operations](#api-operations)
  - [Create a Board](#create-a-board)
  - [Create a new List](#create-a-new-list)
  - [Create a Card](#create-a-card)
  - [Create a Checklist](#create-a-checklist)
  - [Create a Label](#create-a-label)

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

## Postman Setting Environment Variables

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

## API Operations

### 1. Create a Board

  1. Open the [Trello Rest API Documentation](https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-post)
  2. Copy the URL in the [Trello Rest API Documentation](https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-post)
  3. Go to Postman
  4. Create a new request and give a name (Create a Board). The method type for this operation is POST. Choose POST. Paste the URL and Convert the BaseURL part of URL to the global variable we created for BaseURL. Use enviroment variables we created for API Key and Token. Then give a name for new board.
<img height="400" src="https://github.com/user-attachments/assets/ef053232-96ce-4838-a662-bb0561d95a1c" />

 5. Write test to check the response status code.
<img  height="400" src="https://github.com/user-attachments/assets/a2f1dcb0-e4fc-4aa1-9f3c-b228b35664b5" />

6. Send the request. Response should be 200.
7. Check the Trello.
<img height="400" src="https://github.com/user-attachments/assets/47e07081-9232-44ad-83e8-d5446ee719d7" />

### 2. Create a new List

  1. Open the [Trello Rest API Documentation](https://developer.atlassian.com/cloud/trello/rest/api-group-lists/#api-lists-post)
  2. Copy the URL in the [Trello Rest API Documentation](https://developer.atlassian.com/cloud/trello/rest/api-group-lists/#api-lists-post)
  3. Go to Postman. Create a new request and give a name (Create a new List). The method type for this operation is POST. Choose POST. Paste the URL and Convert the BaseURL part of URL to the global variable we created for BaseURL. Use enviroment variables we created for API Key and Token. Then give a name for new board.
  4. Give a name for new list.
  5. To determine which board to add the list to, copy the id of the board we created in the previous step and paste it into the value field opposite the idBoard parameter.
  6. Write test to check the response status code. Send the request. Response should be 200.
<img height="400" src="https://github.com/user-attachments/assets/26ce9f4c-b7a4-4ba1-85f7-1286db46bc62" />
  
  7. Check the Trello.
<img height="400" src="https://github.com/user-attachments/assets/c5b82d93-6247-4c1d-ab4d-1a5294364ba2" />








