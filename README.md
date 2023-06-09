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

  <img src="./Screenshot from 2023-05-03 17-36-59.png" alt="Get your public key">

- Add your public key to DigitalOcean

  <img src="./Screenshot from 2023-05-03 16-13-43.png" alt="Get your public key">
  
- Create an Inbound Firewall Rule to connect to remote droplet server using ssh by providing port number and sources
 
  <img src="./Screenshot from 2023-05-03 16-17-44.png" alt="Get your public key">
  
- Add the firewall rule to our droplet

  <img src="./Screenshot from 2023-05-03 16-19-41.png" alt="Get your public key">
  
- SSH into droplet server using Public IP of server

  <img src="./Screenshot from 2023-05-03 16-21-16.png" alt="Get your public key">
  
- Create build for the Web Application

  <img src="./Screenshot from 2023-05-03 16-26-45.png" alt="Get your public key">
  
- Copy jar file from local to remote server 

  <img src="./Screenshot from 2023-05-03 17-50-00.png" alt="Get your public key">
  
- Check if file got copied successfully

  <img src="./Screenshot from 2023-05-03 16-30-13.png" alt="Get your public key">
    
- Executing jar file on server (to run command in detach mode: java -jar java-react-example.jar &)

  <img src="./Screenshot from 2023-05-03 16-31-01.png" alt="Get your public key">
  
- Output after running above command
  
  <img src="./Screenshot from 2023-05-03 16-32-59.png" alt="Get your public key">
  
- Open the port on server via inbound firewall rule to access the webapp through web browser

  <img src="./Screenshot from 2023-05-03 16-33-57.png" alt="Get your public key">
     
- It is not recommended to use root user for everything, create a separate linux user

  <img src="./Screenshot from 2023-05-03 16-43-30.png" alt="Get your public key">
  
- Add new user to sudo group

  <img src="./Screenshot from 2023-05-03 16-44-43.png" alt="Get your public key">
  
- To access server via ssh using new user we have to paste our public key into .ssh/authorized_keys

  <img src="./Screenshot from 2023-05-03 16-48-26.png" alt="Get your public key">
    
- SSh using new user

  <img src="./Screenshot from 2023-05-03 16-50-54.png" alt="Get your public key">
