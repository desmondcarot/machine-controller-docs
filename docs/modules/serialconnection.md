# SerialConnection
The `SerialConnection` class manages communication between a serial device (e.g. The Machine) and a camera interface `CameraRepo`. It allows asynchronous sending of custom command sequences over a serial port and can trigger image captures from an attached camera. This class ensures thread-safe interactions using an asyncio.Lock, handles connection recovery in case of failure, and provides logging for all major actions.


---
# Commands
The Commands class represents a single instruction to be sent to a machine via serial communication. It is used to encode positional movements and special actions, such as triggering a camera capture.

Each instance contains:

- positionX, positionY, positionZ: Axis movement values.
- sleep: Delay (in seconds) to wait after executing the command.
- capture: If True, the command triggers an image capture instead of movement.

The class automatically encodes the instruction into a byte string (command_byte) for transmission over a serial connection.