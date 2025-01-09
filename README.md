# Currency-Converter
Objective
   Build a Spring Boot application that integrates with a public API to provide real-time currency conversion functionality.

Features

1. Fetch Exchange Rates
   Use a public API (e.g., Exchange Rates API or Open Exchange Rates) to fetch real-time currency exchange rates.
2. Endpoints
   GET /api/rates?base=USD: Fetch the exchange rates for the given base currency. The default base is USD if not provided.
   POST /api/convert: Convert an amount from one currency to another using the fetched exchange rates.
3. Error Handling
   Handle cases where:
   The external API is unavailable.
   Invalid currency codes are provided.
4. Testing
   Basic unit tests for the service layer using JUnit.

Technologies Used
  Spring Boot: Backend framework.
  Maven: Dependency management.
  Lombok: Simplify Java code with annotations.
  RestTemplate: HTTP client for making API calls.
  JUnit: Unit testing framework.

Project Structure
src/main/java/com/converter
├── controller
│   ├── CurrencyController.java
├── service
│   ├── CurrencyService.java
├── dto
│   ├── ConversionRequest.java
│   ├── ConversionResponse.java
│   ├── ExchangeRatesResponse.java
├── exception
│   ├── CurrencyConversionException.java
│   ├── GlobalExceptionHandler.java
├── config
│   ├── RestTemplateConfig.java
├── util
│   ├── Constants.java
├── CurrencyConverterApplication.java

Running the Application
1. Clone the repository:
   git clone <repository-url>
   cd currency-converter
2. Build the application using Maven:
   mvn clean install
3. Run the application:
   mvn spring-boot:run
4. Access the API:
   Base URL: http://localhost:8080
   POST /api/convert

Testing
  Run the tests using Maven:
  mvn test

API Documentation
  Detailed API documentation is available in the docs/ folder or can be accessed via a tool like Postman.
