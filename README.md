# Acing the Technical Interview

The following document includes a list of tips, common interview questions and external resources that might be helpfull when applying to job postions in the Web Development field. It covers both front-end and backend topics.

## Target

The document is targeted at Ironhack Web Development Bootcamp graduates who aim to enter the job market working as Junior Front-end or Backend Developers.

The subjects it touches upon are, for the most part, entirely covered in the bootcamp. Those which are only partially or not at all covered during the bootcamp are signaled.

## General Tips for Interviews

The following tips are based on generalizations, and repeated experimentation with interviewing processes. Each interview process will have its own quirks and will be conducted differently from the others.

### Interview Process

Interview processes are normally conducted in two to four steps, and will rarely be entirely overseen by the same company employee.

The first interview is often designed to filter through the candidate pool. It is usually conducted by a recruiter; that is, someone with a non-technical background.

The second interview is normally a technical interview. The interviewer might be a developer who works as technical lead in the project you aim to work on, or a technical employee whose sole responsibility is to interview potential job candidates.

After a technical interview, some companies will ask a candidate to complete a technical challenge. This technical challenge might be sent as "homework" to be completed in a timeframe ranging from 2 to 7 days. It might also be administered in person with the duration of 1 to 2 hours.

A third and last interview might be conducted by other company stakeholders, such as the company's CEO, a general manager, HR personnel, or development team members to ensure a cultural fit.

### Sitting at an interview

Each of the steps outlined above might be conducted separately or in conjunction with another step, so you should always be ready to sit at an interview for up to 4 hours.

Don’t eat or drink too much before the interview. You don't want to feel unwell during the lenght of the interview.

Wear fresh clothing. Some people will get nervous and sweat.

Take a water bottle with you. It might make you more confortable to have something to hold on to.

If the interview lasts more than two hours, don't feel bad about asking to get up and go to the bathroom, get a glass of water or a coffee.

### Some quick points

- Technical interviews may vary widely between companies/interviewers.
- Some might last 15m, others might last one hour.
- Questions could be more open ended or more exercise driven.
- They can be conducted by one or two people.
- There can be more than one technical interview during an entire recruitment process.
- If you’re getting into consulting, you might get a technical interview at the consulting firm and later at the client.

## Mock Interview Questions

### Programming Paradigms

#### Q: Is JavaScript an object-oriented programming language?

This question is often asked by people with a misinformed view of JavaScript.

JavaScript is a **multi-paradigm language**, meaning that it supports multiple different programming styles, including **event-driven**, **functional** and **object-oriented**.

**Object-Oriented Programming (OOP)** is based around the concept of `objects`. These are data structures that contain data fields, known in JavaScript as `properties`, and procedures, known as `methods`.

Whenever you rely on in-built `methods`, `prototypes` or `classes`, you are essentially using Object-Oriented Programming.

#### Q: Why is it called Object-Oriented?

In *OOP*, everything is considered to be modeled as an object. This abstraction can be taken all the way down to nuts and bolts for a car, or as broad as simply a car type with a year, make, and model.

#### Q: What are some advantages of functional programming?

FP is based around the concept of “pure functions”, which avoid shared state, mutable data and side-effects.
https://www.freecodecamp.org/news/functional-programming-principles-in-javascript-1b8fc6c3563f/

#### Q: What is a pure function?

Given the same inputs, a pure function always returns the same output. It does not have side effects: these are anything, such as logging to the console or modifying an external variable, beyond returning the result.

#### Q: What’s the difference between imperative and declarative programming?

We can also think about the difference between *OOP* and *FP* in terms of the difference between *imperative* and *declarative* programming.

These are umbrella terms that describe shared characteristics between multiple different programming para digms. FP is an example of *declarative* programming, while OOP is an example of *imperative* programming.

In a basic sense, imperative programming is concerned with how you do something. It spells out the steps in the most essential way, and is characterised by for and while loops, if and switch statements, and so on.

```js
const sumArray = array => {
  let result = 0;
  for (let i = 0; i < array.length; i++) result += array[i];
  return result;
};
```

By contrast, declarative programming is concerned with what to do, and it abstracts away the how by relying on expressions. This often results in more concise code, but at scale, it can become more difficult to debug because it’s that much less transparent.

Here’s a declarative approach to our `sumArray()` function, above.

```js
const sumArray = array => {
  return array.reduce((x, y) => x + y);
};
```

## Object-oriented programming

#### Q: What is a class?

Classes are at the core of object-oriented programming. They generalize a type of object, allowing you to instantiate multiple objects that share the same basic properties and methods.

Classes can be extended.

