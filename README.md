# Hello World com Spring Boot

Esse projeto tem como objetivo rodar uma aplicação Spring Boot que retorna "Hello World!!!", utilizando o Gradle para fazer o build e o Docker-Compose para subir a aplicação.

## Dependências

* JDK 1.8 ou mais recente

* Gradle 4+

* Docker

* Kubernetes (Opcional)

## Como executar

* Clone esse repositório

* Altere o valor das variáveis em __build.gradle__:

	* docker\_user\_name: Seu nome de usuário no Docker (Default: bryanbcruz) 

* Execute `./gradlew build`

* Executando a aplicação:
	
	* (Opção 1) Utilizando apenas o Docker:
		
		* Execute `docker run -p 8080:8080 $docker_user_name/hello-world-spring-boot`

	* (Opção 2) Utilizando o Docker Compose:
		
		* Execute `docker-compose up`

	* (Opção 3) Utilizando Kubernetes:

		* Execute `kubectl create -f k8s/manifests/hello-world-deployment.yaml`

		* Execute `kubectl create -f k8s/manifests/hello-world-service.yaml`

* Acesse localhost na porta 8080 se utilizou a opção 1 ou 2, ou acesse o IP da sua máquina que está executando o Kubernetes na porta 30080 se utilizou a opção 3.
