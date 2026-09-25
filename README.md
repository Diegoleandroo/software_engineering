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

Arquitetura Limpa

é um diagrama estrutural (estático) do UML que agrupa elementos relacionados (classes, interfaces) em pacotes (namespaces lógicos), e mostra as relações de dependência entre esses pacotes e entre os elementos internos a eles. Ele documenta como o código está organizado e quais partes podem depender de quais — não mostra comportamento, tempo ou execução (isso seria diagrama de sequência, de atividades, etc.).

Os elementos formais que ele contém
Elemento visual	Nome técnico UML
Retângulo com aba (pasta)	Pacote (Package)
Retângulo com 3 compartimentos	Classe (Class) — nome, atributos, métodos
Retângulo com «interface»	Interface
Retângulo com «artifact»	Artefato (Artifact) — representa algo físico/implantável, como uma biblioteca externa
Seta tracejada aberta, rotulada «depende de»	Dependência (Dependency)
Seta tracejada com triângulo vazado, rotulada «realize»	Realização de Interface (InterfaceRealization) — quando uma classe implementa uma interface
Retângulo com dobra no canto	Nota (Note/comentário)


💹 Mercado de Trabalho 

O que é mais usado no mercado, na ordem real de frequência

1º lugar — Estrutura de pastas (nem é bem um "diagrama")
Na esmagadora maioria das empresas — startups, scale-ups, times ágeis — a "documentação" da arquitetura é simplesmente a organização de pastas do projeto (entities/, usecases/, adapters/, infra/), às vezes com um README explicando as regras. Nenhum diagrama formal é desenhado no dia a dia.

2º lugar — C4 Model (nível Component ou Container)
Esse é, honestamente, o que mais se aproxima de um "padrão de mercado" hoje em dia para documentar arquitetura de forma visual, principalmente em empresas de médio/grande porte. Não é UML formal — é uma notação mais simples e pragmática, criada justamente como reação à complexidade excessiva do UML. Ferramentas como Structurizr, ou até draw.io com o template C4, são comuns.

3º lugar — Diagramas informais tipo "caixa e seta"
Feitos no Miro, Excalidraw, FigJam ou draw.io sem seguir nenhuma notação rígida — só caixas coloridas, setas, e texto explicativo. Muito comum em times ágeis para reuniões de design/RFC.

4º lugar — Diagrama de sequência (não necessariamente UML estrito)
Usado quando o time quer mostrar um fluxo específico passo a passo (tipo o nosso "fluxo de controle" anterior), mas geralmente sem rigor total de notação UML.

Por último — UML formal com pacotes, compartimentos de classe, estereótipos
Isso que fizemos nos últimos diagramas — package diagram com «interface», «artifact», compartimentos de atributo/método — é raro no mercado ágil/startup atual. Ele aparece mais em:

Empresas grandes e tradicionais (bancos, governo, sistemas legados)
Contextos acadêmicos (faculdade, TCC, certificações)
Setores regulados que exigem documentação formal (aeroespacial, saúde, defesa)
Times que usam ferramentas como Enterprise Architect ou Astah por exigência contratual/processo (ex: CMMI, ISO)


