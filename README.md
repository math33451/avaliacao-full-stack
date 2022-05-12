# Versões das ferramentas
Java 11, SpringBoot, Vue 5.

Optei por uma interface um pouco mais simples, devido não ter tanta familiaridade com o frontend.
A tratativa de erros foi melhor elaborada no backend, mas não a coloquei para ser exibida no frontend, então optei por um alert mais simples.

# Instruções para subir o projeto

Com o eclipse, o backend pode subir normalmente como uma aplicação java, certifique-se de que sua porta 8081 esteja livre, pois ele está setado para ela.
O frontend pode ser executado com o npm, certifique-se de que sua porta 8080 esteja livre.

Pode acessar o frontend pelo navegador usando o endereço http://localhost:8080


# Detalhes da Avaliação

Desenvolver tanto a API quanto o front-end (Spring boot e Vue no front, caso não tenha conhecimentos de vue, aceitamos o front com angular)

O objetivo dessa tarefa é avaliar como você vai desenvolver o código em termos de estilo,
eficiência, qualidade e prazo de entrega.

A tarefa é a seguinte:

Desenvolver um sistema de agendamento de transferências financeiras.

1) O usuário deve poder agendar uma transferência financeira com as seguintes
 informações:
 Conta de origem (padrão XXXXXX)
 Conta de destino (padrão XXXXXX)
 Valor da transferência
 Taxa (a ser calculada)
 Data da transferência (data que será realizada a transferência)
 Data de agendamento (hoje)
 
2) Cada tipo de transação segue uma regra diferente para cálculo da taxa

 A: Tranferências no mesmo dia do agendamento tem uma taxa de $3 mais 3% do valor a
ser transferido;

B: Tranferências até 10 dias da data de agendamento possuem uma taxa de $12.

C: Operações do tipo C tem uma taxa regressiva conforme a data de
transferência:

 acima de 10 dias da data de agendamento 8.2%
 
 acima de 20 dias da data de agendamento 6.9%
 
 acima de 30 dias da data de agendamento 4.7%
 
 acima de 40 dias da data de agendamento 1.7%
 
 D: Operações do tipo D tem a taxa igual a A, B ou C dependendo do valor da
transferência.

 Valores até $1.000 seguem a taxação tipo A
 
 Valores de $1.001 até $2.000 seguem a taxação tipo B
 
 Valores maiores que $2.000 seguem a taxação tipo C
 
Obs: Caso não haja taxa aplicável, lançar um alerta sobre o erro.

3) O usuário deve poder ver todos os agendamentos cadastrados.

Nota: A persistência deve ser feita em banco de dados em memória (h2, por exemplo).
