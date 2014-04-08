jQuery standbyTimer
===================

jQuery standbyTimer is a little jquery plugin that gives you a complete timer for your applications.
It initializes a timer when clicking on a page element.
If a click has been detected before the end of the timer, it will execute a function you can specify.
If no click has been detected, the timer will naturally restart without any further actions, and will be ready for a new click events.
You can stop the timer (clear interval).

1) Examples - How to get it work?
---------------------------------

Simple example, when you click on the body, it inits a 10s timer with an interval of 1s. The timer will execute endlessly.

    $.standbyTimer('body', {timer: 10, interval: 1000} );


Here, when you click on the body, it inits a 10s timer with an interval of 1s, that will execute test() function  at the end of the timer.
At the end of the first cycle, standbyTimer will listen for a click event to repeat the operation.

    function test() {
        alert('Simple test!');
    }

    $.standbyTimer('body', {timer: 10, interval: 1000, action: test} );


Here, we will do a 10s timer with an interval of 1s, that will stop at the first cycle and executes test() function.
No more action will be done.

    function test() {
        alert('Simple test!');
    }

    $.standbyTimer('body', {timer: 10, interval: 1000, stop: true, action: test} );


standbyTimer has been tested under and will work for further Jquery 2.1.0.

Enjoy!