# Flash Chat Refactoring Challenge

### Part 1:

The welcome screen, the login screen and the registration screen all have the same style of button. The code for this button should ideally be in a separate class in its own file. 

* Locate the ```Padding``` widget that contains the ```MaterialButton``` in the welcome_screen.dart. Make a note of the colours of the buttons. You'll need these colours later. 

* Extract the entire ```Padding``` widget into a separate StatelessWidget called ```RoundedButton```. 

* Add three properties to the ```RoundedButton```: a ```Color``` variable, a ```String``` variable for button title, and a ```Function``` variable for the button's ```onPressed```  callback. Modify the ```RoundedButton```'s constructor so that these properties are assigned a value when a ```RoundedButton``` is created. 

* Modify the code in the ```RoundedButton``` to replace the hard-coded title, colour, and onPressed callback to use the three properties you created above. 

* Create a new directory under ```lib``` called ```components```. Inside ```components``` create a new file called ```rounded_button.dart```. 

* Add the code for the ```RoundedButton``` class to the new file. 

* Refactor the code in the welcome_screen.dart, the login_screen.dart, and the registration_screen.dart to use the ```RoundedButton```. *Hint*: Leave the code inside the callback for the button's ```onPressed``` on the login and registration screen blank (for now). 

### Part 2:

The ```TextField``` for entering the email (and password) is heavily styled by the ```decoration``` property. Let's extract the code for the ```InputDecoration``` and add it to the ```constants.dart``` file instead. There the decoration can sit alongside its friends which will also further simplify our ```registration_screen.dart``` and ```login_screen.dart```.  

* In the ```constants.dart``` create a new ```const``` called ```kTextFieldDecoration```. Set this constant equal to the ```InputDecoration``` used to style the email and password fields. 

* Make use of the ```kTextFieldDecoration``` on the ```registration_screen.dart``` and ```login_screen.dart```.

*Hint*: Vary the ```hintText``` using ```.copyWith()```. 
