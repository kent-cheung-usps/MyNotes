## Quick steps to launch a complete COP app
1. run ./localDeploy.sh
2. https://cop-localhost.usps.com:8443/
   
### COP Web App
1. npm install
2. ng build
3. ng serve
### COP Core App
1. mvn clean install
2. mvn spring-boot:run -Dspring-boot.run.profiles=sit -f pom.xml
### Launch the COP
https://cop-localhost.usps.com:8443/
