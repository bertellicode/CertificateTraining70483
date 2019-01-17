# CertificateTraining70483
Repository for certificate training 70-483

CHAPTER 1 - Manage program flow 

Aplicações Multithreaded -> aplicações escalaveis e responsivas.
Aplicativos que sejam fracamente acoplados usando delegates e eventos.
Estratégia robusta de tratamento de erros.

Objective 1.1: Implement multithreading and asynchronous processing

Para sistemas multicore e manter a capacidade de resposta, é necessário criar aplicativos que usem várias threads, geralmente chamado de 
paralelismo.

Entendendo threads

Cada aplicativo é executado em seu próprio processo. 
Um processo isola uma aplicação de outras aplicações, dando-lhe a sua própria memória virtual e assegurando que processos diferentes 
não podem influenciar uns aos outros. Cada processo é executado em seu próprio segmento.
O Windows deve gerenciar todos as threads para garantir que elas possam fazer seu trabalho. Cada thread é permitida pelo Windows 
para executar por um determinado período de tempo. Após esse período terminar, a thread é pausada e o Windows alterna para outra 
thread. Isso é chamado de troca de contexto(context switching).
O thread atual está usando uma determinada área da memóriaa Ela usa registradores de CPU e outros dados de estado e o Windows, que precisa 
garantir que todo o contexto da thread seja salvo e restaurado em cada switch.
O uso de thread garante que cada processo tenha seu tempo de execução sem ter que esperar até que todas as outras operações sejam concluídas.
Isso melhora a capacidade de resposta do sistema e dá a ilusão de que uma CPU pode executar várias tarefas ao mesmo tempo. Dessa forma, 
você pode criar um aplicativo que use paralelismo, o que significa que ele pode executar várias threads em diferentes CPUs em paralelo.

Usando Thread class

Esta classe permite que você criar novas Threads, gerenciar sua prioridade e obter seu status.

Listing 1-1 

Synchronization é o mecanismo para garantir que duass threads não executem uma parte específica de seu programa ao mesmo tempo. 
Duas threads não não podem ser executadas no mesmo tempo, enquanto uma thread está sendo executada, as outras terão de esperar. 

Diferença entre foreground and background threads. Threads em primeiro plano podem ser usados para manter um aplicativo ativo. 
Somente quando todos os threads em primeiro plano terminam, o common language runtime (CLR) encerra seu aplicativo. 
Threads de plano de fundo são então finalizados.
