# RxJs In Action - Reactive Extensions for JavaScript

[“An API for asynchronous programming with observable streams”](http://reactivex.io/)


###javascript Closure

- [w3schools js closures](http://www.w3schools.com/js/js_function_closures.asp)

Closure example:

    var add = (function () {
        var counter = 0;
        return function () {return counter += 1;}
    })();
    add();
    add();
    add();
    // the counter is now 3


### JavaScript Promises support and Polyfill

from p 11

    makeHttpCall('<host1>/transactions')
    .then(item => makeHttpCall(`<host2>/data/${item.getId()}/info`))
    .then(dataInfo => makeHttpCall(`<host3>/data/files/${dataInfo.files}`))
    .then(processFiles);

- [JavaScript Promises support and Polyfill](http://www.javascriptkit.com/javatutors/javascriptpromises.shtml)

### 1.4.1 Thinking in streams: data flows & propagation

>__Array extras__
>JavaScript ES5 introduced new Array methods, known as the “Array extras,” which enable some level of native support
>for functional programming. These include map, reduce, filter, some, every, and others.

