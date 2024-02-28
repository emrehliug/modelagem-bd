# Modelagem de banco de dados
Em 1976 o Dr.Peter Cheng propõe o modelo entidade-relacinamento (ER) para banco de dados, dando uma nova percepção para dos conceitos de modelos de dados.
É o assunto que iremos falar nesse artigo/anotação.

## Banco de dados usando formas normais

"A normalização de banco de dados é o processo de organizar um banco de dados relacional de acordo com uma série de formas normais para reduzir a redundância de dados e melhorar a integridade dos dados."
by <a href="https://www.dio.me/articles/organizando-um-banco-de-dados-usando-as-formas-normais">Giovanni Rozza</a>

### Primeira Forma:
1 - Todo campo vetorizado se tornara outra tabela.

    Ex: [uva, maca, banana, melancia] - vetor de frutas que possivelmente será outra tabela
2 - Todo campo multivalorado se tornara outra tabela. quando o campo for divisivel. 

    Ex: uma tabela com campo endereço que contem o valor [Rua Fulado de tal - Bairro Fulano - Cep F], temos nessa tabela um campo multivalorado que pode se tornar outra tabela com campos RUA, BAIRRO, CEP.

3 - Toda tabela necessita de pelo menos um campo que indentifique todo o registro como sendo unico.

    Ex: basicamente aqui é o que chamamos de PK(Primary key) da tabela. 

Agora vamos aplicar essas 3 regras em uma tabela Cliente: 

![image](https://github.com/emrehliug/modelagem-bd/assets/44777996/ae92e839-11b7-4e8f-914e-5f6598576d46)

Analisando essa entidade entendemos que a mesma esta sem um campo unico de indentificação (fere a regra numero 3), o campo telefone pode ser vetorizado onde 1 cliente pode ter N telefones (fere regra numero 1), e por fim o campo endereço é um multivalorado, contendo toda a informação RUA-BAIRRO-CEP-UF que pode ser dividida nele mesmo.

Como corrigimos isso? simples, seguindo as 3 regras da primeira forma, como mostra a modelagem abaixo:
