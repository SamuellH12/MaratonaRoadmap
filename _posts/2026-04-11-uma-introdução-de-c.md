---
layout: post
title: Uma introdução de C++
date: 2026-04-11 22:04 -0300
---

## Introdução

Esse é um tutorial rápido de **programação em C++** e no básico de **lógica de programação**, focado principalemente na **programação competitiva**. A ideia é ser uma introdução para quem está começando a aprender programação agora, assim como pra quem já possui alguma experiência de programação básica, mas em outra linguagem como _python_. 

Como este é um resumo, existem _muitas_ informação que acabaram ficando de fora, mas espero que com o que você vir aqui já seja capaz de criar seus primeiros códigos e iniciar sua jornada na programação competitiva, mas saiba que há muito mais para descobrir e você pode, e deve, buscar outras fontes e tentar se aprofundar mais.


### O que é Programação? E C++? E algoritmos???

Na programação nós escrevemos **algoritmos** através de _**linguagens de programação**_, os códigos. Esses códigos são arquivos de texto comuns que são então _interpretados_ ou _compilados_, algo como"traduzidos", para instruções e comandos básicos que os computadores são capazes de entender.

Mas o que são algoritmos afinal? **Um algoritmo é definido como uma sequência de passos ou operações bem definidas que permitem solucionar um problema ou realizar uma ação**. Um comparação clássica é com uma _receita de bolo_: existe uma sequência de passos e instruções que se seguidos corretamente levam ao resultado esperado. Mas em nosso caso, essas instruções não devem conter nenhuma ambiguidade, por isso utilizamos linguagens de programação como o C++, Python, Java e etc.


### Onde programar?

Normalmente utilizamos programas como o **Visual Studio Code**, o Sublime, o Vim, entre outros. Esses são **editores de texto**, eles nos ajudam a organizar o código, detectar erros de sintaxe e agilizam a tarefa de codificar mostrando dicas, mas até o _bloco de notas_ poderia ser usado para escrever códigos.

Mas para realmente se obter um programa de computador a partir de linhas de código é necessário utilizar um **compilador**, que vai pegar seu código e transformá-lo em um programa propriamente
dito, um arquivo executável! 

