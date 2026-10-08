Síntese Teórica (Pesquisa):
Explique, com suas palavras, a diferença entre Processo e Thread.
# Processo e Threads:

Um processo pode ser entendido como um programa em execução e como um agrupamento dos recursos necessários para que esse programa funcione. Baseado na aula 7, o processo possui espaço de endereçamento, uma linha de execução, resentado por uma thread. Entre os recursio de um processo estão o código e os dados do programa, arquivos abertos e outras informações utilizadas pelo sistema operacional.

Uma Thread, representa uma linha de execução dentro de um processo. No processo pode possuir várias threads, permitindo que diferentes atividades sejam executadas de maneira concorrente. As Threads, representam as linhas de execução do programa. Um processo pode ter apenas uma Threads ou várias Threads executando tarefas ao mesmo tempo. As Threads de um processo compartilham o espaço de endereçamento e diversos recursos do processo, possuindo informações próprias para controlar a sua execução, como contados de programa(PC), registradores e pilha.

Em outros materias como o da microsft, define o processo como a estrutura possui o espaço virtual, o código e recursos do sistema. Já as Thread, ele define sendo unidades que podem ser escalonadas para receber o tempo de processamento.

### Porque as threads são mais leves para o Sistema Operacional?

As Threads de um processo, vão compartilhar o espaço de endereçamento. Dessa forma, várias Threads irão utilizar o mesmo código, dados globaise outros recursos do processo, enquanto cada thread deixa suas informaçõe particulares de execução, como sua pilha e seus registradores. Com isso, vai reduzir o custo de criação e o gerenciamento comparado á criação de vários outros processos. Threads no modo geral, são mais rápidas de criar e destruir que processos.

No caso, se 100.00 usuários entrarem no site no momento da abertura das vendas. Para tratar das solicitações simultaneas, uma abordagem de processos será usada para criar uma grande quantidade de processos independentes. Cada processo terá seu espaço de endereçamento e estruturas de gerenciamento, aumentando o consumo de recursos e o trabalho do sistema operacional. Utilizando as Threads, as linhas de execução serão organizadas dentro de processos servidores, para que, elas compartilhem o espaço de endereçamento do processo e evitando manter um espaço de endereçamento completamente independente para cada linha.

# Threads em modo usuário e modo kernel

Threads em modo usuário
As threads no modo usuário serão implementadas normalmente por meio de uma biblioteca de execução. A criação, a exclusão e o escalonamento dessas Threads podem ocorrer sem que o kernel tenha conhecimento individual de cada uma delas.

Threads em Modo Núcleo (Kernel)
Nas Threads em Modo Núcleo, o próprio Sistema Operacional possui informações sobre as Threads e participa diretamente do seu gerenciamento e escalonamento.


### Comparação entre Threads em Modo Usuário e Modo Núcleo

| Característica | Modo Usuário | Modo Núcleo (Kernel) |
|---|---|---|
| **Gerenciamento** | Biblioteca ou ambiente de execução | Sistema Operacional |
| **Kernel conhece as Threads individualmente?** | Não necessariamente | Sim |
| **Escalonamento** | Feito no espaço do usuário | Feito pelo kernel |
| **Custo de gerenciamento** | Geralmente menor | Geralmente maior |
| **Bloqueio de uma Thread** | Pode afetar outras Threads, dependendo da implementação | Outras Threads podem continuar executando |
| **Paralelismo em múltiplos processadores** | Depende do modelo utilizado | Suportado diretamente pelo escalonamento do kernel |