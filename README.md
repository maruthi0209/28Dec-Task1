1. What will the output of the following code snippet be?
async function test() {
    return "Hello";
}
console.log(test());
Answer : C
a)	Hello

b)	undefined

c)	Promise {: “Hello”}

d)	Error
________________________________________
2. Which of the following correctly invokes an async function?
async function fetchData() {
    return "Data";
}
Answer : D
a)	fetchData();

b)	await fetchData();

c)	fetchData().then();

d)	Both a and c
________________________________________
3. What is the output of the following code?
async function getNumber() {
    return 42;
}
console.log(await getNumber());
Answer : C
a)	42

b)	undefined

c)	SyntaxError

d)	Promise {: 42}
________________________________________
4. What will happen if await is used outside an async function?
const data = await fetch("https://example.com");
Answer : A
a)	SyntaxError

b)	Promise is returned

c)	Works normally

d)	ReferenceError
________________________________________
5. Which of the following is true about async functions?
Answer : A
a) They always return a Promise
b) They can only be used with await
c) They block the main thread
d) They cannot throw errors
________________________________________
6. What does await do in an async function?
Answer : D
a) Waits for the promise to resolve or reject
b) Converts a Promise to synchronous behavior
c) Blocks the main thread until completion
d) Both a and b
________________________________________
7. What is the output of the following code?
async function example() {
    return await 10;
}
example().then(console.log);
Answer : A
a)	10

b)	undefined

c)	Error

d)	Promise {: 10}
________________________________________
8. What happens when an error occurs inside an async function?
async function errorFunction() {
    throw new Error("Oops!");
}
errorFunction().catch(console.log);
Answer : B
a)	The program crashes

b)	Error is returned as a rejected Promise

c)	Error is ignored

d)	Undefined behavior
________________________________________
9. What is the output of the following code?
async function delayedLog() {
    console.log("Before delay");
    await new Promise(resolve => setTimeout(resolve, 1000));
    console.log("After delay");
}
delayedLog();
Answer : B
a)	Before delay, After delay (simultaneously)

b)	Before delay (immediately), After delay (after 1 second)

c)	Before delay, After delay

d)	After delay, Before delay
________________________________________
10. How can you handle a rejected Promise in an async function?
Answer : B
a) Using try-catch
b) Using .catch()
c) Using Promise.resolve()
d) Both a and b
________________________________________
11. What is the output of this code?
async function fetchData() {
    return Promise.resolve("Done");
}
const result = await fetchData();
console.log(result);
Answer : D
a)	Done

b)	Promise {: “Done”}

c)	undefined

d)	Error
________________________________________
12. What will this code output?
async function main() {
    console.log(await Promise.resolve("Resolved!"));
}
main();
Answer : D
a)	Resolved!

b)	undefined

c)	Error

d)	Promise {: “Resolved!”}
________________________________________
13. How does await handle rejected Promises by default?
Answer : D
a) Logs the error
b) Throws an exception
c) Converts it to undefined
d) Returns the rejected Promise
________________________________________
14. What is the output of this code?
async function test() {
    console.log("1");
    await null;
    console.log("2");
}
test();
console.log("3");
Answer : C
a)	1, 2, 3

b)	1, 3, 2

c)	3, 1, 2

d)	1, 2, undefined
________________________________________
15. What happens when await is used with a non-Promise value?
Answer : B
a) Converts it into a resolved Promise
b) Throws a TypeError
c) Skips the line
d) Returns undefined
________________________________________
16. What is the output of the following code?
async function sequence() {
    console.log("Start");
    await new Promise(resolve => setTimeout(resolve, 1000));
    console.log("End");
}
sequence();
console.log("Outside");
Answer : C
a)	Start, Outside, End

b)	Start, End, Outside

c)	Outside, Start, End

d)	End, Start, Outside
________________________________________
17. How do you return multiple resolved values from an async function?
Answer: A
a) Use an array
b) Use an object
c) Chain Promises
d) All of the above
________________________________________
18. Which is true about chaining Promises with async functions?
Answer : D
a) .then can still be used
b) .catch must be used for error handling
c) await removes the need for .then
d) All of the above
________________________________________
19. What is the behavior of await when used with a Promise that never resolves?
Answer : A
a) Blocks forever
b) Throws an error
c) Returns undefined
d) Causes a memory leak
________________________________________
20. What is the result of calling await on a resolved Promise in a try block?
async function main() {
    try {
        const result = await Promise.resolve("Success");
        console.log(result);
    } catch (error) {
        console.log(error);
    }
}
main();
Answer : A
a)	Success

b)	undefined

c)	Error: Unhandled Promise Rejection

d)	SyntaxError
