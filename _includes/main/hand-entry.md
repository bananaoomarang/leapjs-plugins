# Hand Entry
-----------
<a class="view-source" href="https://github.com/leapmotion/leapjs-plugins/tree/master/main/hand-entry" target="_blank">View Source</a>

## Usage

Fires controller events when a hand enters or leaves the frame.

```js
  controller.use('handEntry')
```

```js
Leap.loop(function(frame){
})
.use('handEntry')
.on('handFound', function(hand){
   // ...
});
```


## Events

### handFound(hand)

Triggered from the controller.  This passes in the Hand object.

```js
  controller.on('handFound',
    function(hand){console.log( 'hand found', hand ); }
  )
```

### handLost(hand)

Triggered from the controller.  This passes in the Hand *as it was seen in the last frame*.

This event is also triggered for every hand present when the device is disconnected.

```js
  controller.on('handLost',
    function(hand){console.log( 'hand lost', hand ); }
  )
```

