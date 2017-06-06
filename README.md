# Project
programmeer project
Meet @pp

‘Meet @pp’ allows users to create an event to go to a place they have always wanted to go or just like to go anytime soon. The app uses the Facebook API to login and register users as well as getting their public profile and friend list. Besides the Facebook login API to get the users info and friend list.  (https://developers.facebook.com/docs/facebook-login/ios) the app uses the Google places API (https://developers.google.com/places/) to look up the places and their info.  All the user and place info and authentication will be done with firebase in order to allow the use of the app offline as well as online.

The user data will be stored in an online database using firebase. This database will consist out of three tables: the users table, the places table and the joining users table. In the users table the primary key is the user’s Facebook ID. This ID as well as the Facebook name will also be linked to the place table. Also this table has an ID as primary key and contains all the data retrieved from Google Places the API. The joining users table contains the place ID referring to the place in the places table and the user ID referring to the user in the users table.

The app will consist out of six views. The first view is the login view that allows the user to log in with Facebook and if they are not registered yet it will register trough Facebook. This view will only appear if the user has logged out or if the user hasn’t registered yet. The next view is the ‘my places’ view that shows a search bar and a table view displaying the placed added by the user or attended by the user. If the user clicks on one of the places, he will be directed to the place view, showing a picture of the place, all the details about the place event as well as the users that join the event with their profile pictures. 

When the user types the search field in the ‘my places’ view he will see get a list of the ‘type ahead’ options from Google Places. When the user clicks on one of these suggestions, he will be directed to the ‘add place’ view. This view will display a picture of the place and contains text fields to enter the date and time of the event as well as a description of the event. The user can then add the event and will be redirected to the ‘my places’ view. The event will be added to the places table and will be displayed in the ‘my places’ table view of the user. 

When the user clicks on the ‘friends places’ button on the ‘my places’ view, he will be directed to the ‘friends places’ view. This will display a table view containing all the places added by friends. You can click on this place and go to the ‘place event’ view, that contains the place picture,  an added by user label, the date, time and event description. Underneath this info a table is displayed with all the users that join the event with their profile pictures and name. On the navigation bar a ‘join’ button is displayed. When the user clicks on this button, he will be added to the ‘joining users’ table and will be displayed in the ‘joining users table on the ‘place event’ page. The user will be redirected to the ‘search place’ view. When a user clicks on a place in this view, he will again be directed to the ‘place event’ view. 



The biggest risk in the project is the use of two API’s. Though they can be very helpful, they might cause problems with implementation and risk making the app more buggy. 

Though not a lot of apps are like this, the ‘event’ functionality of the Facebook app is a lot like it. This places the event central and allows the user to add details to it. The user can invite his friends to the app.  As ‘meet @pp’ is more of a social app all of the user’s friends can join the event. 

The MVP of the app is the functionality without the API’s. On this way the user can just fill in a place where he wants to go and subsequently other users can join him by clicking on the event. This way a user can register with an alert that asks for a username and password and uploads it to firebase. 

![App Visualisation](https://user-images.githubusercontent.com/27211421/26836816-28d422d0-4adc-11e7-891a-1fa6813fbb72.JPG)



Opening view with login
	Email
	Password
	Login with facebook


My places
	Add new place button
	Table view of places added by you
		Name of place
		Photo of place
		Description
	Table view of placed that you attend
		Name of place
		Photo of place
		Description
		
Add place
	Search field
	Add new place app

Place
	Name of place
	Photo of place
	Date/time
	Description
	Table view 
		Name of people who are down
	
Friends places
	Friends
		Table view of friends places


