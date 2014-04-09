jQuery standbyTimer
===================

jQuery standbyTimer is a little jquery plugin that gives you a timer that will reset your application within a specific time.
It initializes a timer when clicking on a page element.
If a click has been detected before the end of the timer, it will execute a function you can specify.
If no click has been detected, the timer will naturally restart without any further actions, and will be ready for a new click events.
You can stop the timer (clear interval).

1) Examples - How to get it work?
---------------------------------

Simple example, when you click on the body, a 10s timer with a 1s interval will be initialized.
The plugin will work endlessly.

    $.standbyTimer('body', {timer: 10, interval: 1000} );


Timer with a callback function.
At the end of the cycle, if a click has been detected within specified time, a callback function will be executed.
If no clicks has been detected within the time, the callback function will be ignored. 

    $.standbyTimer('body', {timer: 10, interval: 1000, onComplete: function(){
        alert('Timer has ended!');
    }} );


Stop the timer at the end of a cycle.

    $.standbyTimer('body', {timer: 10, interval: 1000, stop: true} );


Enable debug mode for developers.

    $.standbyTimer('body', {timer: 10, interval: 1000, debug: true} );


standbyTimer has been tested under and will work for further Jquery 2.1.0.

For contacts:
edouard.kombo@gmail.com
@edouardkombo on Twitter.

Enjoy!