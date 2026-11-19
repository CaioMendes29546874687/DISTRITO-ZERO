# Arquitetura multiplayer — proposta

## Modelo
- Servidores regionais simulam sessões e áreas de jogo.
- Uma identidade global do jogador permite viajar entre regiões.
- Perfil, inventário, saldo e propriedades persistem em serviços centrais.
- Transferências entre servidores usam operação atômica: bloquear origem, validar destino, confirmar e registrar; impedir duplicação.

## Autoridade
O servidor valida movimento sensível, inventário, recompensas, compras, vendas, propriedade e transações. O cliente apresenta a interface e envia intenções; não decide o saldo final.

## Componentes lógicos
- Gateway/API autenticada.
- Serviço de identidade e sessão.
- Serviço de personagens e inventário.
- Serviço econômico e ledger imutável de transações.
- Serviço de propriedades e empresas.
- Orquestrador de viagens entre regiões.
- Servidores de jogo regionais.
- Logs, métricas, moderação e ferramentas administrativas.

## Requisitos antes de abrir ao público
- Proteção contra replay e duplicação de transações.
- Rate limiting e validação de entrada.
- Backups e plano de recuperação.
- Testes de carga e latência por região.
- Política de privacidade, termos de uso e moderação.
- Custos operacionais e capacidade definidos por testes.

## Não implementado ainda
Este documento descreve a arquitetura desejada. Nenhum servidor multiplayer, conta, banco de dados ou transferência entre regiões foi criado nesta etapa.
