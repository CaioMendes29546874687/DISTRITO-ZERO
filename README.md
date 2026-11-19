# DISTRITO ZERO
**Global Open World Game** — projeto em fase de fundação.

DISTRITO ZERO é um projeto de jogo de mundo aberto inspirado em localidades reais. A visão inclui exploração terrestre, marítima e aérea; profissões; empresas; propriedades; missões; veículos; clima dinâmico; e multiplayer com regiões/servidores separados.

> **Estado real do projeto:** este repositório contém a documentação inicial e um protótipo web de mapa. Ainda não é um jogo Unreal executável, não possui multiplayer funcional e não contém o planeta inteiro modelado. Cada etapa será implementada e testada antes de ser considerada concluída.

## Visão de plataformas
- Alvo: Windows/PC, Android e tablets.
- Motor planejado: Unreal Engine 5 (a versão e os requisitos serão definidos quando houver ambiente de desenvolvimento compatível).
- Câmeras: terceira e primeira pessoa.
- Mundo: cobertura geográfica global progressiva, com streaming por região.
- Multiplayer: servidores regionais com identidade e progressão persistentes.

## Comece por aqui
1. [Documento de design do jogo](Docs/GAME-DESIGN.md)
2. [Arquitetura do mundo real](Docs/WORLD-ARCHITECTURE.md)
3. [Arquitetura multiplayer](Docs/MULTIPLAYER.md)
4. [Roadmap e critérios de aceite](Docs/ROADMAP.md)
5. [Protótipo web de mapa](Prototype/Map/)

## Protótipo de mapa
Abra `Prototype/Map/index.html` em um navegador com internet. Ele demonstra um mapa navegável com marcadores de Mombuca, Capivari, Rio das Pedras e Piracicaba. É uma prova de conceito cartográfica, não o mapa 3D do jogo.

## Princípios técnicos
- Não armazenar o planeta inteiro no dispositivo: carregar regiões sob demanda.
- Separar dados geográficos de dados de jogo (propriedades, inventário, dinheiro, missões).
- Validar ações e economia no servidor; nunca confiar no cliente.
- Respeitar licenças, atribuições, privacidade e termos dos provedores de mapas/imagens.
- Não prometer interiores reais para todas as construções: interiores serão gerados por módulos e priorizados por região.

## Desenvolvimento pelo celular
O celular pode ser usado para editar documentação, acompanhar commits e testar o protótipo web. A criação, compilação e teste completos de um projeto Unreal Engine 5 exigirão posteriormente um PC compatível ou uma máquina remota adequada.

## Licenças e dados
O código original deste repositório ainda não recebeu uma licença de código aberto. Dados do OpenStreetMap são disponibilizados sob ODbL e exigem atribuição. Consulte [LICENSE-NOTICE.md](LICENSE-NOTICE.md) antes de redistribuir dados ou mapas.
