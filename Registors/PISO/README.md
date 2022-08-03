# PISO
## Parallel-In Parallel-Out Shift Register

- The shift register, which allows parallel input (data is given separately to each flip flop and in a simultaneous manner) and produces a serial output is known as Parallel-In Serial-Out shift register.
- The logic circuit given below shows a parallel-in-parallel-out shift register. The circuit consists of four D flip-flops which are connected. The clear (CLR) signal and clock signals are connected to all the 4 flip flops. In this type of register, there are no interconnections between the individual flip-flops since no serial shifting of the data is required. Data is given as input separately for each flip flop and in the same way, output also collected individually from each flip flop.
- The logic circuit given below shows a parallel-in-serial-out shift register. The circuit consists of four D flip-flops which are connected. The clock input is directly connected to all the flip flops but the input data is connected individually to each flip flop through a multiplexer at the input of every flip flop. The output of the previous flip flop and parallel data input are connected to the input of the MUX and the output of MUX is connected to the next flip flop. All these flip-flops are synchronous with each other since the same clock signal is applied to each flip flop.
- A Parallel in Serial out (PISO) shift register us used to convert parallel data to serial data.

### Circuit Diagram:

![image](https://user-images.githubusercontent.com/100958162/182660542-e48420ee-bead-4139-a3fc-1e832b2bb1e7.png)

#### Thinkercad Circuit:

![image](https://user-images.githubusercontent.com/100958162/182660796-08be72f1-c09f-498d-8fd7-0efaf960b049.png)

<b>
- Components used
</b>

![image](https://user-images.githubusercontent.com/100958162/182660988-2671c417-bfb6-4acd-8bfb-958802e52dda.png)

<a href = "https://www.tinkercad.com/things/hIJ2Lv3GjoD-piso/editel"> <img src ="https://img.shields.io/badge/Thinkercad%20File-PISO%20Shift%20Registor%20-brightgreen" width = 320 align = center> </a>
