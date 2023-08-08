# Prerequisites

## Exceptions and Error Handling

[Exception handling statements](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#exception_handling_statements)

## Callbacks Links

- [Asynchronous](https://developer.mozilla.org/en-US/docs/Glossary/Asynchronous)
- [Callback function](https://developer.mozilla.org/en-US/docs/Glossary/Callback_function)
- [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)
- [Using Promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises)
- [Async function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function)

## Error Handling Example

```js
        // try... catch... finally example
        function getMonthName(mo) {
            mo--; // Adjust month number for array index (so that 0 = Jan, 11 = Dec)
            const months = [
                "Jan", "Feb", "Mar", "Apr", "May", "Jun",
                "Jul", "Aug", "Sep", "Oct", "Nov", "Dec",
            ];
            if (months[mo]) {
                return months[mo];
            } else {
                throw new Error("InvalidMonthNo"); // throw keyword is used here
            }
        }

        try {
            // statements to try
            monthName = getMonthName(1); // function could throw exception
        } catch (e) {
            monthName = "unknown";
            console.error(e); // pass exception object to error handler (i.e. your own function)
        } finally {
            // console.log(monthName);
        }
        // console.log("after try catch");
```

## Callback Functions Example, including Promises and async... await

```js
        // callbacks examples
        let value = 1;

        function receiver() {
            console.log("Call received")
            value = 2;
            console.log("Call caller back");
            console.log("Call ended");
            console.log(value);
        }

        // doSomething();

        function caller(callback) {
            console.log("Call started");
            callback();
            console.log(value);
        }

        setTimeout(() => { caller(receiver) }, 2000);

        console.log(value);

        function fetchPromise(api) {
            fetch(api)
                .then(res => res.json())
                .then(data => {
                    console.log(data);
                })
        }

        fetchPromise('https://api.sampleapis.com/avatar/info');

        async function fetchAsync(api) {
            const response = await fetch(api);
            const data = await response.json();
            console.log(data);
        }

        fetchAsync('https://api.sampleapis.com/avatar/info');
```