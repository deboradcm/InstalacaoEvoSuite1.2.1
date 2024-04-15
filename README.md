# Testando com EvoSuite 1.2.1
## Linux

Antes de prosseguir, verifique se você possui o compilador Java instalado executando o seguinte comando no terminal:
```
javac -version
```
Deve aparecer algo como:
`java 11.0.22`

Além disso, certifique-se de que o Maven esteja instalado em seu sistema. Você pode fazer isso executando:
```
mvn -version
```
Deve aparecer algo como:
`Apache Maven 3.6.3`

Para testar utilizando o EvoSuite, você precisa ter um projeto escrito em Java. Logo a baixo consta a sugestão de um tutorial fornecido pelo [site oficial do EvoSuite](https://www.evosuite.org/documentation/tutorial-part-1/), mas você pode utilizar um a sua escolha.

```
wget http://evosuite.org/files/tutorial/Tutorial_Stack.zip
unzip Tutorial_Stack.zip
```
```
cd Tutorial_Stack
```
Compile o projeto utilizando o Maven
```
mvn compile
```
> Observação: Se ao compilar você receber um erro relacionado a versão do Java, abra o arquivo pom.xm que está em Tutorial_Stack e acrescente ao <project></project>:
```
<build>
    <plugins>
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-compiler-plugin</artifactId>
            <version>3.8.1</version>
            <configuration>
                <source>11</source>
                <target>11</target>
            </configuration>
        </plugin>
    </plugins>
</build>
```
## Intando EvoSuite 1.2.1

Clone o repositório EvoSuite para o diretório desejado. Por exemplo, para cloná-lo dentro da pasta Tutorial_Stack, execute o seguinte comando:
```
git clone https://github.com/EvoSuite/evosuite.git
```
Para compilar e instalar o EvoSuite, navegue até o diretório do EvoSuite que você acabou de clonar:

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
java -jar ~/Tutorial_Stack/evosuite/master/target/evosuite-master-1.2.1-SNAPSHOT.jar -target /caminho/para/seu/projeto   
```
Você deve ver a seguinte mensagem indicando que o EvoSuite foi iniciado com sucesso:
`
EvoSuite 1.2.1-SNAPSHOT
`

