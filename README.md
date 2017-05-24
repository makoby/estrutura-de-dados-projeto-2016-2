# Projeto Estrutura de Dados

## Professor: Tiago Maritan

#### Especificação	do	Projeto	da	Disciplina		
##### Proposta:	Codificador	de	Huffman

Em	 arquivos	 de	 texto	 (ou	 em	 linguagens	 de	 programação)	 que	 utilizam	 a	 codificação	 de
caracteres	ASCII,	todos	os	caracteres	são	representados	por	códigos	de	8	bits,	independente
da	frequência	de	ocorrência	de	cada	caractere.	Nesse	caso,	o	caracter	'a',	por	exemplo,	que
tende	a	ocorrer	de	forma	muito	frequente	(em	um	texto	de	língua	portuguesa,	por	exemplo)
no	texto,	receberia	um	código	de	8	bits,	assim	como	o	caracter	'z',	que	tem	usualmente	uma
probabilidade	de	ocorrência	bem	menor	do	que	o	'a'.		

Para	 endereçar	 esse	 problema,	 o	 Algoritmo	 de	 Huffman	 tem	 como	 ideia	 central	 a
associação	de	códigos	binários	com	menos	bits	para	os	caracteres	mais	usados	num	texto,	e
de	 códigos	 binários	 com	 mais	 bits	 aos	 caracteres	 menos	 usados,	 possibilitando	 a	 sua
compactação/compressão.	Com	isso,	ele	possibilita	a	compressão	de	textos	na	proporção	de
até	3:1.	Em	outras	palavras,	ele	é	capaz	de	reduzir	o	tamanho	do	arquivo	em	até	1/3	do	seu
tamanho	original.

O	 algoritmo	 de	 Huffman	 tem	 por	 objetivo	 a	 construção	 de	 uma	 árvore	 binária	 baseada	 na
frequência	 do	 uso	 destas	 letras	 de	 modo	 que	 as	 mais	 frequentemente	 usadas	 apareçam
mais	perto	da	raiz.	Ele	consiste	basicamente	em	três	fases:

1. Calculo	da	frequência	de	ocorrência	de	cada	caracter	no	arquivo;
2. Construção	de	uma	árvore	binária,	denominada	árvore	de	Huffman;
3. Codificação	dos	caracteres	com	base	na	árvore	de	Huffman.

A	 árvore	 binária	 de	 Huffman	 é	 construída	 de	 baixo	 para	 cima	 (das	 folhas	 para	 raiz),
começando	a	partir	das	letras	menos	usadas	até	atingir	a	raiz.	Em	cada	passo	do	algoritmo,
existe	uma	coleção	de	árvores	de	Huffman.	No	início,	cada	uma	das	letras	forma	uma	árvore
que	 é	 composta	 apenas	 pela	 raiz	 e	 cujo	 conteúdo	 é	 a	 frequência	 (f)	 com	 que	 esta	 letra
ocorre	 no	 texto.	 Em	 seguida,	 são	 escolhidas	 as	 duas	 árvores	 com	 as	 menores	 frequências
associadas	e	elas	são	unidas	em	uma	só	árvore	cujo	valor	da	raiz	é	a	soma	do	valor	destas
duas.	Este	processo	é	repetido	até	a	existência	de	uma	única	árvore.

Maiores	informações	sobre	o	algoritmo		de	Huffman	podem	ser	encontradas	em:		

- [Codificação Huffman](http://www.inf.ufes.br/~pdcosta/ensino/2009-1-estruturas-de-dados/material/CodificacaoHuffman.pdf)
- [unicamp / Huffman](http://www.ic.unicamp.br/~rtorres/mc326A_06s2/lab2/enunc.html)

Implemente	um	Codificador	baseado	no	Algoritmo	de	Huffman	para	arquivos	de	textos.	Esse
codificador	deve	possuir	as	seguintes	características:		

1. Receber	um	arquivo	de	texto	como	entrada;
2. Calcular	a	probabilidade	de	ocorrência	de	cada	caracter	do	texto;
3. Gerar	a	árvore	de	Huffman	desse	arquivo	e		
4. Exibir	a	codificação	de	Huffman	para	cada	um	dos	caracteres	do	texto.

Em	seguida,	utilize	a	mesma	Árvore	de	Huffman	para	realizar	o	processo	de	decodificação.
Esse	 processo	 consiste	 em	 consultar	 os	 códigos	 de	 Huffman,	 e	 percorrer	 a	 árvore	 de
Huffman	para	descobrir	que	caracter	está	relacionado	a	um	determinado	código.		

Você	deve	entregar	o	código-fonte	do	projeto	e	um	relatório	de	1	ou	2	páginas	explicando,
de	forma	geral,	as	principais	funções	do	sistema.

Bom	trabalho!
