#  Introduction

This lab will introduce you to Pulse Width Modulation (PWM) using the Arduino. 

> The primary tool for this project will be TinkerCad -> https://www.tinkercad.com

This project follows on from the lecture  **Analogue Write with Arduino** and is designed to put into practice the theory. You will control the brightness of an LED using PWM pins on the Arudino Uno by using the `analogWrite()` function and view the voltage and PWM value in the serial monitor using the `Serial.print()` and `Serial.println()` functions. 

## Setting up the Circuit

Once loaded login to TinkerCad and then click on **Circuits** > **Create new Circuit**.

Change the circuit name, located top-left hand side of the screen to `PWM_ LED`, see image below.


<div align=center>

![](./figures/step1.png)

</div>

Next you need to add an Arduino Uno and a breadboard that need to be connected together from the 5V and GND pins of the Arduino to the power and ground rails of the breadboard. 

This can be achieved by either selecting the Arduino Uno and the breadboard from **Components** > **Basic** components or by changing **Components** > **Basic** to **Components** > **Starter** and choosing Arduino Uno and the Breadboard starter. Please refer to image below.

<div align=center>

![](../MotorController/figures/step3-1.png)

</div>

If you have chosen the Arduino and breadboard template from the the **Components** > **Starter** then these two components are already connected with a corresponding red 5V line and GND line.

- 1 x LED, any colour
- 1 x Potentiometer, set at \\(10k\Omega\\) or \\(10000\Omega\\)
- 1 x resistor, set at \\(0.22k\Omega\\) or \\(220\Omega\\)

Placing components (refer to the image below the steps):

1. Place the LED so that the **cathode** and **anode** is in row **18** and **19** column **e** respectively.
2. Place the resistor's **terminal 2** in row**18** column**b** and **terminal 1** in the GND rail
3. connect a wire from row **19** column **d** to the PWM pin \textasciitilde6 in the Arduino Uno
4. Place the potentiometer so that **Terminal 1**, **Wiper** and **Terminal 2** are in row**26**,**27** and**28** column **e** respectively.
5. Wire up the potentiometer so that terminal **1** and **2** are in GND and 5V line of the breadboard. then take the Wiper to **A0** of Arduino Uno. 

*Note the wires are placed in row **26**, **28** and **27** column **d** respectively.*

<div align=center>

![](figures/step2.png)

</div>

## Programming the Circuit

```C++
void setup()
{

}

void loop()
{

}
```

Now you are ready to set up all the Sketch up as follows:

```C++
int ledPin = 6;      // LED connected to digital pin 6
int analogPin = A0;   // potentiometer connected to analog pin A0
int val = 0;         // variable to store the read value

void setup() {
  pinMode(ledPin, OUTPUT);  // sets the pin as output
}

void loop() {
   val = analogRead(analogPin);  // read the input pin
   analogWrite(ledPin, val / 4); 
}

```

> TODO
>
> - Can lines 1 to 3 be refactored so that the variables are declared and initialised on 1 line? Refactor the code to test your answer.
>
> - Looking inside the `void setup()` only the `ledPin` has had its mode changed to `OUTPUT`. Do we need to need to specify the `pinMode` for the variable `analogPin`? Test your theory by adapting the code.
>
> - What is the purpose of the mathematical operation in line 11? Recall what `analogRead` returns and how `analogWrite` operates. Add comment to the the line 11 to briefly describe the code.
>
> - Describe the relationship between the LED and the resistor based on your observation of your circuit.

## Further Programming

In order to see what is happening numerically with the circuit you will need to send the data to the serial monitor: 

1.  Create a new variable called `PWM` as an interger data type
2.  Adjust the code so that `void setup()` includes the command `Serial.begin(9600);`
3.  Make a new line after the `val = analogRead` in `void loop()` and write `PWM = val \ 4;`
4.  Next replace `analogWrite(ledPin, val \ 4);` with `analogWrite(ledPin, PWM);`
5.  Then finally, modify the code inside the `void loop()`  to produce an output similar to below with a delay of 500*ms*.

<div align=center>

![](./figures/step4.png)

</div>

Now that you have the PWM outputting to the Serial monitor. 

> QUESTIONS:
> 
> - What is the voltage when PWM is 0, 51, 102, 153, 204 and 255? Use the the calculation:
> 
>  \\[ V = \frac{PWM}{51}\\]
>
> - Use a multimeter to measure the voltage out of the pin ~ when the PWM is 51, 102, 153, 204 and 255, why is the multimeter value different to your calculations?

Now adjust the code to output the calculated voltage to the Serial Monitor:

 - Add `float voltage = 0;` to your list of variables at the top of the sketch.
- After the `PWM = val /4;` add `voltage = PWM / 51.0;` to a new line
- Output the voltage to the Serial monitor.