# Oficina Purific

Controle das OS de purificadores recebidos na loja: recepção no balcão, orçamento
e serviço na oficina, fotos/vídeos de cada etapa e medição do tempo de cada etapa.

- `index.html` — o app inteiro (hospedado no Netlify).
- Dados no Firebase do AquaPure (`aquapure-9100b`), em coleções próprias:
  `oficina_os`, `oficina_midias`, `oficina_tecnicos`.
- Número da OS gerado no Bling pelo servidor `whatsapp-crm` (Railway):
  `GET /api/bling/os/contatos` e `POST /api/bling/os`.
