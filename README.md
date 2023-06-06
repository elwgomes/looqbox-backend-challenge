# Repositório do Back-end Looqbox Challenge
Repositório criado com a finalidade de entregar o desafio de Backend da Looqbox.


### Sobre o desafio:
Foi criado um microsservice utilizando a API externa PokeAPI.co. Ele fornece endpoints de consulta que podem retornar a resposta tanto em ordem alfabética como pela quantidade de caracteres em ordem crescente. Os algoritmos de <b>SORTING</b> foram feitos sem o uso de qualquer biblioteca utilizando apenas bubble sort. Na resposta da API também é mostrada um highlight no nome Pokemon onde representa a substring.

### Integração:
O projeto é integrado com a API PokeAPI. Mais informações no link baixo:
```
https://pokeapi.co/
```

## Screenshots:

#### Consultas:

```
GET 
v1/api/pokemon/ala
```
![screenshot-1](/looqbox-backend-challenge/screenshots/default1.png "screenshot 1")

```
GET 
v1/api/pokemon/alph/ala
```
![screenshot-2](/looqbox-backend-challenge/screenshots/alph1.png "screenshot 2")

```
GET 
v1/api/pokemon/length/ala
```
![screenshot-3](/looqbox-backend-challenge/screenshots/length.png "screenshot 3")

#### Testes:

![screenshot-4](/looqbox-backend-challenge/screenshots/junit-test.png "screenshot 4")

## Tecnologias utilizadas
#### - Frameworks e linguagens-
* Java 17; 
* Spring Framework 3.1.0;
* Gradle;
* jUnit;
* Docker;
* Lombok;

## Docker

1- Após clonar o repositório, execute o comando gradle para buildar o projeto:
```
./gradlew build
```

2- Após buildar o projeto, crie a imagem Docker executando o comando abaixo:
```
docker build -t looqbox:latest .
```

3- Após o processo de criação de imagem finalizar, execute-a para iniciar o container com o comando abaixo:
```
docker run -p 8080:8080 looqbox:latest .
```





### Would you like to work with us? Apply [here](https://app.pipefy.com/public_form/840222)!

# Looqbox Backend Challenge
![Looqbox](logo.png)

## Challenge
In this challenge you will need to build a **Microservice** using the stack below and a provided api.

We will not use anything from your project other than evaluate your skills and you are free to use this project in your portfolio.

## Stack
We use:
- Java/Kotlin
- `Spring Boot` for the framework
- `Gradle` for dependency management and local deployment

## Submitting
- Make a fork of this repository
- When you're done send us a pull request

# Guidelines
You need to make a HTTP REST API that 
- Consumes the [PokeAPI](https://pokeapi.co/) data.
- Provides an endpoint to query pokemons based on the substring of its name. For example:
  - Request: `GET /pokemons?q=pidge`
  - Expected response: ```{"result" : ["pidgey", "pidgeotto", "pidgeot"]}```
- You need to apply sorting by two algorithms (it is not permitted to use a sorting library, for this particular feature you must implement by yourself). And it’s very important to explain your implemented logic (For instance, you can use inline comments on the source code): 
  - the pokemon name's length and; 
  - the pokemon name's alphabetical order 
 
- Find a way to indicate the pokemon name highlight regarding the piece of its queried name. For example:
  - The queried name was `pi`
  - The highlight object must be ```{"name": "pikachu", "highlight": "<pre>pi</pre>kachu"}``` or ```{"name": "pikachu", "start": 0, "end": 2}```
- Draw a diagram explaining your architecture

## Bonus points!
- Design Patterns
- Unit Testing
- Dockerize the application
- Explain the Big-Ω (time complexity) of your sorting algorithms (explain how you calculated them)

## Useful links
- [Spring Framework](https://spring.io/)
- [Gradle](https://gradle.org/)
- [PokeApi docs](https://pokeapi.co/docs/v2.html)
