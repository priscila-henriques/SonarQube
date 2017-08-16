![aaeaaqaaaaaaaaccaaaajdywnmqzndmyltqxzdetndvhmi1izjgwltm2mmfhndi0nwuwmw](https://user-images.githubusercontent.com/4249709/29342568-d8977fda-8201-11e7-92e8-9191627ab853.png)


É uma ferramenta de analise na qualidade do código.


## Criar a base de dados: 

    CREATE DATABASE sonar CHARACTER SET utf8 COLLATE utf8_general_ci;

    CREATE USER ‘sonar’ IDENTIFIED BY ‘sonar’;

    GRANT ALL ON sonar.* TO ‘sonar’@’%’ IDENTIFIED BY ‘sonar’;

    GRANT ALL ON sonar.* TO ‘sonar’@’localhost’ IDENTIFIED BY ‘sonar’;

    FLUSH PRIVILEGES;

## Configurar o banco de dados no arquivo "Sonar.Prorpeties": 

    sonar.jdbc.url=jdbc:mysql://localhost:3306/sonar?useUnicode=true&characterEncoding=utf8&rewriteBatchedStatements=true&useConfigs=maxPerformance

    sonar.jdbc.driverClassName=com.mysql.jdbc.Driver

    sonar.jdbc.validationQuery=select 1

    sonar.jdbc.username=root

    sonar.jdbc.password=123456


## Logar no Sonar(default) 
 
    Login: admin 

    Senha: admin 

## Projeto

    4.1 Criar o projeto 
    4.2 Criar (key) do Projeto 
    4.3 Dar permissão para usuario nas seções do projeto: 
    - Browser

    - See source code 

    - Administer issues 

    - Administer

    - Execute Analysis 

## Configurar o arquivo (sonar-scanner.properties):

    sonar.login=admin

    sonar.password=admin

    sonar.projectKey=apiyandeh

    sonar.projectName=ApiYandeh

    sonar.projectVersion=1.0

## executar o sonar

    linha de comando cmd dentro do projeto que será analisado:

    C:\sonar-scanner-3.0.3.778-windows\bin\sonar-scanner.bat




