# Teste de PSI 1 - Turno 1 - Versão 2

## Informação do aluno

    Nome: ...

Teste termina às 10:45.

Escreve as respostas dentro dos blocos correspondentes.
Substitui as reticências pelo que é pedido em cada pergunta.
Não desformates o documento.

### P1. Indica o que é impresso pelo seguinte código. Justifica a tua resposta

    bool b = 5 < 2;
    double d = Convert.ToDouble(b);
    
    Console.WriteLine(d);

P1 - Resposta

    É impresso: 0

    Definimos que o valor da variável b equivale a '5 < 2'.
    Visto que esta é uma variável do tipo bool, apenas pode ter os valores 'true' ou 'false'. 
    Sendo que 2 não é um número maior que 5, sabemos que b = false;
    O método Convert.ToDouble permite converter outros tipos de valor em double.
    Sendo que 'false' equivale ao valor lógico '0', esse é o valor a guardar na variável d.
    O método Console.WriteLine é responsável por imprimir um tipo de valor. 
    Este valor é passado entre parênteses depois do nome do método.
    Assim sendo, o valor entre parênteses 'd' corresponde ao valor da variável de mesmo nome.

### P2. Considera o seguinte código com um *bug*

    string s = "2.5";
    double d = Convert.ToInt32(s);

    Console.WriteLine(d);

### Indica uma possível correção para que o código não apresente erros. Explica porque foi necessário fazer essa correção

P2 - Resposta

    Uma possível correção: double d = Convert.ToDouble(s);

    Apesar de ser possível converter strings para números inteiros,
    o valor da variável 's' não pode ser guardado na variável do tipo 'double'
    com a conversão "ToInt32" que é feita.
    O valor '2.5' tem uma casa decimal, logo, é um número real.
    O tipo de sistema 'Int32', que se refere a valores do tipo 'int',
    apenas contém números inteiros.
    Não é possível esta conversão ocorrer implicitamente, gerando umm erro
    que indica que a string não está no formato correto.
    A correção indicada acima altera o tipo de valor em que a string é convertida
    de 'int' para 'double'.
    Este tipo real consegue conter o valor da string, possibilitando assim que a
    conversão seja feita sem erros.

### P3. Escreve um programa que solicite ao utilizador dois números inteiros e os multiplique, apresentando o resultado. Caso este seja um número divisível por 3, deve também ser impressa a mensagem "Múltiplo de 3!"

P3 - Resposta

    // Variáveis para guardar números inteiros e resultado da multiplicação
    int i, j, resultado;

    // Pedir o primeiro número ao utilizador e guardar na variável correspondente
    Console.Write("Insere o primeiro número inteiro: ");
    i = Convert.ToInt32(Console.ReadLine());

    // Pedir o segundo número ao utilizador e guardar na variável correspondente
    Console.Write("Insere o segundo número inteiro: ");
    j = Convert.ToInt32(Console.ReadLine());

    // Guardar o resultado da multiplicação dos dois valores anteriores na variável correspondente
    resultado = i + j;

    // Imprimir resultado da multiplicação
    Console.WriteLine($"{i} * {j} = {resultado}");

    // Verificar se resultado corresponde a um número divisível por 3
    if (resultado % 3 == 0)
    {
      // Imprimir mensagem adicional
      Console.WriteLine("Múltiplo de 3!");
    }

### P4. Tens um repositório git criado localmente, onde estás no ramo 'master'. Queres associá-lo ao repositório remoto contido no url 'https://github.com/PSI/OMeuRepositorioRemotoV2'. Queres também alterar o nome do ramo atual para 'main'. Deverás enviar os *commits* já feitos localmente para o repositório remoto. Indica os comandos necessários

P4 - Resposta

    1. Adicionar repositório remoto no URL indicado ao repositório local:
        git remote add origin https://github.com/PSI/OMeuRepositorioRemotoV2

    2. Alterar o nome do ramo atual para 'main'
        git branch -M main

    3. Enviar commits locais para o repositório remoto
        git push -u origin main
