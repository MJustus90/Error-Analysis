# Conceptual Database Design and Description of Tables

	Users will create an account or continue with a temporary profile. Users will submit measurements for various calculations. If the users created an account, the results of these calculations are displayed and then stored for future access. If they are using a temporary profile, the results will be displayed but not stored for future use.


## Users:
	Users will create a profile if they want to save and access old calculations. The User profiles will store their userID, First and Last Name, Email address, Username, and Password. Users will be linked to other tables by their userID.
	If users do not want to create a profile, they will be given a temporary userID to use for their current calculation without the ability to view old calculations.
	
## Submissions:
	Users will define the type of input they will submit and then enter their measurements. These details will decide which type of calculation will be conducted.

## Calculations:
		Based on the input type, a calculation method will be determined and therefore conducted. The results will be sent to a separate table to view.
		
## Results:
	The results will be will be stored in their own table where they can be accessed by their result ID
	
## UserHistory:
	Users can access the UserHistory table by their UserID. The UserHistory table is then connected to the results table through the Result ID.