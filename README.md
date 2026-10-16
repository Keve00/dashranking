# Ranking comercial

Protótipo navegável interno para gamificação de vendas de internet e serviços. Visual escuro e laranja, configurável; ranking com pódio e modo TV, campanhas guiadas, cadastro de vendedores, importação CSV/XLSX com revisão, correção e atualização por ID.

## Execução

Sirva `dist/` com um servidor estático. Exemplo: `python -m http.server 8080 --directory dist`. Abra o endereço local correspondente. Não abra o HTML diretamente por file://, pois utiliza módulos JavaScript.

## Dados

Persistência no localStorage do navegador. Não há banco compartilhado, autenticação de papéis, integração CRM ou encerramento oficial com homologação. O acesso ao site hospedado é privado; não constitui um sistema de permissões entre gestores e vendedores. Dados iniciais e fotos são demonstrativos.

Planilha: primeira aba do XLSX, ou CSV UTF-8 com vírgula/ponto e vírgula. Colunas: id_venda, vendedor (ID ou nome), data_ativacao, produto, status, valor. Status suportados: ativada, pendente, cancelada, aprovada, fechada. Data é a data do evento que pontua. Vendas pendentes não pontuam. IDs repetidos no mesmo arquivo bloqueiam aplicação; IDs já existentes atualizam registros. Se o navegador não suporta descompressão XLSX deflate-raw, a interface orienta salvar como CSV. Limite de 5 MB / 10.000 linhas.

Pontuação recalculada pelos participantes, status, período e pontos da campanha. Empates aparecem em ordem alfabética; regra de premiação deve ser definida antes do uso real. Metas coletivas usam pontos. Prêmios são informativos; entrega fora do produto.

## Próxima etapa

Banco compartilhado, acesso por perfil, importação validada no servidor, homologação e encerramento de campanhas. Manter o acesso privado e a identidade aprovada.