> **External Resource**: [Digital Ocean's guide on JS OOP](https://www.digitalocean.com/community/tutorials/understanding-classes-in-javascript)

#### Q: What is an instance?

It’s an object instantiated from a class.

#### Q: How does inheritance work?

A class can extend another class, and therefore inherit its constructor, properties, methods, statics.

#### Q: Explain Polymorphism?

As one of the tenets of Object Oriented Programming, it is the practice of designing objects to share behaviors and to be able to override shared behaviors with specific ones. Polymorphism takes advantage of inheritance in order to make this happen.

#### Q: Differentiate between composition and inheritence.

Composition gives you more flexibility by composing functionality to create a new object, while inheritance forces you to extend entities in an inheritance tree.

> External Resource: [Composition vs. Inheritance](https://www.vicompany.nl/magazine/composition-over-inheritance-and-javascript)

### Diverse JavaScript Questions

#### Q: Explain immutability

Something mutable is, by definition, liable or subject to change or alteration. We use the word to refer to objects whose state is allowed to change over time. An immutable value is the exact opposite: after it has been created, it can never change.

Values in JavaScript are immutable. Declared variables, objects are, by default, mutable.

```js
var statement = "I am an immutable value";
var otherStr = statement.slice(8, 17);

console.log(statement); // "I am an immutable value"
console.log(otherStr); // "immutable"

statement = otherStr;

console.log(statement); // "immutable"
```

In the example above, the value for the original string stays unchanged. The variable, on the other hand, can be re-assigned.

#### Q: What is a Regular Expression?

**Regular Expressions (RegEX)** are patterns used to match character combinations in strings. In JavaScript, regular expressions are also objects.

These patterns are used with the `exec` and `test` methods of RegExp, and with the `match`, `matchAll`, `replace`, `search`, and `split` methods of `String`.

> External Resource: [Short explanation of RegEx](https://twitter.com/s0md3v/status/1171394403065155584?s=03)

> External Resource: [MDN Reference for Regular Expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)

#### Q: What should I take into account when choosing between writing synchronous or asynchronous code?

Synchronous operations might block the main thread. Asynchronous operations should be built in a way that doesn’t block the main thread.

> **External Resource**: [node.js `fs` module documentation](https://nodejs.org/api/fs.html#fs_fs_readfile_path_options_callback)

#### Q: How Does a Function Expression Differ from a Function Declaration?

Function declarations are hoisted, while function expressions are not. That means function declarations are moved to the top of their scope by the JavaScript interpreter, and so you can define a function declaration and call it anywhere in your code.

By contrast, you can only call a function expression in linear sequence: you have to define it before you call it.

```js
// Function Declaration
sum(1,2);

function sum(x, y) {
  return x + y;
};

// Function Expression: ES5
const sumES5 = function(x, y) {
  return x + y;
};

// Function Expression: ES6+
const sumES6 = (x, y) => x + y;
```

#### Q: What are the data types in JavaScript?

There are several data types defined in JavaScript:

- **Primitive type**: `Boolean`, `Number`, `String`, `Null`, `Undefined`, and as of recently `BigInt` and `Symbol`.
- **Reference type**: `Object`.

#### Q: Is an `Array` a data type?

An `Array` is not a data type. It is one of JS’s built-in global objects. Other global objects include instantiatable classes such as `Date`, `Error`, `Promise`, and useful objects such as `Math`.

`Arrays` are special, in the sense that they have some of their functionality built into the language.

#### Q: What is a closure?

A **closure** encapsulates a portion of code.

A closure is an inner function that has access to the outer (enclosing) function’s variables — scope chain.

The closure has access to three scope chains:

- Access to its own scope (variables defined between its curly brackets).
- Access to the outer function’s variables.
- Access to the global variables.

#### Q: What is a `Promise`? What is their advantage over callbacks?

A `callback` is a pattern, while `promises` have been specified into the language.

A `Promise` is an object that wraps an *asynchronous operation* and *resolves* when it’s done.

Promises can also be used in conjunction with `async`/`await` in order to write asynchronous code in a more synchronous-looking manner.

> External Resource: [Medium article on callbacks vs. promises](https://medium.com/codebuddies/getting-to-know-asynchronous-javascript-callbacks-promises-and-async-await-17e0673281ee)

### APIs

#### Q: What are microservices?

The microservice architecture is an architectural style that structures an application as a collection of small services that are loosely coupled, independently deployable, highly maintainable and testable.

The microservice architecture enables the rapid, frequent and reliable delivery of large, complex applications.

#### Q: Name several patterns for web-service APIs. Which is most commonly used in 2019?

**REST** (or Representational State Transfer) is an architectural pattern that separates content by resources and methods.

**SOAP** (or Simple Object Access Protocol) is a protocol that transfers strictly defined data, structured in the XML format. It was first defined in 1999 and is used in a lot of legacy applications.

**GraphQL** is a data query and manipulation language that offers great flexibility when loading and modifying data. It allows you to load only the data you require. It was developed internally by Facebook in 2012 but released as an open-source standard in 2015. Many think it’s the future of web-service APIs, but it’s still an incomplete spec, with some poor implementations.

#### Q: Enumerate some HTTP methods, and explain their purpose.

**GET**: Retrieve data. Should not have consequences in terms of mutating state or side effects on the server.
**POST**: Used to submit an entity to the specified resource, often causing a change in state or side effects on the server.
**PUT**: Replaces all current representations of the target resource with the request payload.
**PATCH**: Partially updates the target resource.
**DELETE**: Deletes the specified resource.

### Testing

#### Q: Distinguish between unit testing, integration testing and end-to-end testing.

In *unit testing*,  we test each piece of functionality at the smallest practical level and ensure it is working as desired, not relying on external state, services, and not mutating external state or invoking external services.

In *integration testing*, we test how two or more separate pieces of functionality work together.

In *end-to-end* (or e2e) we test an application in its entirety, including the integration with external services.

Google’s engineering guidelines suggests a *70/20/10 split*: 70% unit tests, 20% integration tests, and 10% end-to-end tests.

#### Q: What is test-driven development (TDD)? How does it differ from behaviour-driven development (BDD)?

**Test-driven development (TDD)** is a software development process that relies on the repetition of a very short development cycle: first the developer writes an (initially failing) automated test case that defines a desired improvement or new function, then produces the minimum amount of code to pass that test, and finally refactors the new code to acceptable standards.

**Behaviour-driven development (BDD)** aims to address the shortcomings of *TDD*, by trying to abstract away implementation details and instead focusing in the behaviour of the functionality.

In both **TDD** and **BDD** approaches, tests are written upfront before the actual code is written. Writing tests first helps predict the course of the development, which will ultimately prevent any cases being missed from the code or functionality.

### Programming design patterns

#### Q: What is a design pattern?

Design patterns are typical solutions to common problems in software design. Each pattern is like a blueprint that you can customize to solve a particular design problem in your code.

#### Q: Explain the Model-View-Controller (MVC) architectural pattern.

The **MVC** pattern separates application logic between **“Models”**, **“Views”** and **“Controllers”**.

**Controllers** handle a request, process it, retrieve data from the **Model**, format it and pass it to the **View**.

**Models** are responsible for shaping, storing and retrieving the data.

**Views** display the data and receive user input.

### Web Security

#### Q: What are some common web security concerns?

**HTTP**

We should use HTTPS instead of HTTP, since HTTPS is encrypted using public/private key encryption.

> External resource: [Google Developer's article on the usage of https.](https://developers.google.com/web/fundamentals/security/encrypt-in-transit/why-https)

**Cross-Site Scription (XSS)**

With Cross-Site Scripting, a malicious third party will find a way to *inject* arbitrary code on your page, and will use it to perform actions in name of the user.

The way we mitigate XSS is by 

For example, if Twitter didn't *escape* special characters in user publications before displaying them on a page, someone with bad intentions would have the ability to inject custom JavaScript that would create spam posts in name of the user. [This has happened in the past](https://www.youtube.com/watch?v=zv0kZKC6GAM).

> External resource: [Cross-site Scripting (**XSS**).](https://en.wikipedia.org/wiki/Cross-site_scripting)

**Cross-Site Request Forgery (CSRF)**

With Cross-Site Request Forgery, an ill-intentioned third party would be able issue requests to our application with a user's authentication information without their knowledge.

The way we mitigate CSRF attacks is by sending a unique CSRF Token with each request, or by not using cookie-based authentication at all (using JWT instead).

> External resource: [Cross-site Request Forging (CSRF).](https://www.owasp.org/index.php/Cross-Site_Request_Forgery_(CSRF))

### Project Management

#### Q: What is Waterfall?

Waterfall is a sequential, linear process of project management. It consists of several discrete phases. No phase begins until the prior phase is complete, and each phase's completion is terminal.

Waterfall management does not allow you to return to a previous phase.

#### Q: What is the Agile methodology?

The Agile methodology helps continuous iteration of development and testing by breaking the product into smaller builds.

In this methodology, development and testing activities are concurrent, unlike other software development methodologies (such as Waterfall). It also encourages teamwork and face-to-face communication. Business, stakeholders, and developers and clients must work together to develop a product.

#### Q: What is SCRUM?

Scrum is an agile process that allows us to focus on delivering value in the shortest time. It rapidly and repeatedly inspects actual working software. It emphasizes accountability, teamwork, and iterative progress toward a well-defined goal.

The Scrum Framework usually deals with the fact that the requirements are likely to change or most of the time not known at the start of the project.

> External Resource: [Agile vs. SCRUM](https://www.guru99.com/agile-vs-scrum.html)

#### Q: What are SOLID principles?

Principles we should strive for when developing.

**S: Single Responsibility**
Each piece of your code should address a single purpose and not get entangled with other code.

**O: Open/closed**
Your code should be open to extension (think inheritance) and closed to modification.

**L: Liskov Substitution Principle**
Your code should be substitutable for a different code implementation without breaking your application.

**I: Interface Segregation Principle**
Many highly specific smaller interfaces should be better than a few general purpose interfaces.

**D: Dependency Inversion Principle**
One should "depend upon abstractions, [not] concretions."

## External Resources

> [123 JavaScript Interview Questions](https://github.com/ganqqwerty/123-Essential-JavaScript-Interview-Questions)

> [1000 JavaScript Interview Questions](https://github.com/sudheerj/javascript-interview-questions)
