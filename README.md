# Rain-detector-with-VSDSquadron-FPGA-Mini
I Have made another Repositry named [VSDSquadron FPGA Mini internship program](https://github.com/Bhavankumar123/VSDSquadron-FPGA-Mini-Internship-program), This is related to the exact same board.

## FPGA Moisture Sensor System — Project Overview
### Objective

To implement a real-time soil moisture detection system using the VSDSquadron FPGA Mini board and control an LED based on moisture presence.

System Overview
 | Component      | Role |
 |------------|----|
 | `Moisture Sensor`  | Detects the presence of moisture in the soil. Outputs digital HIGH (dry) or LOW (wet). |
 | `FPGA Mini Board` | Processes the sensor input and controls an output (LED) based on logic. |
 | `LED`| Visual indicator: Lights up when mosture is detected, off when moisture is not. |

Hardware Components ( If you dont have the components, you can order them here )
- [VSDSquadron FPGA Mini Board](https://www.vlsisystemdesign.com/vsdsquadronfm/)
- [Digital Rain sensor](https://www.amazon.in/Prakti-Raindrops-Detection-weather-Humidity/dp/B0BYXCXLP7/ref=sr_1_2?dib=eyJ2IjoiMSJ9.hIJl3knEHW9Z9T4i7O91fH7tPaV1k0Tq6V6RzMvTe_Xc7iU8g3w_WYKnPkRDFrOtVZEcayr6iQqKcdleHH381oxxPkMEt6NfsONimY-De6IEfmbhVACLIHjFQLBk2SbOIzlp5VnB6_TTUrNqxW_NcEQwZkx-RsDJONzy89cwJN4v764IzYuiYt_A41MsrTXf7QHvXT7MaKkOHlBzYKVa1fk5LYi111RGO9DdamMK_k9lNee_rivSWVl8zq7MPN_iqZlkCoP4Dvu2FxGx85cIMckkAzdYy8h38ZbanBWhsxk.MSWHVrcJUJNan81eWkVcFSVlsDUpnGO7WcZQ6zdexJg&dib_tag=se&keywords=rain+sensor&qid=1745513083&sr=8-2)
- [LED](https:www.amazon.in/UNIVERSAL-HUB-LED-Emitting-Brightness/dp/B0D2NZLDJ8/ref=sr_1_2?crid=28GA9OSXW7ZXJ&dib=eyJ2IjoiMSJ9.jA_9Zlo3oaeGIY7CHPtyRHn6b-ihpDxoVmM-glZu_wkI7Up4BhuGwlNwMuXcqQpq7Z4aOPnPlPa5ywvyQL5NkkU0qSHyPR2cvQFl3ioXrkc.7CWVmqL5jj-Zi7XIis6kM3j7zNLGnDBHHJa1ojCXDts&dib_tag=se&keywords=Electronic+Spices+Color+5mm+Led+Light+white&qid=1745513242&refinements=p_n_pct-off-with-tax%3A27060456031%2Cp_36%3A-6600&rnid=3444809031&s=kitchen&sprefix=electronic+spices+color+5mm+led+light+whit%2Caps%2C250&sr=1-2)
- [Breadboard & Jumper Wires](https://www.amazon.in/ApTechDeals-Breadboard-point-jumper-wires/dp/B07PQS67BN/ref=sr_1_2?crid=3RDCLGVF9K4RJ&dib=eyJ2IjoiMSJ9.QognKaHSijKd0KQrtGvEbx_2ybPDtWcO8UEjm0dh3IzNjsaxoO0cbeLqU1XIrnUxRd1huUCp_mn9FvEznPf2Yo_yl0jqt5oRnnHVo7oTrKIUwjWV6J40BcECmm-SI2EpoDc6S6p8lx4F2s_DZuZyDBoE89k6txSClv4K1fi6EkcVOwDAZSkB-8lzHLsX9vWP9VuEafkCZtp603zF3z9t80XhGL-xgc4T5cv8Oo6nHOvp_koE64g6d9lO5GOKxRlrdLu_-NdBch-2Qnz6Lml5aCG0t12_aeTdzdcJ91eC0iI.MeDpXWG8OBpHQcHRTwa13x0n6uOK3asxeHmsh-kmyBI&dib_tag=se&keywords=Breadboard%2Bwith%2Bjumper%2Bwires&qid=1745513285&s=kitchen&sprefix=breadboard%2Bwith%2Bjumper%2Bwires%2Ckitchen%2C248&sr=1-2&th=1)
- [USB cable (for programming the board)](https://www.amazon.in/Dyazo-Charging-Supports-Compatible-Smartphone/dp/B0DDY5RFM2/ref=sr_1_4?dib=eyJ2IjoiMSJ9.RTtbuuQ1uiUAz7N0sBptI58yZaXsn-0qeUUQYFsFsWkUsB6z6H-Fka3NVlYaHqwvOtQTVj5Xxh9d215jQVEpi9N9aFsdheTW_KHlf9iniKWRpQbw7dxaRts2nYfYpdcHq7jcTUyuiJMYYHXOR772_T6ynimZE2q8vuRm6QwLmqo-8AcT2jIERTf9_pitDbMGH7iSnXEFyj4iL85t9VUxhxZWp3IpXZEC73oBm5PSr43peZ8InEijX1FgTR_hJlzIIDKPGDXealwXLb3kaeO993PZl_8qpjYyOexED--HBJo.eW08YyfK3RbZhY7SBj7_f4LgP6a8XaCE9b3mzN3Poi4&dib_tag=se&keywords=USB%2BCable%2BC&qid=1745513379&refinements=p_36%3A-10000%2Cp_n_pct-off-with-tax%3A27060457031&rnid=1318502031&s=computers&sr=1-4&th=1)

## Needed Files

1. Makefile
2. pins.pcf
3. top.v
4. moisture_sensor.v

## Codes
### 1. Makefile
```bash
# Define variables
TOP_MODULE = top
PCF_FILE = pins.pcf
SRC_FILES = top.v moisture_sensor.v
JSON_FILE = top.json
ASC_FILE = top.asc
BIN_FILE = top.bin

# Synthesize Verilog code with Yosys
synth:
	yosys -p "synth_ice40 -top $(TOP_MODULE) -json $(JSON_FILE)" $(SRC_FILES)

# Place and route with nextpnr
place_and_route:
	nextpnr-ice40 --up5k --package sg48 --json $(JSON_FILE) --pcf $(PCF_FILE) --asc $(ASC_FILE)

# Generate bitstream with icepack
bitstream:
	icepack $(ASC_FILE) $(BIN_FILE)

# Program the FPGA with iceprog
program:
	iceprog $(BIN_FILE)

# Full build process
build: synth place_and_route bitstream

# Clean the generated files
clean:
	rm -f $(JSON_FILE) $(ASC_FILE) $(BIN_FILE)
```

### 2. top.v
```bash
module top(
    input wire moisture_pin,
    output wire led_pin
);

moisture_sensor sensor_inst (
    .moisture_input(moisture_pin),
    .led_output(led_pin)
);

endmodule
```

### 3. moisture_sensor.v
```bash
module moisture_sensor(

    input wire moisture_input,

    output wire led_output

);



assign led_output = ~moisture_input;



endmodule
```

### 4. pins.pcf
```bash
set_io moisture_pin  10   ; Moisture sensor input pin (GPIO Pin 10)
set_io led_pin       6    ; LED output pin (GPIO Pin 6)
```

Post the above codes In a file named Moisture_Sensor in VSDSquadron_FM

then run this in terminal:-
```bash
cd
cd VSDSquadron_FM/Moisture sensor
lsusb
```
You should be able to see something like - 
Future Technology Devices International, Ltd FT232H Single HS USB-UART/FIFO IC

Then run:-
```bash
make clean
make build
sudo make program
```
The moisture sensor is connected to the VSDSquadron FPGA Mini Board through its accompanying digital output module. The module has three pins: VCC, GND, and DO (Digital Output). The VCC pin is connected to the 3.3V (or VCC) pin of the FPGA board, and the GND pin is connected to the FPGA's ground. The DO pin is connected to pin 10 on the FPGA board, which serves as the input signal to the Verilog module (moisture_pin).

An LED is used to indicate the presence or absence of moisture. The anode of the LED is connected to pin 6 on the FPGA board (assigned to led_pin in the code), and the cathode is connected to the ground rail on the breadboard, which in turn is connected to the FPGA’s GND. For safe operation, it's recommended to add a 220Ω resistor in series with the LED to limit the current.

Functionally, when the moule feels moisture, the sensor outputs a  signal HIGH signal (1) on the DO pin, causing the LED to turn on. Conversely, when there is no humidity, the sensor outputs a LOW signal (0), which turns the LED off. This behavior matches the Verilog logic where led_output is directly assigned to the moisture_input signal (assign led_output = ⁓moisture_input;), making the LED light up only in wet conditions.

## Connections
LED +ve - pin 6 on FPGA Mini

LED -ve - GND pin on FPGA Mini

Moisture sensor - Moisture sensor Module ( +ve, -ve doesn't matter )

Moisture sensor module - +ve - 5v on FPGA Mini

Moisture sensor module - -ve - GND on FPGA Mini

Moisture sensor module - DO pin - pin 10 on FPGA Mini

![Image](https://github.com/user-attachments/assets/f2a1311f-454b-437c-a5fe-c5dbf5e2436d)

You connect and upload the code to bring your project to life!!
Happy coding!!
