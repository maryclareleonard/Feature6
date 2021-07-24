This details notes for my feature 6, resources I used and details about my changes.

EPIC 1: Email Verification

(1)	I used EmailJS to complete this feature.
(2)	The DoggyService.js file, where functions like moveDoggyDate and createDoggyDate are defined, is where emailDoggyDate is defined. RemoveDoggyDate, which is prompted when the “Request Date” button is pushed, calls emailDoggyDate() before the doggyDate is then destroyed, and removed from the database.
(3)	emailDoggyDate calls ContactUs(), the function that DoggyDate/Email.js defines. This function sends the information needed to the emailJS template.
(4)	The emailjs.send function takes 
o	the service id
o	the template id
o	the templateParams (defined in the js file)
o	my user id for the platform
(5)	I opted to use EmailJS because I wanted to use an external emailing platform so that email username/password would not be accessible if someone were to dig through the code via inspect source.

 
EPIC 2: Logout
Notes: 
(1)	In order to do this I included a log out button on the DatesList.js file with a handler.
(2)	The handler first does calls the AuthService function logout() that calls Parse.User.logOut()
(3)	Then the handler uses useHistory to redirect to “home”.


 
EPIC 3: Routing Refinement
Notes: I did this story for two reasons:
(1)	I put in a lot of effort past the deadline for the last feature in order to figure out what we were doing wrong, so I was very excited to get it to work
(2)	It is nice to give feedback that will not end up being an ugly error.  

In trying to affect the routing at the Components.js file I was overcomplicating things and after taking a step back I realized I needed to handle the case within MainGood.js, 
the main page for our doggy date site. Lines 20-33 will cause the user to be redirected to the error page IF a URL is attempted with an invalid username or a username that is n
ot currently logged in.

EPIC 4: CSS 
Notes: The following our elements I added designed via CSS
-	Text/titles
-	Background
-	Buttons
-	hr: color, size (as a function of the window width)
-	I used the display formatting tool to treat forms as tables, divs surrounding labels and inputs as table rows, labels as table cells and inputs as table cells so that input boxes were aligned
-	Instead of list items being organized by bullets, I used a class list to organize them into boxes.
-	LogOut button on upper right of screen
