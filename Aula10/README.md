# Aula 10
Vamos começar a ver processos de tempo:  
* Planejar gerenciamento de tempo  
* Definir atividades  
* Sequênciar atividades  
* Estimar recursos de atividades  
* Estimar duração de atividades  
* Desenvolver cronograma  

## Planejar o Gerenciamento do Tempo
![Planejar Gerênciar Tempo](planejarGerTempo.PNG)

Tem a função de decidir/criar o plano para gerênciar o cronograma, ou seja, as regras para você criar tudo relacionado a tempo. Nele você decide:  
* O modelo do cronograma
* Nível de precisão das durações
* Unídade de medida de tempo (dia/mês/hora/minuto)
* As regras de medição de desempenho
 
Na EAP, nós não obdecemos nenhuma ordem lógica de trabalho, apenas listamos pacotes e atividades. Nós iremos botar em ordem lógica quando estivermos em "Sequenciar atividades".  

## Definir Atividades
As ações que precisam ser feitas para se completar pacotes de trabalho que vão produzir as entregas do projeto.  
Com base nos pacotes de trabalhos da EAP, nós listamos as atividades necessárias para fazer o futuro cronograma.  
![Atividades](atividades.PNG)

Nessa imagem aquele subproduto é como se fosse um pacote.

## Sequênciar Atividades
Depois de lista as atividades, precisamos sequênciar elas, botar em uma ordem lógica. A ordem em que vai ser feito.  
Isso nos ajuda a ver que atividade precisa que outra seja feito primeiro, ou quais podem ser feito em paralelo.  
![Sequência das Atividades](sequencia.PNG)

### Diagrama de rede
Um diagrama que além de mostrar a ordem que precisa ser feito, mostra quais são dependentes das outras atividades.  
![Diagrama de Rede](diagramaRede.PNG)

Outra maneira que esse diagrama pode ser representado é por uma tabela.  
![Tabela de Diagrama de Rede](tabelaRede.PNG)

### Dependências
Existe 3 tipos de dependências:  

**Dependências Obrigatórias**:  
Uma atividade depende da outra para começar.  
![Dependência obrigatória](depObrigatoria.PNG)  
Só pode testar o código depois que escrever ele.  

**Dependências Arbitradas**:  

![Dependência arbitradas](depArbitradas.PNG)  

**Dependências Externas**:  
