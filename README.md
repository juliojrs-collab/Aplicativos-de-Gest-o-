# Oficina Purific

Controle das OS de purificadores recebidos na loja: recepção no balcão, orçamento
e serviço na oficina, fotos/vídeos de cada etapa e medição do tempo de cada etapa.

- `index.html` — o app inteiro (hospedado no Netlify).
- Dados no Firebase do AquaPure (`aquapure-9100b`), em coleções próprias:
  `oficina_os`, `oficina_midias`, `oficina_tecnicos`.
- Número da OS gerado no Bling pelo servidor `whatsapp-crm` (Railway):
  `GET /api/bling/os/contatos` e `POST /api/bling/os`.

## OS de Campo (`campo/`)

App para os técnicos de rua, publicado em `<site>/campo/`. O técnico abre no
celular a OS lançada no Bling (lista das OS abertas, filtro "Minhas" pelo campo
Técnico), registra fotos, observações e quem recebeu, o cliente assina na tela
(com hora e GPS) e o PDF assinado vai para o WhatsApp do cliente pelo número
oficial, via `whatsapp-crm`:
`GET /api/bling/campo/os`, `GET /api/bling/campo/os/:id`, `POST /api/bling/campo/enviar`.
Coleções no Firebase: `campo_os`, `campo_midias`, `campo_tecnicos`.
