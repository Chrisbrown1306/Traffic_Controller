# Traffic_Controller

## 🎯 Objective

To design and simulate a traffic light controller that:
- Cycles through predefined light sequences for different roads.
- Uses a synchronous FSM with multiple timing states.
- Responds to reset input to return to initial state.
- Can be synthesized and optionally implemented on FPGA hardware.


## 🧠 Features

- ✅ **6-State FSM** controlling traffic lights for:
  - Main Road 1 (M1)
  - Main Road 2 (M2)
  - Side Road (S)
  - Turning Lane (MT)
- ✅ Configurable timing for each state (7s, 5s, 3s, 2s durations)
- ✅ Synchronous counter-based state transitions
- ✅ Synthesizable and simulation-ready
- ✅ Clean waveform generation for analysis


## 🛠️ Tools & Tech

- **Language**: Verilog HDL
- **Simulation & Synthesis**: Xilinx Vivado (tested on version 2020.2+)
- **Optional Hardware**: Xilinx Basys 3 / Nexys A7 / any FPGA board
- **Time Units**: `1ns / 1ps`


## ▶️ How to Simulate

1. **Open Vivado**
2. Create a new project → Add existing `Traffic_Light_Controller.v` and `Traffic_Light_Controller_TB.v`
3. Set `Traffic_Light_Controller_TB` as simulation top
4. Run behavioral simulation
5. Observe waveform:
   - Light outputs: `light_M1`, `light_M2`, `light_MT`, `light_S`
   - Clock (`clk`) and reset (`rst`) behavior

## 🔧 How to Synthesize

1. Open the Vivado project
2. Set `Traffic_Light_Controller` as **Top Module**
3. Run **Synthesis**
4. Click **"Open Synthesized Design"**
5. Navigate to **Tools → Schematic** to view the FSM structure



## 🚀 Future Improvements

- Add pedestrian crossing logic
- Support for sensor-based input (smart traffic)
- Timing configuration via inputs or registers
- Real FPGA implementation with onboard LEDs

## 📚 Credits

Project by: Om Naik
Tools used: Xilinx Vivado, Verilog HDL


## 📌 License

This project is open-source and available under the MIT License.
