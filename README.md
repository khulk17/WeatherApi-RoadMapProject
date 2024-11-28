# Weather API Microservice
### https://roadmap.sh/projects/weather-api-wrapper-service
This project is a Spring Boot microservice that fetches weather data from the Visual Crossing Weather API and caches the responses using Redis.

## Prerequisites

- Java 17 or higher
- Maven 3.6.0 or higher
- Redis server

## Getting Started

### Clone the repository

```bash
git clone https://github.com/khulk17/weather-api-microservice.git
cd weather-api-microservice
```

### Build the project

```bash
mvn clean install
```
### Run the application

```bash
mvn spring-boot:run
```
### Configuration
```bash
spring.redis.host=localhost
spring.redis.port=6379
spring.redis.password=yourpassword

weather.api.key=your_api_key
```
## Usage
### Endpoints
#### Get weather by city and country
```bash
GET /weather/{city}/{country}
Example:
GET /weather/London/UK
```

#### Get weather by city, country, and date range
```bash
GET /weather/{city}/{country}/{startDate}/{endDate}
Example:  
GET /weather/London/UK/2024-11-26/2024-11-27
```
## Project Structure
#### src/main/java/com/khulk/microservice/weatherapi/Configs/RedisConfig.java: Redis configuration.
#### src/main/java/com/khulk/microservice/weatherapi/Controllers/WeatherController.java: REST controller for weather endpoints.
#### src/main/java/com/khulk/microservice/weatherapi/Dtos/: Data Transfer Objects (DTOs) for API responses.
#### src/main/java/com/khulk/microservice/weatherapi/Models/WeatherOfDay.java: Model class for weather data.
#### src/main/java/com/khulk/microservice/weatherapi/Service/RedisService.java: Service for Redis operations.
#### src/main/java/com/khulk/microservice/weatherapi/Service/WeatherService.java: Service for fetching weather data and caching it in Redis.

## Dependencies
#### Spring Boot
#### Spring Data Redis
#### Lombok
#### Visual Crossing Weather API
# License
## This project is licensed under the MIT License.

## This `README.md` file provides an overview of the project, including prerequisites, setup instructions, configuration details, usage examples, and a brief description of the project structure.
