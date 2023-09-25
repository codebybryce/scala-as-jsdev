# # JavaScript (ES6) vs Scala 3 Cheatsheet

## Basic Language Features

| **Variables**                 |                                              |                                                              |
|-------------------------------|----------------------------------------------|--------------------------------------------------------------|
| Immutable                     | `const x = 10;`                              | `val x: Int = 10`                                            |
| Mutable                       | `let y = 20;`                                | `var y: Int = 20`                                            |
| **Data Types**                |                                              |                                                              |
| String                        | `"hello"` or `'hello'`                       | `"hello"`                                                    |
| Integer                       | `let int = 123;`                             | `val int: Int = 123`                                         |
| Double                        | `let dbl = 123.45;`                          | `val dbl: Double = 123.45`                                   |
| Boolean                       | `true` or `false`                            | `true` or `false`                                            |
| Matrix                        | `const matrix = [[x,x,x], [y,y,y]]     `      | `val matrix: Array[Array[Double]] = Array(Array(x,x,x), Array(y,y,y))` |
| **Functions**                 |                                              |                                                              |
| Function Declaration          | `function sum(a, b) { return a+b; }`         | `def sum(a: Int, b: Int): Int = a + b`                       |
| Arrow Function                | `const sum = (a, b) => a + b;`               | (Lambdas use `=>` too)                                       |
| **Arrays**                    |                                              |                                                              |
| Declaration                   | `let arr = [1,2,3];`                         | `val arr = List(1,2,3)`                                      |
| Accessing                     | `arr[0]`                                     | `arr(0)`                                                     |
| **Control Structures**        |                                              |                                                              |
| If-Else                       | `if (cond) {} else {}`                       | `if (cond) {} else {}`                                       |
| For Loop                      | `for (let i = 0; i < 10; i++) {}`            | `for (i <- 0 until 10) {}`                                   |
| While Loop                    | `while (cond) {}`                            | `while (cond) {}`                                            |
| **Objects**                   |                                              |                                                              |
| Declaration                   | `let obj = {key: "value"};`                  | `val obj = Map("key" -> "value")`                            |
| Accessing                     | `obj.key` or `obj["key"]`                    | `obj("key")`                                                 |
| **Classes**                   |                                              |                                                              |
| Declaration                   | `class MyClass {}`                           | `class MyClass`                                              |
| Constructor                   | `constructor() { }`                          | `class MyClass(val x: Int)`                                  |
| **Traits (Interfaces)**       |                                              |                                                              |
| N/A in JavaScript             | N/A                                          | `trait MyTrait`                                              |
| **Pattern Matching**          |                                              |                                                              |
| N/A in JavaScript             | N/A                                          | `x match { case y => ... }`                                  |
| **Functional Programming**    |                                              |                                                              |
| Map over Array                | `arr.map(x => x + 1)`                        | `arr.map(x => x + 1)`                                        |
| Filter Array                  | `arr.filter(x => x > 2)`                     | `arr.filter(x => x > 2)`                                     |
| Reduce Array                  | `arr.reduce((acc, x) => acc + x, 0)`         | `arr.reduce(_ + _)`                                          |
| **Async Programming**         |                                              |                                                              |
| Promises                      | `new Promise((resolve, reject) => {})`       | Future, etc. (Complex topic)                                 |
| Async/Await                   | `async function() { await someFunction(); }` | N/A in a direct form                                         |
| **String Interpolation**      |                                              |                                                              |
| Template Strings              | `` `Hello, ${name}!` ``                      | `s"Hello, $name!"`                                           |
| **Tuples**                    |                                              |                                                              |
| Declaration                   | `let tuple = [1, "two"];`                    | `val tuple = (1, "two")`                                     |
| Accessing                     | `tuple[0]`                                   | `tuple._1`                                                   |
| **Optionality**               |                                              |                                                              |
| Option/Nullable               | `let x = null;`                              | `val x: Option[String] = Some("hello")` or `None`            |
| **Pattern Matching on Types** |                                              |                                                              |
| N/A in JavaScript             | N/A                                          | `x match { case _: Int => "int"; case _: String => "string" }` |
| **Imports & Packages**        |                                              |                                                              |
| Importing                     | `import {x} from "module";`                  | `import packageName.className`                               |
| Exporting                     | `export const x = 10;`                       | `class MyClass` (inside a package)                           |
| **Implicit Parameters**       |                                              |                                                              |
| N/A in JavaScript             | N/A                                          | `def f(implicit x: Int) = x * 2`                             |
| **Extensions**                |                                              |                                                              |
| N/A in JavaScript             | N/A                                          | `extension (x: Int) def square = x * x`                      |
| **Destructuring**              |                                                |                                             |
| Arrays                         | `let [a, b] = [1, 2];`                         | `val List(a, b) = List(1, 2)`               |
| Objects                        | `let {a, b} = {a: 1, b: 2};`                   | `val Person(a, b) = Person(1, 2)`           |
| **Enumerations**               |                                                |                                             |
| Enumerations                   | `const COLORS = {RED: 'RED', BLUE: 'BLUE'};`   | `enum Colors { case Red, Blue }`            |
| **Higher Order Functions**     |                                                |                                             |
| Functions as Arguments         | `arr.filter(func)`                             | `arr.filter(func)`                          |
| Returning Functions            | `const outer = () => () => "Hello";`           | `def outer(): () => String = () => "Hello"` |
| **Case Classes & Objects**     |                                                |                                             |
| N/A in JavaScript              | N/A                                            | `case class Person(name: String, age: Int)` |
| Singleton Objects              | N/A in JS (closest: static methods in classes) | `object Singleton`                          |
| **Lazy Values**                |                                                |                                             |
| N/A in JavaScript              | N/A                                            | `lazy val x = compute()`                    |
| **Collections**                |                                                |                                             |
| Sets                           | `new Set([1,2,3])`                             | `Set(1, 2, 3)`                              |
| Maps                           | `new Map([["a", 1], ["b", 2]])`                | `Map("a" -> 1, "b" -> 2)`                   |
| **Type Inference**             |                                                |                                             |
| Basic Inference                | `let x = 10; // number`                        | `val x = 10 // Int`                         |
| **Tail Recursion**             |                                                |                                             |
| N/A in JavaScript              | N/A                                            | `@tailrec def factorial(n: Int): Int = ...` |
| **Union & Intersection Types** |                                                |                                             |
| Union                          | let x: string // number` (TypeScript)          | `type X = String // Int`                    |
| Intersection                   | `let x: string & {prop: number}` (TypeScript)  | `type X = String & MyTrait`                 |
| **Generics**                   |                                                |                                             |
| Using Generics                 | `function identity<T>(arg: T): T { return arg; }` (TypeScript) | `def identity[A](arg: A): A = arg`                 |
| **Operators**                  |                                                              |                                                      |
| Equality                       | `===`                                                        | `==`                                                 |
| Inequality                     | `!==`                                                        | `!=`                                                 |
| **Companion Objects**          |                                                              |                                                      |
| N/A in JavaScript              | N/A                                                          | `class MyClass { ... }; object MyClass { ... }`      |
| **Traits with Implementation** |                                                              |                                                      |
| Mixins (similar concept)       | Using class extends in combination with mixins               | `trait TraitName { def method = ... }`               |
| **Error Handling**             |                                                              |                                                      |
| Try-Catch                      | `try { ... } catch (e) { ... }`                              | `try { ... } catch { case e: ExceptionType => ... }` |
| **Concurrency**                |                                                              |                                                      |
| Futures/Promises               | `Promise.resolve().then().catch()`                           | `import scala.concurrent.Future; Future { ... }`     |
| **Implicit Conversion**        |                                                              |                                                      |
| N/A in JavaScript              | N/A                                                          | `given Conversion[String, Int] = _.toInt`            |
| **Type Bounds**                |                                                              |                                                      |
| N/A in JavaScript              | N/A (TypeScript has)                                         | `[A <: UpperBound]` or `[A >: LowerBound]`           |
| **For-comprehensions**         |                                                              |                                                      |
| Promise chaining               | `.then().then()`                                             | `for { x <- Future1; y <- Future2 } yield ...`       |
| **Local Type Definitions**     |                                                              |                                                      |
| TypeScript `type`              | `type MyType = string  number;`                              | `type MyType = String or  Int`                       |
| **Annotations**                |                                                              |                                                      |
| Decorators (similar concept)   | `@decorator`                                                 | `@annotation`                                        |


