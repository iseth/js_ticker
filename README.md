## ticker package

### Examples

This is a countdown timer from 5 secs to 0 out putting the current count
```js
timer({
  timer_type: "count_down",
  timer_max: 5000,
  interval: 1000,
  main_callback: () => {console.log(i + "seconds left")},
  finish_callback: () => {console.log("countdown finished")}
})
```

This is a countup timer from 0 secs to 5 out putting the current count
```js
timer({
  timer_type: "count_up",
  timer_max: 5000,
  interval: 1000,
  main_callback: () => {console.log(i)},
  finish_callback: () => {console.log("finished")}
})
```

API:
```js
timer({
  timer_type: "count_down",
  timer_max: 5000,
  timer_min: 0,
  interval: 1000, // if interval is 0 then interval becomes random between 1000 and 2000 ms
  interval_rand_min: 1000, // interval is ignored if this is and interval_rand_max is used
  interval_rand_max: 1000,
  before_start_callback: first_callback,
  main_callback: main_callback,
  finish_callback: finish_callback
})
```
