#Computer #Engineering 

Node.js is a [[cross-platform]], [[open-source]] [[server]] environment that can run on [[Windows]], [[Linux]], [[Unix]], [[macOS]], and more. Node.js is a [[back-end]] [[JavaScript]] runtime environment, runs on the V8 JavaScript Engine, and executes JavaScript code outside a [[web]] browser.

Node.js is similar in design to, and influenced by, systems like Ruby's Event Machine and Python's Twisted. Node.js takes the event model a bit further. It presents an event loop as a runtime construct instead of as a library. In other systems, there is always a blocking call to start the event-loop. Typically, behavior is defined through callbacks at the beginning of a script, and at the end a server is started through a blocking call like EventMachine::run(). In Node.js, there is no such start-the-event-loop call. Node.js simply enters the event loop after executing the input script. Node.js exits the event loop when there are no more callbacks to perform. This behavior is like browser JavaScript — the event loop is hidden from the user.

HTTP is a first-class citizen in Node.js, designed with streaming and low latency in mind. This makes Node.js well suited for the foundation of a web library or [[framework]].

Node.js being designed without threads doesn't mean you can't take advantage of multiple cores in your environment. Child processes can be spawned by using our child_process.fork() API, and are designed to be easy to communicate with. Built upon that same interface is the cluster module, which allows you to share sockets between processes to enable load balancing over your cores.


Helpful links: 
https://code.visualstudio.com/docs/nodejs/nodejs-tutorial
[Node.js Ultimate Beginner’s Guide in 7 Easy Steps](https://www.youtube.com/watch?v=ENrzD9HAZK4&ab_channel=Fireship)
