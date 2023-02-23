# aws-helloworld-node-development
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
- name: Install nvm
  ansible.builtin.shell: >
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
- Una vez realizado esto nos vamos  a la carpeta nvm para instalar node:
  args:
    creates: "{{ ansible_env.HOME }}/.nvm/nvm.sh"
- En carpeta para descargar node usamos este comando:
    nvm install --lts
- Realizamos estos comandos:
    /home$ sudo mkdir logs
    sudo curl -sL https://github.com/DavidHormigoRamirez/aws-helloworld-node/archive/master.zip -- output master.zip
- Descomprimimos la app con el comando:
    unzip master
- Instalamos la app:
    sudo mv aws-helloworld-node-master/ app
    cd app
    npm install
- Por último para iniciar la app usamos:
    npm start
- Y para verlo usamos:
    curl localhost:8080
