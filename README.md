# devops-bootcamp
El paso a paso de mi inico de devops de cero a experto

# Que es devops?
 - DevOps es un conjunto de prácticas, filosofías y herramientas que buscan mejorar la colaboración y comunicación entre los equipos de desarrollo y operaciones de software. Su objetivo principal es acelerar el ciclo de vida del desarrollo, desde la creación hasta la implementación, permitiendo la entrega continua de software de alta calidad y valor para el cliente.
   ![33516ef6-48d4-415b-b747-3bcc3bd2b00d](https://github.com/user-attachments/assets/4af943d6-daf0-4d1a-851a-b78d01c8538e)

   

 # Instalar los programas
   # Primero instalar WSL para ocupar el entorno linux
      - En powershell como administrador
      - Escribir comando wsl --install 
      - si tienes errores ocupar estos comandos, verificar si el hyper-v y en la bios la virtuzalicacion estan activos   
        dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
        dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
      - Reinciar
      - Ejecutar desde windows ubuntu o wsl en la consola
      - Actualizar linux (sudo apt update && sudo apt upgrade -y)
      - Instalar herramientas  (sudo apt install curl unzip git -y) 
      - Listo probrar comandos basicos de linux, ls, pwd, whoami
   # Instalar Git
      - Verificar si esta instalado git --version
      - si no ocupar 
        sudo apt update
        sudo apt install git -y
   # Instalar VS Code
      - Instalar las siguientes extensiones
        - Docker
        - GitHub Copilot (opcional)
        - YAML
        - Terraform
        - Remote - WSL (solo si usas WSL)
   # Instalar Docker
      - Verificar si esta docker --version
      - Si no instalar en wsl con los siguientes comandos
        sudo apt update
        sudo apt install docker.io -y
        sudo systemctl start docker
        sudo systemctl enable docker
        sudo usermod -aG docker $USER
     - Luego verificar con el comando docker run hello-world, si aparece "Hello from Docker!" → ✔️ ¡Éxito!
  # Instalar AWS CLI
     - Verificar con aws --version
     - Si no ocupar
       sudo apt update
       sudo apt install unzip curl -y
       curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
       unzip awscliv2.zip
       sudo ./aws/install
     - Revisar con comando aws --version 
  # Instalar Terraform CLI
     - Verificar con terraform -help
     - Si no ocupar
       sudo apt install -y gnupg software-properties-common curl
       curl -fsSL https://apt.releases.hashicorp.com/gpg | gpg --dearmor -o hashicorp.gpg
       sudo install -o root -g root -m 644 hashicorp.gpg /etc/apt/trusted.gpg.d/
       echo "deb [arch=$(dpkg --print-architecture)] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
       sudo apt update
       sudo apt install terraform -y
     - Luego ver si instalo bien con terraform -help





        
    
      
