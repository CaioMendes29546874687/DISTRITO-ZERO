# Arquitetura do mundo geográfico

## Objetivo
Representar a Terra por dados geoespaciais e carregar apenas a região necessária ao jogador. A cobertura será global, mas o nível de detalhe e a interatividade serão implantados progressivamente.

## Camadas
1. **Globo e terreno:** referência geodésica, elevação e terreno.
2. **Cartografia:** países, limites administrativos, ruas, trilhas, rios e pontos de interesse.
3. **Edificações:** pegadas, altura aproximada e classificação quando os dados existirem.
4. **Camada de jogo:** colisões, fachadas interativas, interiores, portas, lojas e propriedades.
5. **Estado persistente:** proprietário, aluguel, mobília, garagem e estado de missão.

## Coordenadas
- Fonte geográfica usa latitude/longitude WGS84 (EPSG:4326) quando aplicável.
- Conversão para coordenadas locais do motor deve usar origem georreferenciada e precisão adequada.
- Não usar latitude/longitude diretamente como coordenadas de física do jogo.
- Cada região carregável deve ter identificador estável e limites explícitos.

## Streaming
- Dividir o mundo em células geográficas.
- Carregar terreno, ruas e edifícios próximos conforme distância e nível de detalhe.
- Descarregar recursos distantes sem apagar estado persistente.
- Usar cache com limites de tamanho, validade e política de atualização.
- Evitar baixar tiles em massa ou contornar limites dos provedores.

## Fontes possíveis
- OpenStreetMap para ruas, caminhos, edifícios e pontos de interesse, observando ODbL e atribuição.
- Cesium/terreno e provedores de imagens para visualização global, conforme licença, custo e termos comerciais.
- Dados públicos locais podem complementar alturas, endereços e limites, após verificação de licença e qualidade.

## Limites conhecidos
- Cobertura de edifícios varia muito por país e cidade.
- Uma pegada de edifício não fornece necessariamente fachada, altura correta ou interior.
- Imagens de satélite não concedem automaticamente direito de redistribuição ou uso como textura comercial.
- Interiores serão construídos com kits modulares e conteúdo autoral; imóveis especiais podem ter interiores exclusivos.

## Primeira região de validação
Mombuca, Capivari, Rio das Pedras e Piracicaba (São Paulo, Brasil). Validar cobertura de ruas, edifícios, coordenadas, desempenho em celular e atribuição dos dados antes de ampliar.
