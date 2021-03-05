# Culled from a "Free Education For Everyone" class
- Andrei Neagoie

- INTRODUCTION:
    - What does this mean? And how can one succeed? 
    - This isn't a sprint, it's a marathon. And there is a pyramid of knowledge involved.

- FOUNDATION:
    - How JavaScript works:
    - JAVASCRIPT ENGINE: An "intrepreted" single-threaded language that uses callback functions. (ECMAScript engine.)
        - e.g.: Google Maps: Needed power. So Chrome V8 is an open-sourced JavaScript engine. 2008.
        - Who created the very first JavaScript engine? Brendan Eich (Netscape.) SpiderMonkey. (Firefox still uses.)
        - Inside the engine: Written in C++. ECMAScript is the governing body of JavaScript.
        - Interpreter: Translate and read the file line by line.
        - Compiler: Works ahead of time and compiles down to a machine-understood language. A lower-level language.
        - All languages need to be both interpreted (bytecode) and translated into something low-level (machine code.)
        - JavaScript can *run* in both. Bytecode is not understood without an engine.
        - Is JavaScript an interpreted language? Compilers are used to optimize the code. It depends upon the implementation.
        - Things to watch out for when working with a JavaScript engine. (Poor for optimizations:)
            - eval()
            - arguments
            - for in
            - with
            - delete
            - Inline caching. Code that repeats a method may cache key/value pairs.
            ```javascript
                function findUser(user) {
                    return `found ${user.firstName} ${user.lastName}`
                }
                const userData {
                    firstName: 'Johnson', lastName: 'Junior'
                }
            ```
            - Hidden classes. Different orders create two different things. Assign all properties in the constructor, or add properties and their values in the same order.
            ```javascript
                function Animal(x, y) {
                    this.x = x; this.y = y;
                }
                const obj1 = new Animal(1,2);
                const obj2 = new Animal(3,4);

                obj1.a = 30;
                obj1.b = 100;
                obj2.b = 100;
                obj2.a = 30;
            ```
        - Webassembly. History: Compiled code for the Website. Compling on browser or the browsers agree on some binary executable format.
        - Standard binary executable format.
        - Call stack and memory heap. Important and foundational.
        - Memory. (Memory heap.) Storing and writing information. Allocation, using, and releasing memory. Unordered.
        - Where are we in the code? Run in order. FIFO.
