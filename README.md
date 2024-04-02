# Instalaçao EvoSuite1.2.1

## Verificar versão do Java Compiler

Antes de prosseguir, verifique se você possui o compilador Java instalado executando o seguinte comando no terminal:

```
javac -version
```
## Verificar a instalação do Maven

Além disso, certifique-se de que o Maven esteja instalado em seu sistema. Você pode fazer isso executando:
```
mvn -version
```

## Clonar o repositório EvoSuite
Clone o repositório EvoSuite para o diretório desejado. Por exemplo, para cloná-lo dentro de uma pasta chamada Tutorial_Stack, execute o seguinte comando:
```
git clone https://github.com/EvoSuite/evosuite.git
```
## Compilar e instalar o EvoSuite
Navegue até o diretório do EvoSuite que você acabou de clonar:
```
cd Tutorial_Stack/evosuite
```
Em seguida, execute os seguintes comandos para compilar e instalar o EvoSuite usando o Maven:
```
mvn package
mvn install
```
## Executar o EvoSuite
Por fim, execute o EvoSuite com o seguinte comando:
```
java -jar ~/Tutorial_Stack/evosuite/master/target/evosuite-master-1.2.1-SNAPSHOT.jar
```
Você deve ver a seguinte mensagem indicando que o EvoSuite foi iniciado com sucesso:
```
EvoSuite 1.2.1-SNAPSHOT
```

