\# SOFE 3980U — Lab 2: Binary Calculator (Web Application \& API)



A Spring Boot application built with Apache Maven that implements a binary calculator, available both as a web application (with a browser-based UI) and as a REST API. Supports \*\*addition\*\*, \*\*multiplication\*\*, \*\*bitwise AND\*\*, and \*\*bitwise OR\*\* on binary number strings.



\## Overview



This project extends the Lab 1 `Binary` class into a full Spring Boot web application and API service. It includes:



\- A web-based calculator UI for performing binary operations

\- A REST API returning results as plain text or JSON

\- A full automated test suite using Spring's MockMvc framework



\## Technologies Used



\- Java

\- Apache Maven

\- Spring Boot

\- Thymeleaf (server-side templating)

\- JUnit / Spring MockMvc (testing)



\## Project Structure



```

BinaryCalculatorWebapp/

├── pom.xml

├── src/

│   ├── main/

│   │   ├── java/com/ontariotechu/sofe3980U/

│   │   │   ├── Application.java

│   │   │   ├── Binary.java

│   │   │   ├── BinaryController.java

│   │   │   ├── BinaryAPIController.java

│   │   │   ├── BinaryAPIResult.java

│   │   │   ├── HelloController.java

│   │   │   ├── HelloAPIController.java

│   │   │   └── APIResult.java

│   │   └── resources/templates/

│   │       ├── calculator.html

│   │       ├── result.html

│   │       ├── error.html

│   │       └── hello.html

│   └── test/

│       └── java/com/ontariotechu/sofe3980U/

│           ├── BinaryControllerTest.java

│           ├── BinaryAPIControllerTest.java

│           ├── HelloControllerTest.java

│           └── HelloAPIControllerTest.java

```



\## Getting Started



\### Prerequisites



\- Java JDK installed

\- Apache Maven installed

\- `JAVA\_HOME` environment variable configured



\### Build the project



```bash

mvn clean install

```



\### Run the application



```bash

mvn spring-boot:run

```



The application will start on \*\*http://localhost:8080\*\*.



\## Web Application



Navigate to \[http://localhost:8080](http://localhost:8080) to use the calculator interface.



\- Enter two binary numbers (`operand1` and `operand2`)

\- Select an operator: `+`, `\*`, `\&`, or `|`

\- Click \*\*=\*\* to calculate the result

\- Use \*\*New Calculation\*\* to start over, or \*\*Continue Calculation\*\* to carry the result forward as the next `operand1`



\## REST API Endpoints



\### Hello API



| Endpoint | Description |

|---|---|

| `GET /helloAPI` | Returns `Hello World!` |

| `GET /helloAPI?name=Jack` | Returns `Hello Jack!` |

| `GET /emailAPI` | Returns a suggested email using default name |

| `GET /emailAPI?fname=Abraham` | Returns a suggested email using the given first name |

| `GET /emailAPI?lname=Lincoln` | Returns a suggested email using the given last name |

| `GET /emailAPI?fname=Abraham\&lname=Lincoln` | Returns a suggested email using both names |



\### Binary Calculator API



| Endpoint | Description |

|---|---|

| `GET /add?operand1=111\&operand2=1010` | Addition (string result) |

| `GET /add\_json?operand1=111\&operand2=1010` | Addition (JSON result) |

| `GET /multiply?operand1=111\&operand2=1010` | Multiplication (string result) |

| `GET /multiply\_json?operand1=111\&operand2=1010` | Multiplication (JSON result) |

| `GET /and?operand1=1100\&operand2=1010` | Bitwise AND (string result) |

| `GET /and\_json?operand1=1100\&operand2=1010` | Bitwise AND (JSON result) |

| `GET /or?operand1=1100\&operand2=1010` | Bitwise OR (string result) |

| `GET /or\_json?operand1=1100\&operand2=1010` | Bitwise OR (JSON result) |



JSON responses are structured as:



```json

{

&#x20; "operand1": "1100",

&#x20; "operator": "or",

&#x20; "operand2": "1010",

&#x20; "result": "1110"

}

```



\## Running Tests



```bash

mvn clean install

```



This compiles the project and runs the full test suite (37 tests) covering:



\- Default and parameterized behavior of the web application

\- All four operators (`+`, `\*`, `\&`, `|`) in both the web application and API

\- Edge cases: zero operands, leading zeros, and operands of different bit lengths

\- Pre-existing functionality (default addition, calculator navigation)



Expected output:



```

Tests run: 37, Failures: 0, Errors: 0, Skipped: 0

BUILD SUCCESS

```









\Janvi Naresh Gurfude — SOFE 3980U, Ontario Tech University

