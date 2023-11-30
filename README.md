# Develop-a-countdown-timer-Create-a-countdown-timer-that-counts-down-TASK-3

Create a countdown timer that counts downfrom a set time to zero, with options to stop,reset, and restart the timer.

#CODE:

INDEX.HTML
```
<!DOCTYPE html>
<html lang="en">

  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css">
    <title>Stopwatch</title>
  </head>
  <body>
    <div class="container">
      <h1>Stopwatch</h1>
      <p class="time">
        <span id="minutes">00</span>:<span id="seconds">00</span>:<span
          id="tens"
          >00</span
        >
      </p>
      <button id="start">Start</button>
      <button id="stop">Stop</button>
      <button id="reset">Reset</button>
    </div>

  <script src="script.js"></script>
</body>
</html>
```
STYLE.CSS:

```

* {
    margin: 0;
    padding: 0;
  }
  body {
    width: 100%;
    height: 100vh;
    background-image: url('https://images.unsplash.com/photo-1531512073830-ba890ca4eba2?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=3374&q=80');
    background-position: center;
    background-size: cover;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    
  }

  .container {
    padding: 1rem;
    max-width: 300px;
    text-align: center;
    position: relative;
    border-radius: 10px;
    background-color: rgba(0, 0, 0, 0.6);
  }

  .time {
    padding: 1rem 0;
    font-size: 2rem;
  }

  h1,
  p {
    color: #f8f8f8;
  }

  button {
    padding: 0.4rem 1rem;
    margin: 0 0.2rem;
    border-radius: 10px;
    border: 1px solid #f8f8f8;
  }

  button:hover {
    background-color: rgba(0, 0, 0, 0.4);
    color: #f8f8f8;
  }
```
SCRIPT.JS:
```
window.onload = function () {
    let minutes = 0;
    let seconds = 0;
    let tens = 0;
    let appendMinutes = document.querySelector('#minutes');
    let appendTens = document.querySelector('#tens');
    let appendSeconds = document.querySelector('#seconds');
    let startBtn = document.querySelector('#start');
    let stopBtn = document.querySelector('#stop');
    let resetBtn = document.querySelector('#reset');
    let Interval;

    const startTimer = () => {
      tens++;
      if (tens <= 9) {
        appendTens.innerHTML = '0' + tens;
      }
      if (tens > 9) {
        appendTens.innerHTML = tens;
      }

      if (tens > 99) {
        seconds++;
        appendSeconds.innerHTML = '0' + seconds;
        tens = 0;
        appendTens.innerHTML = '0' + 0;
      }

      if (seconds > 9) {
        appendSeconds.innerHTML = seconds;
      }

      if (seconds > 59) {
        minutes++;
        appendMinutes.innerHTML = '0' + minutes;
        seconds = 0;
        appendSeconds.innerHTML = '0' + 0;
      }
    };

    startBtn.onclick = () => {
      clearInterval(Interval);
      Interval = setInterval(startTimer, 10);
    };

    stopBtn.onclick = () => {
      clearInterval(Interval);
    };

    resetBtn.onclick = () => {
      clearInterval(Interval);
      tens = '00';
      seconds = '00';
      minutes = '00';
      appendTens.innerHTML = tens;
      appendSeconds.innerHTML = seconds;
      appendMinutes.innerHMTL = minutes;
    };
  };
```

#OUTPUT:

![image](https://github.com/ssnithyaasri/Develop-a-countdown-timer-Create-a-countdown-timer-that-counts-down-TASK-3/assets/119122478/254d5f7b-1a34-4f83-b5a1-eaafee29c83c)


![image](https://github.com/ssnithyaasri/Develop-a-countdown-timer-Create-a-countdown-timer-that-counts-down-TASK-3/assets/119122478/c35e5707-b1e4-4fd5-8fdc-78d365a247c9)


![Uploading image.png…]()



