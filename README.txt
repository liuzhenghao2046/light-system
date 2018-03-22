To compile: make
To run: ./output --docroot /usr/local/share/Wt --http-address 0.0.0.0 --http-port 8080

Make sure V0.6 of the emulator is running to use commands properly

Once logged in:

To create a bridge: fill in the first 4 fields (name,ip,location,port and with the optional 5th for username) 
	with valid information then click the create bridge button.
	Once a bridge is created it is also selected.
	To get a list of bridges click get all bridges. this will show all the bridges and their ids at the bottom of the page.
	To select a new bridge enter bridge id where it says select bridge by id: then click select bridge.
	To delete a bridge enter the id into the same field and click delete bridge
	To edit a bridge enter the id into the same field and fill out the same fields used to create a bridge.
	
Lights: (must have a bridge specified from above to do any light commands!):
	To change a light you will have to have a bridge selected. 
	Once you create a bridge it is automatically selected or you can also select a new bridge like explained above.
	
	To edit light states fill in the fields you want to edit with valid information and press change light. Note: the only required field is light 
	number everything else is optional and will not be changed unless you fill information in
	
	To view all lights press get all lights
	To get a specific light fill in the light num field with the light you want to view then press get specific light
	
	To start a recurring hue cycle change enter the amount of time you want it to take in seconds for 
	a full hue cycle to happen in the input field then click start light recur. A light number and bridge must be specified
	
Groups:
	To create a group you must specify a bridge above.
	Enter the name of the group you want in the field name the group
	also Enter the lights you want inside the group separted by commas inside the field
	Enter which lights to group(separate by comma no duplicates)
	Then click create group
	
	To get all group ids clck the get all groups button and they will be displayed at the bottom of the page
	
	To edit a group (must have a bridge specified):
		enter the group ID you want to edit
		Editing group states uses the same input fields as editing light fields.
		Fill in the states you wish to change above as well as the group id inside enter group number to edit
		then click change group states.
		To get the group states of a specific group enter the id inside enter group number to edit then clcik get group states. The information will display at the bottom of the page
		
	To delete a group enter the id in the enter group number to edit field then press delete group.

Scheduler:
	To create a schedule: you will have to have a bridge currently selected/specified
	You will also need to enter the name of the schedule, description, year, month, hours, minutes, seconds.
	The light/group num field will act as a field that will hold either the light id or the group id.
	Enter the field below to change the fields you want to edit.
	To create a schedule for a specific light press schedule light button. To create a schedule for groups press the schedule group button.
		
	To get all schedule ids and their name press get all schedules.
	To get information on a specific schedule enter the id then press get schedule information
	To edit a schedule enter the schedule id into the Enter schedule ID: field then edit the states like you did to create the schedule.
	To remove a schedule simply enter the id then click remove schedule.
Note for scheduler: A schedule must happen in the future not the past. local time may or may not be off by a couple hours depending on time zone.
	
Additional Features:

	Reccuring Hue Color Change: A user can have a specific light or a specific group 
		continously change hues in a cycle until they press the stop button. The inputted number is how long it will take to do a full cycle. 
		This is done asynchronously with WTs built in thread and event handling to avoid hanging the program while the recurring schedule/cycle runs.
	

	Holiday themed lights: Pressing the "set light for closest Holiday" button will changes the 3 lights for the current bridge into a holiday themed color set up
		depending on the closest holiday. Currently only supports Halloween and Christmas