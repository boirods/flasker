# flasker
Seguindo o tutorial do flask para a criação de um blog simples, mas com autenticação, banco de dados e um pouco mais...

## Para executar o projeto faça os seguintes passos:
1. Provavelmente já possui o python instalado, se tiver também instale o pip (possívelmente há como instalar neste link https://pypi.org/project/pip/)
2. Intale o venv para geração de ambientes de desenvolvimento para isso execute 
~~~
pip install virtualenv
~~~
3. Após isso pode criar seu ambiente virtual com o comando abaixo, na linha abaixo criei meu ambiente com o nome devenv, mas voce pode no lugar de devenv escrever da melhor forma que preferir (prefira nomes curtos por serem mais faceis e rapidos de digitar).
~~~
virtualenv devenv
~~~
4. Ative seu ambiente com o comando abaixo:
~~~
source devenv/bin/activate
~~~
5. após isso precisamos exportar algumas variaveis de ambiente, e para isso criei um arquivo .sh para executar o meu projeto, segue codigo abaixo, mas agora vou tentar explicar. Primeiro precisamos da variavel com o nome do nosso aplicativo (que no meu caso dei o mesmo nome do tutorial do flaskr ali na primeira linha). E segundo (na segunda linha) precisamos da variavel com o tipo de ambiente em que estamos executando nosso projeto, no meu caso em desenvolvimento, caso queira por em produção já seria outra coisa que tenho que procurar. E em terceiro temos como queremos executaro nosso projeto, o flask run roda o projeto (e aplicativo) o --host diz que qualquer ip na rede pode acessar (deixo assim para testar se o estilo está legal também em celular) e o --port eu declaro a porta que quero acessar (pode-se colocar qualquer numero, mas prefira numeros altos pois você pode prejudicar a execução de outro aplicativo que esteja usando a porta que você escolheu).

~~~shell
export FLASK_APP=flaskr
export FLASK_ENV=development
flask run --host 0.0.0.0 --port 5000
~~~