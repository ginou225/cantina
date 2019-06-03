# cantina
Code Exercise
For this project I use JQ to parse the json input and store a particular property from the Json into a variable for the output.

In my command promp I send a request to the API using a curl command and pipe the result of that into jq processor to parse the data

curl -s https://raw.githubusercontent.com/jdolan/quetoo/master/src/cgame/default/ui/settings/SystemViewController.json | jq

then I also use JQ to access properties of the result using filters in JQ ‘.’

The first exercise 
1.class - The view class name, e.g. "StackView"
I use the command 
curl -s https://raw.githubusercontent.com/jdolan/quetoo/master/src/cgame/default/ui/settings/SystemViewController.json | jq '.subviews[].class'
to save this into a variable called stackview: is created this command
stackview=$(curl -s https://raw.githubusercontent.com/jdolan/quetoo/master/src/cgame/default/ui/settings/SystemViewController.json | jq '.subviews[].class')
then to call the variable you echo $stackview


2) CSS class names, e.g. ".container"
I use the command

curl -s https://raw.githubusercontent.com/jdolan/quetoo/master/src/cgame/default/ui/settings/SystemViewController.json | jq '.subviews[].classNames[0]'

3)  identifier - The view identifier, e.g. "#videoMode"
I use the command :  curl -s https://raw.githubusercontent.com/jdolan/quetoo/master/src/cgame/default/ui/settings/SystemViewController.json | jq '.subviews[].subviews[].subviews[].identifier'








