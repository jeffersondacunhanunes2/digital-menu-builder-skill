# Validação e entrega

## Verificações focadas

Usar build, diagnósticos, testes existentes e verificações HTTP/código. Evitar navegador/screenshots sem pedido explícito do usuário ou defeito visual/interativo observado que precise deles.

- [ ] Conteúdo: cada produto, descrição, preço, unidade e imagem corresponde à fonte aprovada; pendências não foram convertidas em fatos.
- [ ] Cabeçalho: nenhum status operacional ausente é apresentado como fato ou como placeholder público; campos existentes no painel/banco permanecem preservados. Se houver WhatsApp confirmado, o card é clicável, exibe o número correto, monta `wa.me` somente com dígitos validados e continua acessível por teclado; a grade se adapta a itens removidos.
- [ ] Contratos: resposta real do catálogo valida tipos, valores nulos e moeda em centavos usados pela interface.
- [ ] Cliente público: categorias, busca, ocultação, indisponibilidade e preço a confirmar comportam-se conforme as regras.
- [ ] Carrinho: quantidades, remoções, subtotal, pedido mínimo, taxa fixa/variável e total calculado têm resultado correto; dados desconhecidos não resultam em falsa confirmação.
- [ ] Mensagem WhatsApp: teste entrega/retirada, pagamento disponível, dinheiro/troco condicional, acentos, endereços, linhas, taxa, total e dados de contato. Confirmar que a ação só prepara o rascunho e que o atendente ainda confirma o pedido.
- [ ] Checkout responsivo (quando solicitado ou houver falha interativa reportada): reproduzir adicionar item → abrir carrinho → finalizar em pelo menos um viewport mobile e um desktop; cobrir entrega/retirada e os ramos de pagamento relevantes. Confirmar que o CTA está visível, alcançável por rolagem e recebe o clique (hit-test no centro não deve apontar para barra, backdrop ou outro overlay); verificar a rolagem interna do painel. Interceptar `wa.me` antes de carregar o destino externo e validar número internacional e texto URL-encoded com dados fictícios; bloquear/stubbar pixels de analytics quando possível. Nunca enviar uma mensagem ou pedido real no teste.
- [ ] Sessão: rota administrativa sem login retorna 401/403; login válido cria sessão; senha incorreta falha sem revelar qual parte estava errada; logout/expiração revogam acesso. Não registrar nem imprimir credenciais.
- [ ] Painel/API: salvar configuração e produto persiste após reload; produto oculto desaparece do público, mantém-se no painel e pode ser reativado; erro API é exposto com mensagem compreensível.
- [ ] Imagens: upload autenticado dentro do limite é decodificado, otimizado, salvo no storage durável e associado ao produto; formato/MIME forjado, arquivo corrompido e arquivo grande são rejeitados; outros cards não mudam.
- [ ] Infra: build, migrações idempotentes e concorrentes, health check, `manus-routes.json`, rotas/API/assets/fallback e os caminhos diretos `/` e `/admin` respondem. Confirmar portabilidade do container e ausência de segredos no cliente.
- [ ] Após qualquer correção, repetir a verificação afetada. Se o projeto entrou em Plan Mode Webdev, seguir sua exigência de revisão independente somente leitura antes de entregar.

## Checkpoint e publicação

- Antes de avanço para `main`, consultar instruções atuais Webdev/checkpoint, verificar publicação automática, atualizar/integrar o `origin/main` remoto, rodar novamente os checks afetados e preservar alterações concorrentes. Um commit local isolado não é checkpoint.
- Tratar checkpoint, Preview e publicação como estados distintos. Não criar ou reportar URL de produção sem confirmação da plataforma de que a publicação está ativa. Não iniciar publicação pública sem pedido/autorização aplicável.
- Se a publicação falhar, comunicar o erro observado e corrigir apenas a causa confirmada. Não repetir uma submissão desconhecida nem executar ação destrutiva para “destravar” o ambiente.

## Entrega ao cliente

Informar em linguagem simples:
1. Link do cardápio e marcar **Preview** ou **Publicado** corretamente.
2. Link `/admin` e como entrar sem expor e-mail/senha em local inseguro; indicar onde o próprio responsável ajusta preço, disponibilidade, fotos, WhatsApp, horários e condições.
3. Fluxo do pedido: comprador preenche o necessário, confere resumo e envia manualmente a mensagem no WhatsApp; atendente confirma disponibilidade, taxa, prazo e pagamento.
4. Campos ainda a confirmar, aspectos não executados e versão/checkpoint, quando existente.

Nunca dizer que um pedido foi enviado/recebido pelo estabelecimento só porque o link do WhatsApp foi aberto; nunca afirmar que o site está publicado por conta de Preview, build ou checkpoint.
