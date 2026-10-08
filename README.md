# Docker Compose — Turma B

Evidências da atividade de 08/10/2026.

## Arquivos

- `compose.yaml`: versão final corrigida.
- `evidencias/00-docker-disponivel.jpg`: versões do Docker e Compose no Windows.
- `evidencias/01-primeira-execucao-https.jpg`: captura complementar do teste do navegador em HTTPS; o portal atende por HTTP.
- `evidencias/02-criterio-1-api-e-livros.jpg`: página corrigida, API `ok` e os três livros.
- `evidencias/03-criterio-2-reserva.jpg`: reserva registrada e quantidade restante reduzida.
- `evidencias/04-criterio-3-persistencia.jpg`: reserva ainda presente após reiniciar os containers.
- `evidencias/05-down-up-ps.jpg`: comandos `down`, `up -d` e estado dos serviços.
- `evidencias/primeira-execucao.txt`: trechos de comandos, saídas e logs da primeira execução, transcritos do terminal.

A captura original do PowerShell da primeira execução ainda deve ser adicionada se o formulário exigir essa imagem. A captura de HTTPS é apenas complementar; o endereço funcional é `http://localhost:8081`.

## Correções no Compose

- Portal encaminha para `http://api:3001` pela rede interna do Compose.
- Reservas persistem no bind mount `./registros:/app/registros`.
- A porta da API não é publicada no host; somente o portal publica `127.0.0.1:8081`.
