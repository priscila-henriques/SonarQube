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

3.Logar no Sonar: 

Login: admin 
Senha: admin 

(default) 


