<h2><a href= "https://www.mackenzie.br">Universidade Presbiteriana Mackenzie</a></h2>
<h3><a href= "https://www.mackenzie.br/graduacao/sao-paulo-higienopolis/sistemas-de-informacao">Sistemas de Informação</a></h3>


<font size="+12"><center>
*&lt;Fast Delivery Tech&gt;*
</center></font>

**Conteúdo**

- [Autores](#nome-alunos)
- [Descrição do projeto](#introdução-do-projeto)
- [Análise de requisitos funcionais e não-fucionais](#descrição-dos-requisitos)
- [Diagrama de casos de uso](#diagrama-de-comportamento-atores)
- [Descrição dos casos de uso](#descrição-das-funcões)
- [Diagrama de sequencia](#diagrama-de-ordem-interações) 
- [Diagrama de classes](#diagrama-orientado-objetos) 
- [Diagrama de componentes](#diagrama-estrutura-componente) 
- [Decisões de arquitetura](#decisões-de-arquitetura) 
- [Diagrama de implantação](#diagrama-de-hardware-software) 
- [Referências](#referências) 

# Autores

* João Pedro Lopes Mendes TIA: 32211694 

# Descrição do projeto

Este projeto visa criar um sistema de gerenciamento de entrega de pizza para a Pizza-Express, uma cadeia de 40 lojas de fast-food e entrega em casa. Esse sistema busca otimizar o processo de preparo e entrega no prazo de 15 minutos, tornando-o mais eficiente e permitindo que a Pizza-Express compita melhor no mercado de entrega de pizzas, com o objetivo de reduzir o tempo de entrega e melhorar a satisfação do cliente.

# Análise de requisitos funcionais e não-funcionais

*Requisitos funcionais do sistema:
- O sistema deve ser capaz de registrar os pedidos de pizza dos clientes e seus cancelamentos.
- O sistema deve ser capaz de registrar a localização do cliente.
- O sistema deve identificar a loja de Pizza-Express mais próxima da localização do cliente.
- O sistema deve calcular o tempo estimado de entrega com base na localização do cliente, da loja e nas condições de trânsito para realizar a entrega no prazo entre 10 a 15 minutos.
- O sistema deve encaminhar os pedidos para a loja Pizza-Express apropriada de acordo com a localização do cliente.
- O sistema deve gerenciar o estoque de ingredientes, incluindo a contagem de itens e a solicitação automática de reposição quando necessário.
- O sistema deve rastrear o processo de preparação de pizzas, incluindo o tempo de cozimento, a montagem e a qualidade do produto final.
- O sistema deve auxiliar na alocação de pessoal para a preparação de pedidos.
- O sistema deve gerar relatórios sobre o desempenho de cada loja da Pizza-Express, como o tempo médio de preparação e número de pedidos atendidos.
- O sistema deve enviar notificações para os clientes sobre o status do pedido, incluindo a preparação, saída para entrega e entrega concluída, sendo capazes de rastrear o status dos pedidos em tempo real.
- O sistema deve permitir a comunicação entre a central e os entregadores para atualizações e direções de entrega.

*Requisitos não funcionais do sistema:
- Segurança: O sistema deve ser protegido contra ataques cibernéticos e garantir a segurança dos dados sensíveis do cliente, como as informações de pagamento.
- Eficiência: O sistema deve ser capaz de lidar com um grande volume de pedidos simultâneos.
- Tempo de Resposta: Respostas rápidas às solicitações do cliente e atualizações em tempo real.
- Escalabilidade: O sistema deve ser escalável para acomodar o crescimento futuro do negócio.
- Usabilidade: A interface do usuário deve ser amigável e intuitiva


# Diagrama de casos de uso


[<img src="https://raw.githubusercontent.com/Joomendes/UML-Engenharia-software/blob/patch-1/docs/diagramacasosdeuso.png" alt="Diagrama de casos de uso" width=800px>](https://github.com/Joomendes/UML-Engenharia-software/blob/patch-1/docs/diagramacasosdeuso.png?raw=true)

*Atores:
- Cliente: Representa os clientes que interagem com o sistema para fazer pedidos e acompanhar o status das entregas.
- Funcionário da loja de pizza Pizza-Express: Representa os funcionários responsáveis por preparar os pedidos e verificam o estoque de ingredientes.
- Central: Representa os gerentes da Pizza-Express que  têm acesso aos relatórios de desempenho.
- Entregador: Representa os entregadores responsáveis por retirar os pedidos nas lojas e entregar os pedidos aos clientes.

*Casos de Uso:
- Fazer Pedido (Cliente):
O cliente faz um pedido, selecionando opções de pizza, inserindo detalhes e endereço de entrega.
Associações: Cliente -> Fazer Pedido
Include: Calcular Tempo de Entrega
Extend: Cancelar Pedido

- Cancelar Pedido (Cliente):
O cliente cancela o pedido.
Associações: Cliente -> Cancelar Pedido

- Acompanhar Pedido (Cliente):
O cliente verifica o status do pedido em tempo real.
Associações: Cliente -> Acompanhar Pedido

- Calcular Tempo de Entrega (Cliente):
 O cliente tem a informação de quanto tempo falta para receber seu pedido.
Associações: Cliente -> Calcular Tempo de Entrega

- Acompanhar Pedido (Central):
A central atualiza o status do pedido em tempo real para o cliente.
Associações: Central -> Acompanhar Pedido

- Calcular Tempo de Entrega (Central):
A central calcula o tempo de entrega do pedido baseado na localização do cliente.
Associações: Central -> Calcular Tempo de Entrega

- Calcular Tempo de Preparo (Central):
A central calcula o tempo de entrega de preparo do pedido do cliente.
Associações: Central -> Calcular Tempo de Preparo

- Gerenciar Estoque (Central):
A central gerencia o estoque da loja.
Associações: Central -> Gerenciar Estoque

- Direções de Entrega de Pedido (Central):
A central informa que o pedido pode ser retirado para o entregador junto com o endereço do cliente.
Associações: Central -> Direções de Entrega de Pedido

- Relatórios de Desempenho das Lojas (Central):
A central gera relatórios sobre o desempenho das lojas de pizzas.
Associações: Central -> Relatórios de Desempenho das Lojas

- Preparar Pedido (Funcionário):
O funcionário da loja de pizza recebe a ordem da central e prepara os pedidos.
Associações: Funcionário -> Preparar Pedido

- Gerenciar Estoque (Funcionário):
O funcionário verifica o estoque de ingredientes para preparar os pedidos.
Associações: Funcionário -> Gerenciar Estoque

- Direções de entrega de pedido (Entregador):
O Entregador é responsável por pegar os pedidos prontos nas lojas de pizza e entregá-los aos clientes.
Associações: Entregador -> Direções de Entrega de Pedido


# Descrição dos casos de uso

[<img src="https://raw.githubusercontent.com/Joomendes/UML-Engenharia-software/blob/patch-1/docs/casodeuso1.png" alt="Especificação de caso de uso:" width=800px>](https://github.com/Joomendes/UML-Engenharia-software/blob/patch-1/docs/casodeuso1.png?raw=true)

- Identificador:UC001
- Nome: Sistema Fast Delivery Tech
- Atores: Cliente, Funcionário, Central, Entregador
- Sumário: O sistema permite que o cliente faça pedidos de pizza e acompanhe seu pedido, que a central busque a loja mais próxima ao cliente, calcule o tempo de entrega, gerencie o estoque e gere relatórios, os - funcionários das lojas de pizzas preparem o pedido e que os entregadores realizem as entregas.

[<img src="https://raw.githubusercontent.com/Joomendes/UML-Engenharia-software/blob/patch-1/docs/casodeuso2.png" alt="Fluxo Principal:" width=800px>](https://github.com/Joomendes/UML-Engenharia-software/blob/patch-1/docs/casodeuso2.png?raw=true)

- 1.O cliente inicia o processo de pedido selecionando a opção "Fazer Pedido".
- 2.O sistema exibe um menu de pizzas disponíveis.
- 3.O cliente seleciona as opções desejadas, incluindo tipo de pizza, tamanho e ingredientes extras.
- 4.O cliente insere o endereço de entrega.
- 5.O sistema calcula o tempo estimado de entrega com base na localização do cliente e da loja de pizza mais próxima.
- 6.O pedido é registrado no sistema.
- 7.O sistema encaminha o pedido para a loja de pizza mais próxima.
- 8.O funcionário da loja recebe o pedido e prepara a pizza de acordo com as especificações.
- 9.O funcionário atualiza o status do pedido no sistema à medida que avança no processo de preparação.
- 10.Quando o pedido estiver pronto, o sistema encaminha o pedido ao entregador.
- 11.O entregador recebe o pedido pronto na loja.
- 12.O entregador verifica o endereço de entrega no pedido e parte para a entrega.
- 13.O entregador entrega o pedido ao cliente e atualiza o status do pedido como entregue.
- 14.A central gera relatórios de desempenho do sistema para monitorar o tempo médio de preparação, número de pedidos atendidos e outros indicadores relevantes.


[<img src="https://raw.githubusercontent.com/Joomendes/UML-Engenharia-software/blob/patch-1/docs/casodeuso3.png" alt="Fluxo Alternativo 1: Cliente cancela o pedido:" width=800px>](https://github.com/Joomendes/UML-Engenharia-software/blob/patch-1/docs/casodeuso3.png?raw=true)

- 3.1.1 O cliente seleciona a opção "Cancelar Pedido".
- 3.1.2 O sistema cancela o pedido do cliente, suspendendo as operações relacionadas a ele.

# Diagrama de sequencia

[<img src="https://raw.githubusercontent.com/Joomendes/UML-Engenharia-software/blob/patch-1/docs/diagramasequencia.png" alt="Diagrama de Sequência" width=800px>](https://github.com/Joomendes/UML-Engenharia-software/blob/patch-1/docs/diagramasequencia.png?raw=true)

# Diagrama de classes

[<img src="https://raw.githubusercontent.com/Joomendes/UML-Engenharia-software/blob/patch-1/docs/diagramaclasses.png" alt="Diagrama de Classes" width=800px>](https://github.com/Joomendes/UML-Engenharia-software/blob/patch-1/docs/diagramaclasses.png?raw=true)

# Diagrama de Componentes

[<img src="https://raw.githubusercontent.com/Joomendes/UML-Engenharia-software/blob/patch-1/docs/diagramacomponentes.png" alt="Diagrama de Componentes" width=800px>](https://github.com/Joomendes/UML-Engenharia-software/blob/patch-1/docs/diagramacomponentes.png?raw=true)

# Decisões de Arquitetura

<h3>Diagrama de Casos de Uso:</h3>
- O Diagrama de Casos de Uso representa as interações entre os atores e o sistema, sendo que os atores essenciais são os clientes, os funcionários da loja, os entregadores e a central de pedidos. Os casos de uso identificados incluem "Fazer Pedido", "Cancelar Pedido", "Acompanhar Pedido", "Calcular Tempo de Entrega", "Acompanhar Pedido", "Calcular Tempo de Preparo", "Direções de Entrega de Pedido", "Relatórios de Desempenho das Lojas" e "Preparar Pedido". 
Tais atores e casos identificados representam como a Fast Delivery Tech enxerga a interação entre usuários e o sistema, abrangendo todas as funcionalidades essenciais para um serviço de entrega de pizza dentro do âmbito dos 15 minutos prometidos. 
<h3>Diagrama de Sequência:</h3>
- O Diagrama de Sequência descreve a interação entre objetos ao longo do tempo. Para o sistema de pedidos de pizza, foram identificadas sequências como o processo de registro de pedidos, preparação de pizza, entrega e geração de relatórios de desempenho. A decisão é de priorizar a eficiência e aclareza nas interações entre os atores, considerando que o tempo de 15 minutos é o fator chave do projeto, garantindo que o sistema da Fast Delivery respondesse de maneira eficaz às ações dos usuários.
<h3>Diagramas de Classes:</h3>
- As classes modeladas para o sistema foram "Pedido", "Cliente", "MenuPizza", "Loja", "Funcionário", "Entregador", "Central" e "Relatório". 
Cada classe modelada desempenha um papel no funcionamento do sistema da Fast Delivery Tech, de forma que o objetivo principal de 15 minutos seja alcançado.
<h3>Diagrama de Componentes:</h3>
- O Diagrama de Componentes representa a estrutura física do sistema, identificando os principais componentes e suas interações. A decisão foi tomada para modularizar o sistema, destacando componentes como "Cliente Interface", "MenuPizza Interface", "Entregador Interface", "Módulo Cliente", "Módulo de MenuPizza", "Módulo de Pedido" e "Módulo de Loja".
<h3>Diagrama de Implantação:</h3>
- O Diagrama de Implantação descreve como o sistema será implantado em hardware físico. 
A decisão foi tomada para garantir que o sistema seja acessível a partir de qualquer navegador web, incluindo em dispositivos móveis. A arquitetura adotada suporta essa acessibilidade, enquanto medidas de segurança, como criptografia, são implementadas para proteger a integridade dos dados sensíveis dos clientes, dos funcionários, dos entregadores e das lojas. 
Para garantir a segurança na manipulação de dados e interações com o banco de dados SQL, a decisão foi utilizar a biblioteca SQLAlchemy, que oferece uma camada de abstração de alto nível e recursos integrados para prevenir vulnerabilidades, como injeção de SQL, por meio da adoção de práticas recomendadas e parâmetros seguros em consultas SQL. 
Além disso, boas práticas de segurança de WEB Servers, como a proteção contra ataques XSS (Cross-Site Scripting), foram incorporadas ao sistema. Isso envolve a implementação de validação de entrada de dados, a utilização de sanitizadores para prevenir a execução de scripts maliciosos inseridos por potenciais invasores, e a adoção de headers HTTP apropriados, como Content Security Policy (CSP), para mitigar os riscos associados a scripts não autorizados.

# Diagrama de Implantação

[<img src="https://raw.githubusercontent.com/Joomendes/UML-Engenharia-software/blob/patch-1/docs/diagramaimplantacao.png" alt="Diagrama de Implantação" width=800px>](https://github.com/Joomendes/UML-Engenharia-software/blob/patch-1/docs/diagramaimplantacao.png?raw=true)

# Referências

<ul>
  <li>Todo o material disponibilizado pelo professor Rodrigo Silva na plataforma educacional Moodle.</li>
  <li>https://www.lucidchart.com/pages/pt/o-que-e-diagrama-de-classe-uml; Acessado em 31 de outubro de 2023.</li>
  <li>https://www.ibm.com/docs/pt-br/rsas/7.5.0?topic=structure-class-diagrams; Acessado em 31 de outubro de 2023.</li>
  <li>https://www.ionos.es/digitalguide/paginas-web/desarrollo-web/diagrama-de-componentes/; acessado em 6 de novembro de 2023.</li>
  <li>https://www.lucidchart.com/pages/pt/diagrama-de-componentes-uml; acessado em 6 de novembro de 2023.</li>
  <li>https://www.youtube.com/watch?v=uivUGTgJlGA; acessado em 6 de novembro de 2023
  <li>https://www.lucidchart.com/blog/pt/como-fazer-diagramas-de-arquitetura-de-sistema/; acessado em 11 de novembro de 2023.</li>
  <lil>https://ldfgrupo.pt/blog/diagrama-de-arquitetura-de-software-uml/; acessado em 11 de novembro de 2023.</lil>
  <lil>https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django; acessado em 14 de novembro de 2023.</lil>
  <lil>https://www.sqlalchemy.org/library.html; acessado em 19 de novembro de 2023.</lil>
  <li>https://creately.com/blog/pt/diagrama/tutorial-do-diagrama-de-implantacao/; acessado em 18 de novembro de 2023.</li>
</ul>
