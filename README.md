#Converter Automato Finito Não Determinístico em Automato Finito Determinístico#

No arquivo ```automato.cpp``` está implementado uma classe chamada AFN 

##Para declarar um automato:##
```AFN automato;``` 

##É necessário setar os seguintes parametros:##

```automato.addEstados("q1,q2,q3");
automato.setEstadoInicial("q1");
automato.addEstadosFinais("q2");
automato.addSimbolos("0,1,*");
//O Símbolo * simboliza o vázio (Ø)
```

##Para incluir uma transição:##
```
automato.addTransicao("q1","q2","1");
```

##Transformar o AFN para AFD basta chamar a função 
```
automato.converter();
```

##Será mostrado os estados e as suas transições como no exemplo:
``` 
*{ q1, q2 } (0) = {q1, q3}
*{ q1, q2 } (1) = {q1, q2, q3}
*{ q1, q2, q3 } (0) = {q1, q3}
*{ q1, q2, q3 } (1) = {q1, q2, q3}
->{ q1 } (0) = {}
->{ q1 } (1) = {q1, q2}
{ q1, q3 } (0) = {q3}
{ q1, q3 } (1) = {q1, q2}
{ q3 } (0) = {q3}
{ q3 } (1) = {q1, q2}
```
##Do it yourself
Para modificar as entradas será necessário modificar o código ```automato.cpp```. Segue alguns exemplos no arquivo ```exemplos.txt```. 
Obs: será necessário compilar novamente.