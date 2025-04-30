# spring-app

Projeto de estudo em Spring Boot 3.4.5 usando JDK 21 e Maven (via Maven Wrapper).

## Descrição

Este é um projeto básico em Spring Boot, criado para fins de estudo e aprendizado.
Ele traz as dependências de:
- **spring-boot-starter-web** (para criar APIs REST)
- **spring-boot-devtools** (reload automático em desenvolvimento)
- **Lombok** (redução de boilerplate com anotações)

O artefato final é um **JAR** executável.

## Pré-requisitos

- **Java 21**
- **Maven** *(opcional)* – usamos o Maven Wrapper incluído no projeto, então não é necessário ter o Maven instalado globalmente.

## Como clonar

```bash
git clone https://github.com/SEU_USUARIO/spring-app.git
cd spring-app
```

## Build & Execução

### 1. Build com Maven Wrapper

Linux/macOS:
```bash
./mvnw clean install
```
Windows (PowerShell/CMD):
```powershell
mvnw.cmd clean install
```

### 2. Executar a aplicação

Linux/macOS:
```bash
./mvnw spring-boot:run
```
Windows:
```powershell
mvnw.cmd spring-boot:run
```

Após iniciada, a API estará disponível em `http://localhost:8080/`.

## Dependências principais

```xml
<parent>
  <groupId>org.springframework.boot</groupId>
  <artifactId>spring-boot-starter-parent</artifactId>
  <version>3.4.5</version>
</parent>
<properties>
  <java.version>21</java.version>
</properties>

<dependencies>
  <!-- API REST -->
  <dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-web</artifactId>
  </dependency>

  <!-- Live reload em dev -->
  <dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-devtools</artifactId>
    <scope>runtime</scope>
  </dependency>

  <!-- Lombok para reduzir código boilerplate -->
  <dependency>
    <groupId>org.projectlombok</groupId>
    <artifactId>lombok</artifactId>
    <optional>true</optional>
  </dependency>
</dependencies>
```

## Estrutura de pastas

```
spring-app
├── mvnw
├── mvnw.cmd
├── .mvn/
│   └── wrapper/
│       ├── maven-wrapper.jar
│       └── maven-wrapper.properties
├── pom.xml
└── src/
    ├── main/
    │   ├── java/com/diogo/spring_app/
    │   │   └── SpringAppApplication.java
    │   └── resources/
    │       └── application.properties
    └── test/
        └── java/com/diogo/spring_app/
            └── SpringAppApplicationTests.java
```

## Customizações

- **application.properties**
  Ajuste servidor, porta, ou configurações de banco caso adicione persistence.
- **Lombok**
  Se usar IDE, ative o _annotation processing_ (Eclipse/STS: `Project → Properties → Lombok`; IntelliJ: `Settings → Compiler → Annotation Processors`).

## Licença

Este projeto é fornecido “as is” para estudo pessoal. Sinta-se à vontade para clonar, forkar e experimentar.

---

> — Diogo Cesar Furlan da Silva
