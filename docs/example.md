# Examples

Below are the examples to set up machines / and perform some action to help you get a feel of what the program is used.

1. Start with initializing MachineController

```python title="main.py"
from MachineController import MachineController

controller = MachineController()

```

2. create instance of connection for the new machine


Create new CameraRepo instance

```python title="CameraRepo"
from MachineController import CameraRepo
 
cam_index = 0
cam_repo = Camera(cam_index)


```
Create new Serial Connection instance

```python title="SerialConnection"
from MachineController import SerialConnection

serial = Serial('COM4',93400)
connection = SerialConnection(serial, cam_repo)

```
>Use MachineController.list_available_ports() and list_available_cameras() to find availalbe ports.


3. Now intialize a new Machine within for the MachineController:

```python title="Machine"
from MachineController import Machine

id=1 #the machine identifier
controller.machines.append(Machine(connection,id,cam_index))

```

or you can skip step 2 and just init with

```python title="Machine"
from MachineController import Machine

id=1 #the machine identifier
controller.machines.append()

```

4. We can now call MachineController to perform task on the machine like:

```python title="MachineController"

await controller.test_machine(id)
await controller.click_machine(id)

```

