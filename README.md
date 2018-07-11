# Hello World com Spring Boot

## Dependências

* JDK 1.8 ou mais recente
* Gradle 4+
* Docker

## Como executar

* Clone esse repositório

* Altere o valor das variáveis em __build.gradle__:

	* docker\_user\_name: Seu nome de usuário no Docker (Default: bryanbcruz) 

	* image\_name: Nome da imagem que será gerada no Docker (Default: teste2)

* Execute `./gradlew build`

* Rodando apenas com o Docker:
	
	* Rode o container com `docker run -p 8080:8080 $docker_user_name/$image_name`

* Rodando com o Docker Compose:
	
	* Execute `docker-compose up`

* Acesse localhost na porta 8080
