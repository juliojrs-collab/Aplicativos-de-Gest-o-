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
(pela data prevista, que é o dia da entrega: atrasados, hoje, amanhã, próximos), registra fotos, observações e quem
recebeu, o cliente assina na tela (com hora e GPS) e o PDF assinado vai para o
WhatsApp do cliente pelo número oficial, via `whatsapp-crm`:
`GET /api/bling/campo/pedidos`, `GET /api/bling/campo/pedidos/:id`, `POST /api/bling/campo/enviar`.
Coleções no Firebase: `campo_pedidos`, `campo_midias`, `campo_tecnicos`.
