# Modelagem de banco de dados
Em 1976 o Dr.Peter Cheng propõe o modelo entidade-relacinamento (ER) para banco de dados, dando uma nova percepção para dos conceitos de modelos de dados.
É o assunto que iremos falar nesse artigo/anotação.

## Banco de dados usando formas normais

"A normalização de banco de dados é o processo de organizar um banco de dados relacional de acordo com uma série de formas normais para reduzir a redundância de dados e melhorar a integridade dos dados."
by Giovanni Rozza

### Primeira Forma:
1 - Todo campo vetorizado se tornara outra tabela.

    Ex: [uva, maca, banana, melancia] - vetor de frutas que possivelmente será outra tabela
2 - Todo campo multivalorado se tornara outra tabela. quando o campo for divisivel. 

    Ex: uma tabela com campo endereço que contem o valor [Rua Fulado de tal - Bairro Fulano - Cep F], temos nessa tabela um campo multivalorado que pode se tornar outra tabela com campos RUA, BAIRRO, CEP.

3 - Toda tabela necessita de pelo menos um campo que indentifique todo o registro como sendo unico.

    Ex: basicamente aqui é o que chamamos de PK(Primary key) da tabela. 

