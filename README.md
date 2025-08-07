# WIT-JAVA-Challenge

## Goals ##

The goal of this is to assess Java developers applying to WIT. It will be used solely to evaluate the applicant’s technical skills and their ability to complete a specific task within a designated timeframe.


Description

Your task will be to develop a RESTful API that provides the basic functionalities of a calculator.

Functional requirements: 
  - RESTful API that exposes the following operations: sum, subtraction, multiplication and division.
  - Offer Support for 2 operands only (a and b, to simplify).
  - Give support to arbitrary precision signed decimal numbers.

  Non-functional requirements:
    - Create a project, using Gradle or Maven, with at least 2 modules — rest and calculator.
    - Use Spring Boot as the foundation for all required modules.
    - Use Apache Kafka for communication between existing modules.
    - Configure via application.properties (default of Spring Boot).
    - None XML configuration (except, eventually, in logging).
    - Include required Docker configuration files for Docker image generation and Docker compose files for running all the modules.
    - Write unit tests to ensure the testability of the developed modules.
    - Include README file describing how to build and run the project.
    - Use of Git.

Bonus Points (Optional):
  - SLF4J: Add SLF4J logger support to both modules so that log messages are generated for every input/output event and errors. Configure an actual logging implementation at your choice (Log4J, Logback, etc.) with an appender to file (+2). 
  - Unique identifiers: Assigning a unique identifier to each individual REST request and communication to their respective customers via a response header (+3).
  - MDC Propagation: Propagation of the request identifier through the MDC in the inter-module communication and inclusion of it in each logging line that concerns an HTTP request in all modules (+5).

Deliverables

Git repository with the developed solution:
  - Publicly hosted on GitHub; or
  - Hosted privately on BitBucket and shared with us; or
  - Zipped and sent by email.


Useful Tips

The project skeleton can be generated at https://start.spring.io/. The instance of Apache Kafka to support inter-module communication can, for convenience, be based on Docker (https://hub.docker.com/r/apache/kafka), running locally.

Examples:
Example of an HTTP request for the operation 1 + 2:
      GET /sum?a=1&b=2 HTTP/1.1
      Accept: application/json
      (…)
Example of a response for the above request:
   HTTP/1.1 200 OK
      Content-Type: application/json
      (…)
      {
       "result": 3
      }

Evaluation
      • Structure and quality of the code;
      • Use correctly the above referred technologies;
      • Performance of the solution;
