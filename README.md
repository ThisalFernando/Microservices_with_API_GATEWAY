# Microservices

API Gateway integration with three microservices (item, order and payment services)

## Docker Setup

Run this command in all the services to ensure a fresh build of a project by removing all previously generated files, and bundling the final code into a distributable format (like a JAR or WAR file) in the target directory. 

```bash
mvn clean package
```
 Build all services.

```bash
docker-compose build
```
Start all containers. 

```bash
docker-compose up
```
Start in background (detached mode). 

```bash
docker-compose up -d 
```

View running containers . 

```bash
docker ps 
```
View logs for a specific service.

```bash
docker-compose logs item-service
```
Stop and remove all containers. 

```bash
docker-compose down 
```

## API Testing Evidence

``
POST http://localhost:8080/items
``

![Evidence 01](https://res.cloudinary.com/fmart/image/upload/v1772496000/Screenshot_2026-03-03_050452_vzkn1d.png)

``
GET http://localhost:8080/items
``

![Evidence 02](https://res.cloudinary.com/fmart/image/upload/v1772496001/Screenshot_2026-03-03_050509_grvzx7.png)

``
GET http://localhost:8080/items'{id}
``

![Evidence 03](https://res.cloudinary.com/fmart/image/upload/v1772496859/Screenshot_2026-03-03_054357_nyybph.png)

``
POST http://localhost:8080/orders
``

![Evidence 04](https://res.cloudinary.com/fmart/image/upload/v1772496001/Screenshot_2026-03-03_050544_m1n0ju.png)

``
GET http://localhost:8080/orders/{id}
``

![Evidence 05](https://res.cloudinary.com/fmart/image/upload/v1772496000/Screenshot_2026-03-03_050620_jfgmie.png)

``
POST http://localhost:8080/payments/process
``

![Evidence 06](https://res.cloudinary.com/fmart/image/upload/v1772495999/Screenshot_2026-03-03_050714_tdwwhq.png)

``
GET http://localhost:8080/payments/{id}
``

![Evidence 07](https://res.cloudinary.com/fmart/image/upload/v1772495877/Screenshot_2026-03-03_050751_qycggk.png)

## GitHub Repository Link

[Repo Link](https://github.com/ThisalFernando/Microservices_with_API_GATEWAY.git)