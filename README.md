# Orchestrate-Lambda-Functions-with-Step-Functions
This guide links AWS Lambda Functions together with AWS Step Functions.

### Set up Step functions to orchestrate Lambda functions

1.  Go to Step functions and navigate to State Machine

2.  Then you will have to create a state machine

3.  For the beginning it is easier to design the workflow visually

4.  Depending on use case choose standard/express (I used standard for
    now)

5.  Then you should see the design interface

![Drag necessary actions into Step functions](images/place_lambas.png)

Just add the Invoke Lambda Function Action to the workflow

 

There you can change the state name and leave the rest pretty much how
it is default

The only thing you need to link to the action is the lambda function you
want to invoke

![Set Lambda function](images/set_function.png)

That can be done here, just open the dropdown and select the latest
version of your desired lambda function

 

Repeat this process for all remaining lambda functions you want to
invoke and order them accordingly in the design workflow

 

Should look something like this at the end:

![Final Step functions](images/final_step_functions.png)

Click next

If wanted you can adjust the code displayed now but this step is
completely optional and if you don’t need any changes to be done then
just click next again

 

### Now we specify the settings for the State machine:

Set a name and if not already existing leave the permission to create a
new role, that covers all permissions you need to invoke the lambda
functions

![Specify State machine](images/specify_state_machine.png)

It might also be advisable to turn on Logs by setting the Log level to
what you need.

![Set Log level](images/set_log.png)

For example ALL

 

Then just click create state machine and it should take some seconds
before it is done

 

To start the workflow just click start execution and find the logs below
