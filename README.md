Task 1: Serverless Web Application

Build a serverless web app on cloud using service like Lambda, API Gateway, and DynamoDB for dynamic functionality. Use AWS Amplify or SAM for deployment automation.


![Untitled Diagram drawio - draw io - Google Chrome 21-05-2024 01_00_35](https://github.com/Yash03032002/Encryptix_taskno.01/assets/151602561/41403981-5fb3-4520-9f69-4df3fa334d04)

In this task, you will create a serverless web application that enables users to request unicorn rides from the Wild Rydes fleet. The application will present users with an HTML-based user interface for indicating a pick-up location and a RESTful web service on the backend to submit the request for dispatching a unicorn. The application will also provide facilities for users to register with the service and log in before requesting rides.

Steps to build a serverless web app using AWS:

1. Create a Git repository and push all the required files and folders to that repository.
2. Launch the AWS Amplify console. Under the Amplify Hosting Host your web app header, choose Get Started. On the Get started with Amplify Hosting page, select GitHub and choose Continue.
3. Create a Amazon Cognito user pool and integrate an app with your user pool. In the Amazon Cognito console, choose Create user pool. On the Configure sign-in experience page, in the Cognito user pool sign-in options section, select User name. Keep the defaults for the other settings, such as Provider types and do not make any User name requirements selections. Choose Next.
4. On the Configure security requirements page, keep the Password policy mode as Cognito defaults. You can choose to configure multi-factor authentication (MFA) or choose No MFA and keep other configurations as default. Choose Next.
5. On the Configure message delivery page, for Email provider, confirm that Send email with Amazon SES - Recommended is selected. In the FROM email address field, select an email address that you have verified with Amazon SES, following the instructions in Verifying an email address identity in the Amazon Simple Email Service Developer Guide. Note: If you don't see the verified email address populating in the dropdown, ensure that you have created a verified email address in Amazon SES.
6. Update the website comfig file. Update the cognito section of the file with the correct values for the User pool ID and App Client ID you saved in Steps 8 and 9 in the previous section. The userPoolID is the User pool ID from the User pool overview section, and the userPoolClientID is the App Client ID from the App Integration > App clients and analytics section of Amazon Cognito.
7. Save the module file and push the changes.
8. Validate the implimentation. Complete the registration form and choose Let's Ryde. You can use your own email or enter a fake email. Make sure to choose a password that contains at least one upper-case letter, a number, and a special character. Don't forget the password you entered for later. You should see an alert that confirms that your user has been created.
9. Build a serverless backend. Create a Amazon DynamoDB table. Create an IAM role for your lamda function. Create a Lamda function for handling request. Validate your implimentation.
10. Deploy a RESTful API. In the Amazon API Gateway console, select APIs in the left navigation pane. Choose Build under REST API. In the Choose the protocol section, select REST. In the Create new API section, select New API. Choose Create API.
11. Create an Amazon Cognito User Pools Authorizer. Amazon API Gateway uses JSON web tokens (JWT), which are returned by the Amazon Cognito User Pool (created in Module 2) to authenticate the API calls. In this section, we will be creating an Authorizer for the API, so we can make use of the user pool.
12. Create a new resource within your API. Then create a POST method for that resource and configure it to use a Lambda proxy integration backed by the RequestUnicorn function you created in the first step of this module.
13. Deploy your API and copy the Invoke URL.
14. Update the website /js/config.js file in your website deployment to include the Invoke URL of the stage you just created. You will copy the Invoke URL directly from the top of the stage editor page on the Amazon API Gateway console and paste it into the invokeUrl key of your site's config.js file. Your config file will still contain the updates you made in the previous module for your Amazon Cognito userPoolID, userPoolClientID, and region and push the changes.
15. Validate your implimentation.

Serverless Web App URl: https://master.d1lapbc2qfmaxw.amplifyapp.com/
