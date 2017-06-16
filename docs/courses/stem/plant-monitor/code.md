# Code

Have you ever tried to making your plant to be interacative? Let's try making a soil moisture sensor!

Soil moisture sensors work by measuring the level of current flowing between two electrodes immersed in soil. Students can investigate and develop their own
moisture sensor using common materials such as aluminium foil, metal roads, insulating tape, foam blocks, insulated wire etc. They can be tested before use by
attaching a bulb and cell, checking that the bulb lights up when the electrodes are inserted into damp soil.



The moisture sensor is then attached
to the micro:bit edge connector with
crocodile clips. 

### Experiment 1:

In Experiment 1, The first step is to create the `forever` loop for to test the current oof the pin.

```blocks
basic.forever(() => {

})

```

Next, we want to read the current from Pin 0. So we want to set the current to the `analog read pin P0`.


```blocks
let current = 0
basic.forever(() => {
    current = pins.analogReadPin(AnalogPin.P0)
})

```

We want to visualize the read pin from the current to show the amount of current from the soil to the pin. The best way to visualize this activity is with the `plot bar graph`. Modify your code so that your code looks like this.


```blocks
let current = 0
basic.forever(() => {
    current = pins.analogReadPin(AnalogPin.P0)
    led.plotBarGraph(
    current,
    0
    )
})

```

### Experiment 2: 

In Experiment 2, we will continue building on the visualization of the current senstivity with show icon that reflect the current from the soil. In this experiement, we will use a condition to test the moisture of the soil.  


We to receive an icon that reflect the current from the soil. In this experiement, we will use a condition to test the moisture of the soil. Let's add a `forever` loop that will constantly take the current read pin.


```blocks

basic.forever(() => {
   
})

```


Next, we want to read the current from Pin 0. So we want to set the variable to current and return the current as a number on the `analog read pin P0`.


```blocks
let current = 0
basic.forever(() => {
    current = pins.analogReadPin(AnalogPin.P0)
})

```


We want to set two conditions to determine the current from Pin 0. We will set the variable to current and the variable `current` will be a number from the `analog read pin P0`. The first condition for current less than 100 and the second condition is for current to be greater than 900.


```blocks
let current = 0
basic.forever(() => {
    current = pins.analogReadPin(AnalogPin.P0)
    if (current < 100) {
    	
    } else if (current > 900) {
    	
    } else {
    	
    }
})
```

Now, we have two conditions to determine the current in the soil. We  want to add `set icon` to visualize when the current is not enough or if too high. We will add `set icon` to provide feedback from the soil. In the first condition, the current is less than 100. So the `show icon` will display a `sad` expression. In the second condition, the current is greater than 900, so the `show icon` will display a `happy` expression. If the current is not satifying either conditions, then the `show icon` will display a `confused` expression.


```blocks
let current = 0
basic.forever(() => {
    current = pins.analogReadPin(AnalogPin.P0)
    if (current < 100) {
        basic.showIcon(IconNames.Sad)
    } else if (current > 900) {
        basic.showIcon(IconNames.Happy)
    } else {
        basic.showIcon(IconNames.Confused)
    }
})
```

We want to 


The code for the radio dashboard activity is available here

Go to https://makecode.microbit.org/examples/radio-dashboard.

* click *Download* to see if the code works as expected.