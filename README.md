# Deploying-WebApp-on-DigitalOcean

## Demo Project

### Technologies used
- DigitalOcean
- Linux
- Java
- Gradle

### Project Description
- Setup and configure a server on DigitalOcean
- Create and configure a new Linux user on the Droplet (Security best practice)
- Deploy and run a Java Gradle application on Droplet

### Notes
- Select SSH Key as authentication method

  <img src="./Screenshot from 2023-05-03 16-13-00.png" alt="Select SSH Key as authentication method">
 
- Get your public key

  <img src="./Screenshot from 2023-05-03 16-13-43.png" alt="Get your public key">
 
 cat ~/.ssh/id_rsa.pub
    add that public key into droplet.
    
    build jar file: ./gradlew build
    
    Copy jar file to remote server: scp build/libs/java-react-example.jar [root@157.245.102.50](mailto:root@157.245.102.50):/root
    
    executing jar file on server: java -jar java-react-example.jar
    
    to run command in detach mode: java -jar java-react-example.jar &
    
    create a separate linux user: adduser rachana
    
    paste your public key for this new user.
