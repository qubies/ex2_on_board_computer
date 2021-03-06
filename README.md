# ex2_on_board_computer
Ex-Alta 2 on board computer firmware

### Unit Tests

Tests can be built inside ./Simulator/test/ and include files from ./Simulator/FreeRTOS-Sim/Source as dependancies.
Test framework is Unity, autogenerated using Ceedling.

### Simulator
The simulator is a FreeRTOS POSIX simulator. Use it to simulate tasks in a FreeRTOS environment.
NOTE: the simulator only builds and runs code in a testbed and does not emualte the hardware of EX_ALTA 2.

Example tasks are included in ./Simulator/FreeRTOS-Sim/Demo/*.c
Custom tasks can be added here. 

To create a task modify ./Simulator/FreeRTOS-Sim/Project/main.c to execute your custom task as required.

#### Dependancy:
    Docker && docker-compose are required install from:
    https://docs.docker.com/install/

#### Build Instructions

To build the tests and start the simulation after modifications:
```
docker-compose build
docker run -ti --rm simulator_sim:latest

```
-ti is terminal interactive, without this the simulation will just startup and run in the background without showing output
--rm destroys the container when you close it. 
