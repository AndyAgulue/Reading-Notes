# Android Tasks and the Back Stack

A task is a collective of activities that users interact with when performing a certain job.

The actvities are arranged in a stack-the back stack- in the order in which each activity is opened. 

When apps are running simutaneously in a multi-windowed environment, supported in Android 7.0(API 24) and higher, the system manages tasks separately for each window, each window may have multiple tasks. 

The device Home screen is the strating place for most tasks. When the user touches an icon in the app launcher, that appp's task comes to the foreground. If no task exists for the app, then a new task is created and the main activity for that app opens as the root activity in the stack.

When the current activity starts another, the new activity is pushed on the top of the stack and takes focus. The previous activity remanins in the stack, but is stopped. When an activity stops, the system retains the current state of it's user interface. When the user presses the back button, the current activity is popped from the top of the stack and the previous activity resumes. Activities in the stack are never rearranged, only pushed and popped from the stack, pushed onto the stack when started by the current activity and popped off when the user leaves it using the back button. As such the back stack operates as a "last in, first out" object structure. 