# HelloBlockchain
Este es mi primer proyecto relacionado con la tecnología Blockchain. En este proyecto he creado mi primer smart contract o contrato inteligente bajo el lenguaje Solidity y el framework Truffle. También, para probarlo, he instalado el cliente Ganache, el cual actúa como una blockchain local para permitirte hacer pruebas en tu entorno local

## Cómo probarlo
* Primero, deberás clonarte este mismo proyecto con el siguiente comando: ```shell git clone https://github.com/robefernandez22/HelloBlockchain.git```
* Una vez clonado el proyecto, para poder ejecutar el mismo y probarlo, deberemos instalar truffle con el siguiente comando: ```shellnpm install truffle -g```
* Luego, te recomiendo que abras otra pestaña en la consola e instales Ganache con el siguiente comando: ```shell npm install -g ganache-cli``` y después de instalarlo, vamos a ejecutarlo con el siguiente comando: ```shell ganache-cli``` y veremos que estará a la escucha normalmente en 127.0.0.1:8545
* Ahora, iniciaremos la consola de truffle para poder compilar y desplegar nuestros proyectos, lo haremos con el siguiente comando: ```shell truffle console –network development``` (ten en cuenta que el guión antes de network es un guión largo, no corto como el que normalmente se usa)
* Estando en la consola de truffle, compilaremos nuestro proyecto con el comando compile y lo desplegaremos con el comando migrate, tras ejecutar estos comandos, observaremos que en ganache-cli ya se ha producido algún movimiento relativo al coste de gas asociado al despliegue de nuestros contratos
* Para poder ejecutar nuestro smart contract HelloBlockchain.sol, crearemos una instancia del mismo con la siguiente instrucción: ```shell const instance = await HelloBlockchain.deployed()```
* Ahora, tras declarar la anterior instancia, la podremos usar para llamar a nuestro método sayHi de la siguiente manera: ```shellinstance.sayHi.call()``` y esto nos devolverá el output "Hello Blockchain"