Capítulo 1. Introdução


Este capítulo apresenta os elementos básicos do C++: tipos, variáveis, expressões, instruções e funções. Ao longo do 
caminho, explicaremos brevemente como compilar e executar um programa.

Depois de ler este capítulo e fazer os exercícios, você será capaz de escrever, compilar e executar programas simples. Nos 
capítulos posteriores assumiremos que você pode usar os recursos apresentados neste capítulo e explicaremos esses 
recursos com mais detalhes.

A maneira de aprender uma nova linguagem de programação é escrevendo programas. Neste capítulo, escreveremos um 
programa para solucionar um problema simples para uma livraria.

Nossa loja mantém um arquivo de transações, cada uma das quais registra a venda de uma ou mais cópias de um único 
livro. Cada transação contém três elementos:

0-201-70353-X 4 24.99

O primeiro elemento é o ISBN (Insternational Standard Book Number, um identificador único de livro), o segundo é o número 
de cópias vendidas e o último é o preço pelo qual cada uma dessas cópias foi vendida. De tempos em tempos, o dono da 
livraria lê esse arquivo e, para cada livro, calcula o número de cópias vendidas, a receita total daquele livro e o preço médio 
de venda.

Para poder escrever este programa, precisamos conhecer alguns recursos básicos do C++. Além disso, precisaremos saber 
como compilar e executar um programa.

Embora ainda não tenhamos projetado nosso programa, é fácil ver que ele deve:
	• Definir variáveis;
	• Definir entrada e saída;
	• Usar uma estrutura de dados para armazenar dados;
	• Testar se dois registros têm o mesmo ISBN;
	• Contém um loop que processará todos os registros no arquivo de transação.

Começaremos revisando como resolver esses pequenos problemas em C++ e então iremos escrever nosso programa para a 
livraria.

1.1 Escrevendo um Programa C++ Simples

Todo programa C++ contém uma ou mais funções, uma das quais deve ser nomeada de main. O sistema operacional 
executa um programa C++ chamando main. Aqui está uma versão simples de main que não faz nada além de retornar um 
valor ao sistema operacional:

int main()
{
	return 0;
}

Uma definição de função tem quatro elementos: um tipo de retorno, um nome de função, uma lista de parâmetros 
(possivelmente vazia) entre parênteses e um corpo de função. Embora main seja especial em alguns aspectos, definimos 
main da mesma forma que definimos qualquer outra função.

Neste exemplo, main tem uma lista vazia de parâmetros (mostrada por () sem nada dentro). 6.2.5 discutirá os outros tipos 
de parâmetros que podemos definir para main.

A função main precisa ter um tipo de retorno int, que é um tipo que representa números inteiros. O tipo int é um tipo interno, 
o que significa que é um dos tipos que a linguagem define.

A parte final de uma definição de função, o corpo da função, é um bloco de instruções que começa com uma chave de 
abertura e termina com uma chave de fechamento:

{
	return 0;
}

A única instrução neste bloco é um return, que é uma instrução que encerra uma função. Como é o caso aqui, um return 
também pode enviar um valor de volta ao chamador da função. Quando uma instrução return inclui um valor, este deve ter um 
tipo compatível com o tipo de retorno da função. Neste caso, o tipo de retorno de main é int e o valor de retorno é 0, que é 
um int.

Observação
	Observe o ponto e vírgula no final da instrução return. Ponto e vírgula marcam o fim da maioria das instruções em C	
	++. Eles são fáceis de ignorar, mas, quando esquecidos, podem levar a misteriosas mensagens de erro do 	
	compilador.

Na maioria dos sistemas, o valor retornado de main é um indicador de status. Um valor de retorno 0 indica sucesso. Um 
retorno diferente de zero tem um significado que é definido pelo sistema.
