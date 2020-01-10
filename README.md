# Industrial-Gate-Operation
PLC logic to open an industrial gate with a either a pushbutton or a prox sensor andclose the gate with a timer and a prox sensor OR by pushbutton (prox sensor),This PLC has one output module (1756-OB8) and one input module (1756-IB16I).
## I/O
Local:1:O.Data.0 is your output that will activates the motor to open the gate,
Local:1:O.Data.1 is your output that will activates the motor to close the gate,
Local:2:I.Data.3 is the input that will tell you when the gate has reached the fully closedposition,
Local:2:I.Data.2 is the input that will tell you when the gate has reached the fully openposition,
Local:2:I.Data.0 is the input that will tell you when someone is at the gate waiting,
Local:2:I.Data.1 is the input that will tell you when there is something in the path of theopen gate.
### Process
Open the gate with the pushbutton on the attached HMI application.
The open button inthe HMI application has been configured to turn on a tag named: Open_Gate_HMI_PB.
Close the gate with the pushbutton on the attached HMI application. 
The close button inthe HMI application has been configured to turn on a tag named: Close_Gate_HMI_PB.
Be sure to turn off the gate closing motor as soon as the gate shows it is fully closed OR  if the closing motor has been running for more than 30 seconds.
Be sure to turn off the gate opening motor as soon as the gate shows it is fully open ORif if the closing motor has been running for more than 30 seconds.
Make sure the closing and opening motors are never on at the same time.
Make sure the gate cannot be closed if the proximity switch for the gate path showssomething in the way (input is on).
Also, allow the gate to be opened automatically if a car is waiting at the gate (proximityswitch at gate entrance is on).
