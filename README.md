# Licita

> Concursos públicos em Angola, do caos ao processo.

Angola gasta centenas de milhões de dólares por ano em aquisições públicas. Uma fracção significativa desse dinheiro perde-se em processos lentos, opacos e fáceis de manipular — não por má fé, mas por falta de infraestrutura. O Licita resolve isso.

---

## O problema

Quando um ministério, câmara municipal ou hospital público precisa de adquirir um bem ou serviço, é obrigado por lei a lançar um concurso público. Na prática, hoje em Angola, isso significa:

- Anúncios publicados em papel no **Diário da República** ou em portais inacessíveis
- Empresas a vigiar manualmente canais dispersos para não perder prazos
- Submissão de propostas por email ou presencialmente, sem confirmação de entrega
- Triagem manual de documentos por parte da entidade contratante
- Avaliação sem rastreabilidade — quem viu o quê, quando e porquê
- Notificação individual dos participantes por telefone ou email

O resultado: processos que demoram meses, são fáceis de manipular, e não deixam rasto claro de nada.

---

## A solução

O **Licita** é uma plataforma de gestão de concursos públicos construída para o contexto angolano.

Uma entidade pública cria o concurso, define os requisitos, os documentos obrigatórios, o prazo e os critérios de avaliação. A partir daí, o sistema assume.

```
Entidade cria concurso  →  Empresas submetem propostas  →  Sistema valida e classifica  →  Resultado publicado
```

Cada etapa é automática, auditável e irreversível.

---

## Funcionalidades principais

### Para entidades públicas
- Criação de concursos com critérios de avaliação configuráveis
- Verificação automática de documentos obrigatórios na submissão
- Abertura simultânea de propostas no momento exacto do fecho do prazo
- Ranking calculado automaticamente com base nos critérios definidos
- Notificação automática de todos os participantes

### Para empresas concorrentes
- Agregação de concursos activos num único lugar
- Submissão digital de propostas com confirmação de entrega
- Validação imediata de completude documental
- Acompanhamento do estado do processo em tempo real
- Notificação automática de resultados

### Para auditores e cidadãos
- Histórico imutável de cada acção — quem fez o quê, quando e em que contexto
- Controlo de visibilidade por papel: júri vê o que lhe compete; auditor vê tudo mas não altera nada; empresa vê apenas o seu processo
- Integração com dados do Diário da República para cruzamento de informação

---

## Arquitectura técnica

| Camada | Tecnologia |
|---|---|
| Frontend | Next.js (App Router) |
| Orquestração de processos | Camunda 8 / Zeebe |
| Backend / Workers | Spring Boot (Java) |
| Base de dados | PostgreSQL |
| Mensageria | RabbitMQ |
| Tempo real | WebSocket |
| Infra | Docker Compose / CI-ready |

O núcleo do sistema é um motor de processos BPMN (Camunda 8) que garante que cada concurso segue exactamente o fluxo definido por lei — sem atalhos, sem excepções não registadas, com rollback automático em caso de falha.

---

## Por que Angola, por que agora

- A Lei 9/16 (Lei das Contratações Públicas) exige transparência e registo — o Licita implementa exactamente isso
- Angola tem mais de **400 entidades públicas** que lançam concursos regularmente
- A digitalização do Estado angolano é uma prioridade declarada do Executivo
- Não existe hoje nenhuma plataforma equivalente funcional no mercado

---

## Modelo de negócio

| Segmento | Modelo |
|---|---|
| Entidades públicas | Licença anual por entidade (SaaS B2G) |
| Empresas concorrentes | Freemium — submissão gratuita, analytics e alertas em plano pago |
| Integração institucional | Contrato de implementação + suporte para grandes organismos |

---

## Equipa

Desenvolvido por **Abner Lourenço** — Luanda, Angola.

## Contacto

📧 `louren.abner@gmail.com`  
