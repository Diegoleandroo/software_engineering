📉 Imagem 1 – Diagrama de Componentes: Arquitetura em Camadas

Mostra as camadas clássicas: Apresentação (Aplicação Desktop/Móvel), Aplicação (Controle, Negócios, Persistência) e Dados (DAO, Modelo), conectadas via interfaces API/HTTPS.

📈 Imagem 2 – Diagrama de Componentes: Arquitetura Orientada a Serviços com ESB

Mostra uma Camada Consumidora (apps em nuvem, interface web), uma Camada Provedora com um Enterprise Service Bus (ESB) fazendo o roteamento para microsserviços (Contas, Ordens de Compra, Envio), cada um com seu próprio banco de dados.

📊
Diagrama (ORM)
É uma variação do mesmo padrão do Imagem 2 anterior, mas simplificado e com um componente adicional (Broker de Mensagens).

Estrutura do diagrama:

Aplicações Clientes: Interface Gráfica Web e Interface Gráfica Móvel
MicroServiços: API Gateway roteando para 3 microsserviços (Compra, Venda, Envio), cada um com seu próprio banco de dados
Comunicação assíncrona: Broker de Mensagens integrando os microsserviços (padrão de mensageria/eventos)
