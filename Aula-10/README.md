# Aula 10

## Desenvolver o Cronograma
![Desenvolver Cronograma](desenvolverCronograma.PNG)

### Caminho Crítico
Antes de descobrir se um caminho é crítico você tem que para cada atividade calcular:  
As datas de **início cedo** e **termino cedo**  
E as datas de **início tarde** e **término tarde**  

Lembrando que esses calculos são sem considerar limites de recursos.

**Caminhos críticos** são os piores caminhos do projeto. Você pode notar pelas caracteristicas do caminho crítico:  
![Caminho crítico](caminhocritico.PNG)  
Folgas são o intervalo de tempo entre uma atividade e outra. Como caminhos críticos não tem folga, ao termina uma atividade desse caminho, você deve começar outra atividade. Isso também quer dizer que se uma atividade crítica atrasar, o projeto também vai atrasar.  

Representação adotada - PDM  
![Representação PDM](representacao.PNG)

### Como calcular caminho crítico
Para começar suponha que tenha uma rede tipo essa.  
![Rede 1](rede1.PNG)  

Vamos começar calculando se começarmos todas as atividades primarias logo no primeiro dia, no tempo 0.  
Se a atividade A tem duração 6 dias e começou no dia 0, vai terminar justamente no dia 6.  
![Rede 2](rede2.PNG)  

Logo o **início cedo** é 0.  
O **término cedo** é 6.  

A atividade em seguida dessa vai começar quando essa terminar, vai durar quanto tempo ela tem que durar e vai ser calculado uma data de término cedo.  
![Rede 3](rede3.PNG)  

O que acontece se a próxima atividade for dependente de mais que uma atividade? Ela apenas começa quando todas as atividades que ela for dependente terminarem.  
Se ela é dependente de 10 atividades, 9 delas terminam no dia 1. Você ainda vai ter que esperar a com maior tempo.  
Logo a data de início cedo acaba sendo a data de término cedo da maior.  
![Rede 4](rede4.PNG)  

Terminando de calcular a rede anterior  
![Rede 5](rede5.PNG)  

Agora que sabemos quando o projeto deve terminar podemos calcular o quanto podemos "enrolar" para começar cada atividade, ou seja, o início tarde e término tarde.  
Como isso funciona, vendo que o término é dia 19 conseguimos ver que no pior caso D, H, K e M podem terminar dia 19 que ainda estaria tudo bem (D,H,K e M são todos necessários para terminar o projeto).  
Olhando H, se H pode terminar até dia 19 e demora 5 dias, quer dizer que pode enrolar até o dia 14 para começar e não estaria atrasando o projeto.  
![Rede 6](rede6.PNG)  

Se uma atividade pode enrolar até dia 9 e outra até dia 11, e essas ambas atividades só podem vem de uma mesma, quer dizer que você só pode enrolar até o menor número entre elas, ou seja, dia 9.  
Se você enrolasse até o dia 11, você estaria atrasando a outra atividade em 2 dias.  
![Rede 7](rede7.PNG)  

Com isso você consegue descobrir as "atividades críticas", são as que as datas não podem ser alteradas.  
Ou seja, a data de início cedo é igual a de início tarde **e** data de término cedo é igual a de término tarde.  
![Rede 8](rede8.PNG)  

Resolvendo aquela rede, podemos ver que o caminho crítico é aquele formado por atividades críticas.  
![Rede 9](rede9.PNG)  

### Folga total
**Folgas total** é quantos dias você pode ficar sem fazer nada naquela atividade sem que afete a duração do projeto.  
Isso é possível de calcular de varias maneiras, mas todos os resultados dão no mesmo, então escolha o que preferir.  
Se você começando o mais cedo **possível** terminaria dia 7 e começando o mais tarde **possível** terminaria dia 10, quer dizer que tem 3 dias dessa atividade pode ser atrasado.  

![Folgas](folgas.PNG)

### Folga livre
**Folga livre** é quantos dias uma atividade pode atrasar sem que afete a ativadade sucessora.  
A única diferença dela para total é 

## Compressão (crashing)
Tentar reduzir a duração de uma atividade, aumentando o número de pessoas ou aumentando os recursos ou pagando para acelerar essa atividade...  
Se fossemos pegar alguém de outra atividade, pegariamos alguém de uma atividade que tem folga.  

Normalmente se faz compressão em atividades que estão em caminho crítico.  
![Crashing](crashing.PNG)

## Paralelismo (fast tracking)
Tentar trabalhar em atividades em paralelo, isso aumenta o risco de dar erros mas tenta acelerar (nem sempre funciona).  
Se duas atividades demoram 5 dias, se começarem uma depois da outra, totaliza em 10 dias.  
Fazendo em paralelo e começando junto, teoricamente terminaria juntas, totalizando 5 dias. Mas sabemos que paralelismo causa muitos problemas.  
![Fast Tracking](fasttracking.PNG)
