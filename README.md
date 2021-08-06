# LambdaGUIConnectionMac

Download global connect:

https://netaccess.utc.edu/vpn/

Connect using UTC ID and password.

Download XQuartz:

https://www.xquartz.org/

Once XQuartz is install it should work with any terminal window.

Connect to lambda server using ssh login credentatils but add -Y command. Ex:

ssh -Y login

verify using xeyes command.

# Non GUI Jupyter access

ssh into lambda like normal and run:

jupyter lab --no-browser --port=XXXX --working-dir /

Open a new terminal window and run the following to open a port from Lambda to your local computer (XXXX from the one you set YYYY to the new port on your computer):

ssh -N -f -L localhost:XXXX:localhost:YYYY user@ecs323lambda.research.utc.edu

Then login on your browser:

localhost:YYYY

if you copy the token from the original /lab?token=ZZZZ you won't have to create a new token and password.