Mas como instalar ou usar um compilador de C++ pode dar um pouco de trabalho pra quem ainda está começando, uma boa alternativa para já começar a praticar são os compiladores online! Basta pesquisar por _"compilador de c++ online"_ que aparecerão muitas opções. Uma boa opção (atualmente) é o [Online CPP](https://www.online-cpp.com/). É claro que em algum momento (não muito longe de agora) você vai precisar passar por esse processo. Mas isso fica pra _outro tutorial_.

## Estrutura básica

No C++ temos que respeitar um certo padrão, chamado de **Sintaxe**. A sintaxe dita quais palavras possuem quais funções e como devemos estruturar nosso código para que ele possa ser entendido pelo computador. Para iniciar nosso código temos de utilizar uma estrutura como essa aqui:

```cpp
#include <iostream>
using namespace std;

int main() {
    

    // O seu código vai aqui
    
    
}
```

Mas pra que serve isso? O que cada palavra dessas quer dizer??? Vamos por partes

O mais simples de entender é o *comentário*, esse texto `// O seu código vai aqui`. Essas duas barrinhas `//` indicam que tudo que vier depois dela nessa linha deve ser ignorado pelo computador. Isso serve somente para que o programador faça anotações no código e não faz diferença para o programa.

Agora, quanto a primeira linha: `#include <iostream>` é um comando para "**importar**" (incluir) *bibliotecas* e outras ferramentas que já estão prontas para serem usadas e que facilitam muitas etapas do código. Neste caso em particular, `<iostream>` é a biblioteca padrão de entrada e saída, que vamos explorar um pouco mais a seguir.

O `using namespace std;` é para declarar que vamos utilizar coisas do "conjunto" de ferramentas do *std*, desse "namespace", e que quando utilizarmos não precisamos dizer explicitamente que pertencem à esse namespace. Utilizamos isso apenas por comodidade, para facilitar a leitura e escrita do código. Mas não é algo com que você deva se preocupar agora.

Agora vamos para a parte *principal* do código! Nossa função principal, a `main`. Dentro da `main` estará o código que vai ser executado, isto é, entre as duas chaves `{}` é onde vamos escrever as linhas de código em si! Quando nosso programa iniciar ele vai identificar essa parte do código como a parte *principal* e os comandos que declaramos dentro da `main` serão executados linha por linha, do começo ao fim. Por isso é importante que esteja escrito exatamente dessa forma, `main`, outra palavra não vai ser identificada pelo compilador.

Ainda falta explicar o que é a palavra `int` antes de `main` e porque têm dois parenteses depois `()`, mas vou dar mais detalhes disso no final do post, por hora, abstraia essas informações. O relevante aqui é entender que essa é a estrutura básica de qualquer código em C++ e que é a partir daqui que vamos começar!

## Saída

A saída é como o nosso programa se comunica com o mundo. Onde vamos imprimir resultados, textos e tudo mais. A saída padrão no nosso caso será o **terminal**, ou *console*, onde vamos interagir com nosso programa.

Mas lembra que falamos sobre sintaxe? Nosso programa deve respeitar algumas estruturas pré-definidas da linguagem de programação que estamos utilizando. Isso inclui algumas palavras que são reservadas pela linguagem, que têm algum significado e função, como a saída, que será identificada por uma palavra e alguns símbolos. No C++ a saída padrão é o `cout`, uma junção de C++ com Output.

Vamos escrever nosso primeiro código!

```cpp
#include <iostream>
using namespace std;

int main() {

    cout << "Ola mundo!";
    
}
```

Aqui usamos `cout` para indicar que vamos fazer um comando de **saída**. Mas o que vamos *"colocar"* na saída? Com esse símbolo, ou *operador*, de "dois menor quê" `<<` dizemos que queremos "jogar" a próxima coisa na saída. A próxima coisa nesse caso é um texto! Para o programa entender que algo é realmente um texto e não confundir isso com parte do código nós usamos aspas `" "`. Tudo que estiver **entre aspas** é considerado como um texto, parecido com o *comentário* de que falamos antes. Uma última observação, sempre que finalizamos um comando, devemos colocar um *ponto e vírgula* `;` para indicar o fim daquele comando.

Experimente trocar esse texto por outras possibilidades e executar o programa para ver o resultado!

Se quisermos deixar esse código ainda melhor, podemos adicionar também um `endl` para sinalizar uma "quebra de linha" na saída, como se tivéssemos apertado enter após escrever a mensagem e pulado para a próxima linha. `endl` é a junção de "end" com "line".

```cpp
cout << "Ola mundo!" << endl;
```

> Você pode colocar várias mensagens no mesmo comando! Ou vários comandos tb. 🙃 \
> `cout << "Oi!" << endl << "Ola!" << endl;`
{: .prompt-tip }

## Variáveis e Tipos

Podemos também armazenar informações! Nós usamos variáveis para armazenar valores e usá-los mais tarde. No C++ as variáveis têm ***tipos*** que indicam que tipo de dado elas armazenam, seja um texto, um número ou um valor "booleano".

Os principais tipos do C++ são:

| Tipo       | Descrição                                                     | Exemplos                         |
| ---------- | ------------------------------------------------------------- | -------------------------------- |
| **int**    | Armazena **números inteiros**                                 | `1` `43` `-20` `1000000000`      |
| **float**  | Guarda números de **"ponto flutuante"** (com casas decimais)  | `1.99999` `0.00001` `200.5`      |
| **double** | Também **"ponto flutuante"**, mas suporta mais casas decimais | `1.99999` `0.123456789`          |
| **bool**   | Valores **booleanos**, isto é, verdadeiro ou falso            | `true` `false`                   |
| **char**   | Guarda UM **caractere de texto** do tipo ASCII, como letras.  | `'a'` `'b'` `'c'` `'1'` `'!'`    |
| **string** | Armazena um **texto**! Isto é, uma lista de `char`            | `"Ola mundo!"` `":)"` `"textos"` |

> **Alguns detalhes importantes:** \
> • Ao escrever um número `float` ou `double` use **ponto** `.` e não vírgula `,`, assim: `1.0`. \
> • Atenção que `string` utiliza "aspas duplas" `" "` enquando `char` usa 'aspas simples' `' '`. \
> • Na *programação competitiva* damos preferência pra `double` em vez de `float`, por ser mais preciso.
{: .prompt-warning }

Antes de utilizar uma variável temos que *declarar* ela, desse jeito: `tipo variavel = valor;` em que "variavel" é um nome qualquer que você queira dar pra essa variável. Além disso, o valor inicial é opcional, podendo ser só `tipo variavel;`. Vamos ver alguns exemplos:

```cpp
#include <iostream>
using namespace std;

int main() {

    string nome = "Dadinho";
    int numero = 13;
    double fracao = 2.5;
    bool sla = true;
    
    cout << "Ola, " << nome << "!" << endl;

    cout << "Sabia que " << numero << " eh um numero primo?" << endl;

    int soma = numero + 2;
}
```

Com números, também vamos querer realizar operações matemáticas! As principais operações são:

|  `+` | Adição           |
|  `-` | Subtração        |
|  `*` | Multiplicação    |
|  `/` | Divisão          |
|  `%` | Resto da divisão |

Você pode realizar operações tanto entre números (ou *literais*) como entre variáveis! Inclusive, é possível "somar" duas strings, isto é, concatenar os dois textos em um único texto! Experimente isso e veja o resultado!

> **Uma observação importante:** as operações retornam um número do mesmo tipo dos números originais! \
> Então `5.0 / 2.0 == 2.5` mas `5 / 2 == 2`, porque o número inteiro perde a parte decimal. Mas `5 % 2 == 1`, porque `1` é o resto da divisão inteira!
{: .prompt-info }

<details>
  <summary> <b>Exercícios sugeridos!</b> </summary>
  <ul>
    <li>Nenhum ainda (o_o)</li>
  </ul>
</details>

## Entrada

Certo, já sabemos como nosso programa pode enviar informações para o *mundo*, mas como ele pode **receber dados**? Esse é outro conceito fundamental, a **entrada**! 

No C++, o comando de entrada é o `cin`, junção de C++ com *input*. E aqui na entrada precisamos armazenar essas informações em algum lugar, então o comando de entrada é feito sobre uma **variável**. 

```cpp
#include <iostream>
using namespace std;

int main() {

    string nome;

    cin >> nome;
    
    cout << "Ola, " << nome << "!" << endl;

    int num1, num2;
    cin >> num1 >> num2;

    cout << "A soma desses numeros eh " << (num1 + num2) << endl;
}
```

Semelhante ao `cout`, no `cin` usamos o *operador* `>>` para indicar a variável em que será armazenada a informação. E aqui o tipo da variável também faz diferença, se você está tentando ler uma variável do tipo `int`, o programa irá esperar que o usuário insira um número, e se uma string for inserida por exemplo, poderá ocorrer um erro!  

> É no **Terminal** que irão ocorrer as interações entre o usuário e o programa, tanto operações de saída como de entrada.
> Quando uma operação de entrada ocorrer, o programa irá **parar**, **esperar** você digitar algo e então pressionar ***enter***. Só então o programa irá continuar sua execução, agora com o valor que você digitou no terminal armazenado na variável.
{: .prompt-info }

> Uma dica para memorizar! `cout` usa `<<`, como se fosse uma setinha apontando do valor para a saída, enquanto no o `cin` usa `>>`, uma setinha da entrada para a variável! Então na dúvida, pense na direção que você quer que a informação siga! Se para a **saída**, aponte para o `cout <<`. Se para a **entrada**, aponte a setinha do `cin >>` para a variável!

## Estruturas Condicionais
## Estruturas de Repetição
## Arrays
### Vetores
## Funções
### Recursão
## Utils

## Próximos passos

