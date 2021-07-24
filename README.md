# Feature6
This README.md file describes my stories. The epic is the overlying idea/functionality. The stories detail more specificities in the form of scenarios. More details on changes I made and resources I used are in the CHANGELOG.md

EPIC 1: Email Verification
Story 1: Valid Email Address
Given that user’s username is their email address 
When a user selects a doggy date by clicking “Request Date” 
Then the user will be emailed verification with details on the other owner, date of event, and time of event.

Email template: [Parameters are filled in based on user data.]
Hello {{first}} {{last}},
You have scheduled a date for your dog on {{dateDay}} at {{dateTime}} with Owner {{dateName}}.
Have a blast!
Warm Regards from Maryclare and Lucas!

Story 2: Invalid Email Address 
Given that user’s username is not a valid email address
When a user selects a doggy date by clicking “Request Date” 
Then the email will not be sent, yet no error will be displayed to the user

 
EPIC 2: Logout
Story 1: 
Given that the user is logged in on the main page
When they press logout 
Then they will be redirected back to the “home” page

Story 2: 
Given that the user just logged out
	If they try to reaccess the main page that they were just on
When they type in the url they were just at, i.e. https://x/user/{username} 
Then they will be redirected to the error page.

Story 3:
Given that the user redirects to the home page via URL
	And they have not logged out
When they type in their user url, i.e. https://x/user/{username}
Then they will be sent back to their home page
  Because they have not logged out.

EPIC 3: Routing Refinement
Story 1: 
Given that the user tries to access their home page via URL
  And they have not logged in
When they type the URL in
Then they will be redirected to the error page
  And there is a button to easily redirect to home page
  
Story 2: 
Given that the user tries to access an invalid path via URL
When they type the URL in
Then they will be redirected to the error page
  And there is a button to easily redirect to home page

EPIC 4: CSS 
Story 1: 
Given that you are not a programmer
When you see a pure html/js page
Then you are thoroughly unimpressed.

