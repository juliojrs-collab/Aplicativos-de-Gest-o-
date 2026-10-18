# Oficina Purific

Controle das OS de purificadores recebidos na loja: recepção no balcão, orçamento
e serviço na oficina, fotos/vídeos de cada etapa e medição do tempo de cada etapa.

- `index.html` — o app inteiro (hospedado no Netlify).
- Dados no Firebase do AquaPure (`aquapure-9100b`), em coleções próprias:
  `oficina_os`, `oficina_midias`, `oficina_tecnicos`.
- Número da OS gerado no Bling pelo servidor `whatsapp-crm` (Railway):
  `GET /api/bling/os/contatos` e `POST /api/bling/os`.

## Entregas de campo (`campo/`)

App para os técnicos que saem para a rua, publicado em `<site>/campo/`. Em vez
de imprimir o pedido de venda, o técnico abre no celular o pedido do Bling
(um filtro por data prevista, que é o dia da entrega, de 7 dias atrás em diante; abre em hoje ou na próxima data com entrega), registra fotos, observações e quem
recebeu, o cliente assina na tela (com hora e GPS) e o PDF assinado vai para o
WhatsApp do cliente pelo número oficial, via `whatsapp-crm`:
`GET /api/bling/campo/pedidos`, `GET /api/bling/campo/pedidos/:id`, `POST /api/bling/campo/enviar`.
Coleções no Firebase: `campo_pedidos`, `campo_midias`, `campo_tecnicos`.

Mapa dos técnicos em `<site>/campo/mapa/`: caminho do dia de cada técnico, com
as posições que o app grava em `campo_localizacoes` ao ser aberto, a cada
10 minutos com ele aberto na tela e em cada assinatura. Com o celular
bloqueado ou o app fechado, o navegador não entrega o GPS.
