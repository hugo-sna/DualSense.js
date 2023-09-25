# DualSense.js
A library to use the DualSense on the web.

Not finished yet, doc coming soon.

[Dualsense tester](https://nougator.github.io/Dualsense-Tester/)

## Features:
  - [x] USB
  - [ ] Bluetooth
  - [x] Inputs
  - [x] Adaptive triggers 
  - [x] Color LED
  - [x] Mute mic LED
  - [x] Player LEDs
  - [x] Doc

## Examples:

```js
let ds = new Duelsensejs();

ds.init();
    
setColor(0, 255, 0); // Set LED's color
setMicLed(ds.micLedState.pulse); // Set mic led button LED state (on, off,, pulse)
setPlayerNumber(4); // Set player number on the controller

if(ds.state.triangle){ // Getting inputs
    ds.setTrigger(triggerState); // Set trigger states from object
}

triggerState = { // Trigger object preset
    selectedTrigger: ds.trigger.both,
    mode: 0x02,
    forces: [100, 255, 0, 0, 0, 0]
};
```
