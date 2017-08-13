# SonarQube

1.Criar a base de dados: 

CREATE DATABASE sonar CHARACTER SET utf8 COLLATE utf8_general_ci;

CREATE USER ‘sonar’ IDENTIFIED BY ‘sonar’;

GRANT ALL ON sonar.* TO ‘sonar’@’%’ IDENTIFIED BY ‘sonar’;

GRANT ALL ON sonar.* TO ‘sonar’@’localhost’ IDENTIFIED BY ‘sonar’;

FLUSH PRIVILEGES;

2. Configurar o banco de dados no arquivo "Sonar.Prorpeties": 

sonar.jdbc.url=jdbc:mysql://localhost:3306/sonar?useUnicode=true&characterEncoding=utf8&rewriteBatchedStatements=true&useConfigs=maxPerformance

sonar.jdbc.driverClassName=com.mysql.jdbc.Driver

sonar.jdbc.validationQuery=select 1

sonar.jdbc.username=root

sonar.jdbc.password=123456


3.Logar no Sonar(default) 
 
Login: admin 

Senha: admin 

4. Projeto

4.1 Criar o projeto 
4.2 Criar (key) do Projeto 
4.3 Dar permissão para usuario nas seções do projeto: 
- Browse

- See source code 

- Administer issues 

- Administer

- Execute Analysis 

5.Configurar o arquivo (sonar-scanner.properties):

#Configure here general information about the environment, such as SonarQube DB details for example
#No information about specific project should appear here

#----- Default SonarQube server
#sonar.host.url=http://localhost:9000
#----- Default source code encoding
# must be unique in a given SonarQube instance
sonar.login=admin
sonar.password=admin
sonar.projectKey=apiyandeh
# this is the name and version displayed in the SonarQube UI. Was mandatory prior to SonarQube 6.1.
sonar.projectName=ApiYandeh
sonar.projectVersion=1.0
# Path is relative to the sonar-project.properties file. Replace "\" by "/" on Windows.
# This property is optional if sonar.modules is set. 
sonar.sources=./ 
# Encoding of the source code. Default is default system encoding
#sonar.sourceEncoding=UTF-8

