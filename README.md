# Oceanic wave altitudes at a specific point using the PM spectrum

## Running on Ortopillar

IP: 192.168.0.160

User: root

Password: gr**l

## How to run the ortopillar:

1. First terminal(real time controller):
```
CFG_CAN=CAN_SUPPORT workframe start && opencan start && console start
```

2. Second terminal(network task):
```
cd modularctrl ./bin/rtai/taskSlimCheckRemoteCtrl
```

3. Third terminal(arm controller):
```
cd modularctrl ./slimcheck startarm
```

4. Then, in the first terminal digit:
```
start
```

## How it works

In the third terminal:
```
arm
```
Then:
```
homing(to set all the joint zeros)
```

To set joint positions/velocities: JVEL/JVELALL and JMOVE/JMOVEALL

### WAVES SOFTWARE:
```
compile the package and run read executable
```

### SETUP FOR ORTOPILLAR:

Initial position for the waves:
```
Current Joint Position: 2.89997 -0.506282 0.441177 -2.10778e-06 4.30798e-05 -3.7192e-06 
```

Final configuration before ends..
```
Current Joint Position: -0.170799 -2.68709 2.64063 -4.21556e-06 4.11217e-05 -7.43841e-06 
```

Hence:
```
disarm 
```
And:
```
shutdown -h now 
```