## Libraries and Frameworks

| Feature/Task                   | ES6 JavaScript (with popular libraries) | Scala 3 (with popular libraries) |
|--------------------------------|------------------------------------------|----------------------------------|
| **HTTP Requests**              |                                          |                                  |
| Fetching Data                  | `fetch(url).then(response => response.json())` (using Fetch API) | `import sttp.client3._; basicRequest.get(uri"$url").send()` (using sttp) |
| **Database Access (SQL)**      |                                          |                                  |
| Making a Query                 | `const result = await pool.query('SELECT * FROM users')` (using node-pg) | `sql"SELECT * FROM users".as[User].list` (using Slick) |
| **JSON Serialization**         |                                          |                                  |
| Encoding                       | `JSON.stringify(obj)`                  | `import io.circe.syntax._; obj.asJson.noSpaces` (using Circe) |
| Decoding                       | `JSON.parse(string)`                   | `import io.circe.parser._; decode[MyClass](string)` (using Circe) |
| **Web Frameworks**             |                                          |                                  |
| Define a route                 | `app.get('/path', (req, res) => { ... })` (using Express.js) | `GET /path controllers.MyController.action` (using Play Framework) |
| **Testing**                    |                                          |                                  |
| Writing a Test                 | `test('description', () => { expect(...).toBe(...) })` (using Jest) | `test("description") { assert(...) }` (using ScalaTest) |
| **WebSocket**                  |                                          |                                  |
| Establishing a Connection     | `const socket = new WebSocket(url);` (using Web API) | `val socket = new WebSocket().url(url)` (using Play Framework WebSocket) |
| **Functional Libraries**       |                                          |                                  |
| Handling Options               | `Maybe.fromNullable(value).map(...)` (using Folktale) | `Option(value).map(...)` (native Scala) |
| **Reactive Programming**       |                                          |                                  |
| Observables                    | `const obs$ = of(1, 2, 3)` (using RxJS) | `val obs = Observable(1, 2, 3)` (using Monix) |
| **Authentication & Authorization** |                                                      |                                                              |
|------------------------------------|------------------------------------------------------|--------------------------------------------------------------|
| JWT Authentication                 | Using `jsonwebtoken`                                 | Using libraries like `Silhouette` or `Pac4j`                 |
| OAuth Integration                  | Using `passport`                                     | Using `Silhouette` with OAuth1/2 providers                   |
| **Asynchronous Programming**       |                                                      |                                                              |
| Handling Async Tasks               | `async/await` with Promises                          | Using `Future` and `Await`                                   |
| **Streaming Data**                 |                                                      |                                                              |
| Stream Processing                  | Using `stream` in Node.js                            | Using `Akka Streams`                                         |
| **Event Sourcing**                 |                                                      |                                                              |
| Event Store Implementation         | Using libraries like `eventstore`                    | Using `Akka Persistence`                                     |
| **Microservices**                  |                                                      |                                                              |
| Service Communication              | Using libraries like `axios` or `grpc-node`          | Using `Akka HTTP` or `Lagom`                                 |
| **UI Frameworks (Web Frontend)**   |                                                      |                                                              |
| Building UI Components             | Using frameworks like `React` or `Vue.js`            | Using `Scala.js` with `React` wrappers like `Slinky`         |
| **Template Engines**               |                                                      |                                                              |
| Rendering HTML                     | Using engines like `EJS` or `Handlebars`             | Using `Twirl` (with Play Framework)                          |
| **Real-Time Communication**        |                                                      |                                                              |
| Real-Time WebSockets               | Using libraries like `socket.io`                     | Using `Akka HTTP WebSockets` or `Play Framework WebSockets`  |
| **Serverless Architecture**        |                                                      |                                                              |
| Deploying Serverless Functions     | Using platforms like `Vercel` or `Netlify`           | Using platforms like `AWS Lambda` with Scala handlers        |
| **Message Queues & Brokers**       |                                                      |                                                              |
| Interacting with Message Queues    | Using libraries like `amqplib` for RabbitMQ          | Using `Akka Streams` with Alpakka connectors                 |
| **Distributed Tracing**            |                                                      |                                                              |
| Monitoring & Tracing               | Using tools like `Jaeger` with OpenTracing libraries | Using `Akka Telemetry` or Lightbend Telemetry                |
| **Data Visualization**             |                                                      |                                                              |
| Charting & Graphing                | Using libraries like `Chart.js` or `D3.js`           | Using Scala.js with facade libraries for D3 or other JS charting libraries |
| **Dependency Injection**             |                                                      |                                                              |
|--------------------------------------|------------------------------------------------------|--------------------------------------------------------------|
| Injecting Dependencies               | Using libraries like `InversifyJS`                   | Using libraries like `MacWire`                               |
| **Logging**                          |                                                      |                                                              |
| Log Messages                         | `console.log('Message')`                             | `import org.slf4j.LoggerFactory; val logger = LoggerFactory.getLogger(getClass); logger.info("Message")` |
| **Date and Time**                    |                                                      |                                                              |
| Handling Dates                       | Using libraries like `moment.js` or `date-fns`       | Using libraries like `java.time` (built-in) or `Joda-Time`   |
| **ORM (Object-Relational Mapping)**  |                                                      |                                                              |
| Entity Definition                    | Using libraries like `Sequelize` or `TypeORM`        | Using libraries like `Slick` or `Quill`                      |
| **Caching**                          |                                                      |                                                              |
| Cache Implementation                 | Using libraries like `node-cache`                    | Using libraries like `Caffeine` or `ScalaCache`              |
| **GraphQL Integration**              |                                                      |                                                              |
| Define a Schema                      | Using libraries like `graphql-js` or `Apollo Server` | Using libraries like `Sangria`                               |
| **File I/O**                         |                                                      |                                                              |
| Read a File                          | Using Node's `fs` module                             | Using Scala's `scala.io.Source` or Java's `java.nio.file`    |
| **Image Processing**                 |                                                      |                                                              |
| Processing Images                    | Using libraries like `sharp`                         | Using libraries like `scrimage`                              |
| **Machine Learning**                 |                                                      |                                                              |
| Building Models                      | Using libraries/frameworks like `TensorFlow.js`      | Using libraries like `Breeze` or `Smile`                     |
| **Build Tools & Package Management** |                                                      |                                                              |
| Dependency Management                | `npm` or `yarn`                                      | `sbt` (Scala Build Tool)                                     |
| **CSS & Styling (for web projects)** |                                                      |                                                              |
| Styling                              | Using libraries/frameworks like `Styled Components`  | Using libraries/frameworks like `ScalaCSS`                   |