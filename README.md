# DualSense.js
A library to use the DualSense on the web.

Not finished yet, doc coming soon.

[Dualsense tester](https://nougator.github.io/Dualsense-Tester/)

## Features:
  - [x] USB
  - [ ] Bluetooth (Might be work but never tested)
  - [x] Inputs
  - [x] Adaptive triggers
  - [ ] Haptic feedbacks (should check if it's possible)
  - [x] Color LED
  - [x] Mute mic LED
  - [x] Player LEDs
  - [x] Doc

## Examples:

```js
let ds = new Duelsensejs();

function i(){
    ds.init();
    
    setColor(0, 0, 255);
    setMicLed(ds.micLedState.pulse);
    if(ds.state.triangle){
        ds.setTrigger(triggerState);
    }
    triggerState = {
        selectedTrigger: ds.trigger.both,
        mode: 0x02,
        forces: [100, 255, 0, 0, 0, 0]
    }
}
```
