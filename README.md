# rabbitmq1
ambiente rabbitmq para envio de mensagem do produtor para os trabalhadores.
esse ambiente é uma criação do próprio site da aplicação Rabbitmq que é um message broker 
de código aberto que implementa o protocolo AMQP que facilita a comunicação assíncrona entre
as aplicações e serviços. No site do Rabbitmq possui uma seção Get started e dentro dela Work Queues
e foi dessa seção que foi feito esse trabalho em uma aula de Sistemas Distribuídos na UFC campus Itapajé
nesse trabalho foi criado um arquivo para os "trabalhadores" que é o worker.py que nele foi implementado
um código que faz com que receba um "trabalho" do arquivo new_task, para isso foi-se necessário a instalação
do Conda e do Rabbitmq. Utilizaremos o conda para criar um ambiente no computador para conseguirmos enviar a 
task para o worker, o diferencial dessa troca é que foi utilizado mais de um worker para observarmos que 
quando estamos em um sistema distribuído existe uma separação de tarefas onde o new_task irá distribuir 
as tarefas dentre os demais workers, ou seja, se utilizarmos 5 workers e 10 tarefas cada worker receberá 
2 tarefas. Para conseguirmos isso foi necessário a criação de um ambiente conda junto do rabbitmq, a criação
dos arquivos new_task e worker ambos na linguagem python, mas, pode-se utilizar outra linguagem. Após a 
finalização dos códigos de cada arquivo foi-se necessário a criação de alguns ambientes utilizando
um prompt para cada ambiente, eu utilizei 6 ambiente 1 para new_task e 5 para workers no qual foram ativados
os 5 workers primeiro para estarem prontos para o envio das tasks, após ativação dos 5 foi enviado 10 tasks
através do new_task e cada worker recebeu 2 mensagens. 
