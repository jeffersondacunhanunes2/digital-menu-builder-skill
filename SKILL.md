---
name: digital-menu-builder
description: Criação e evolução de cardápios digitais responsivos para restaurantes, confeitarias, docerias e delivery — catálogo por categorias, identidade visual, fotos fornecidas, carrinho, finalização por WhatsApp e painel administrativo próprio com dados persistentes. Use quando o usuário pedir para criar, adaptar, completar ou administrar um cardápio/loja de pedidos online, especialmente quando trouxer um site de referência, perfil social, manual da marca, imagens de produtos ou necessidade de trocar preços sem editar código.
---

# Construtor de Cardápios Digitais

Criar uma experiência de pedido rápida e mobile-first, com conteúdo fiel ao cliente, operação administrativa independente e fluxo de compra coerente. Tratar cada cliente como projeto novo: nunca reaproveitar nomes, catálogo, fotos, telefones, contas ou credenciais de outro cliente.

## Fluxo de trabalho

1. **Classificar escopo e coletar fontes.** Se for criar um cardápio novo, antes do design/código enviar a [solicitação inicial de materiais](templates/solicitacao-inicial-de-criacao.md) e preencher a [ficha de briefing](templates/briefing-cliente.md); aproveitar anexos já recebidos e pedir só o que ainda faltar. Se for modificar um cardápio existente, pular essa coleta inicial e pedir somente dados necessários à alteração. Separar referência de navegação, identidade visual, fonte oficial de produtos e fotos. Manter lacunas explícitas; não preencher preços, taxas, horários, disponibilidade, promessas ou contatos por suposição.
2. **Definir a experiência.** Mapear cabeçalho/contato, categorias, busca, cards, imagens, carrinho, entrega/retirada, meios de pagamento e ação final. Usar o [playbook de implementação](references/implementacao-e-seguranca.md) para arquitetura, modelagem, painel e segurança. Perguntar apenas quando faltar uma decisão que altere materialmente produto, permissões, custos ou fluxo; para detalhes reversíveis, escolher um padrão seguro e documentá-lo.
3. **Aplicar marca e montar catálogo.** Usar manual, logotipo, tipografia e cores fornecidos. Associar cada foto ao produto identificado pelo cliente; manter placeholders honestos onde faltar imagem. Não converter conteúdo ilustrativo ou social em verdade comercial. Para transformar imagens existentes, seguir `image-processing`; para criar nova imagem, seguir `imagegen` e não substituir fotos reais sem autorização.
4. **Implementar pedido e painel, se solicitado.** Para site/app novo, seguir as skills Web Dev vigentes e usar `webdev-mcp`. Separar interface pública de API e dados privados. Um “painel próprio” permite ao cliente atualizar catálogo por `/admin` sem abrir Manus para cada alteração; não significa, por si só, hospedagem independente do provedor. Se ele pedir independência total de hospedagem, esclarecer a escolha de infraestrutura antes de migrar.
5. **Validar e entregar.** Validar os contratos entre catálogo, banco, carrinho, checkout e painel usando o [checklist de qualidade](references/validacao-e-entrega.md). Não declarar verificações que não foram executadas.

## Regras essenciais

- Usar cada fonte para o propósito certo: link de referência para experiência; redes sociais para sinais visuais e tom; menu, texto ou confirmação do cliente para produtos e condições; fotos anexadas para imagens associadas pelo cliente. Ver detalhes em `references/fontes-e-conteudo.md`.
- Não inventar catálogo. Perguntar se a lacuna bloqueia o resultado; caso contrário, marcar pendente/“a confirmar” e modelar ausência sem transformar preço desconhecido em zero, horário em aberto ou disponibilidade garantida.
- Tratar meios de pagamento como preferência no pedido, não como pagamento capturado. Não pedir cartão, simular cobrança ou afirmar pagamento confirmado sem integração autorizada.
- Gerar link `wa.me` com número internacional e texto URL-encoded, para o comprador revisar e enviar. Incluir somente preços e condições confirmados; distinguir taxa, prazo e disponibilidade conhecidos dos que aguardam confirmação.
- Fazer alterações do painel por API autenticada e dados persistentes, nunca por estado local, arquivo embutido ou senha hard-coded. Ocultar/reativar em vez de apagar produtos; aplicar segurança do servidor, não confiar no browser.
- Revalidar ambiente, projeto, diretório e autorização da sessão antes de reutilizar qualquer recurso. Manter contas, banco, arquivos, credenciais e catálogo segregados por cliente.
- Separar checkpoint, Preview e publicação permanente. Seguir as instruções Webdev/checkpoint atuais; nunca apresentar Preview como site publicado.

## Recursos desta skill

- Leia a [ficha de briefing](templates/briefing-cliente.md) ao iniciar um novo cliente.
- Use a [solicitação inicial de materiais](templates/solicitacao-inicial-de-criacao.md) somente ao criar um cardápio novo; fotos dos produtos podem chegar progressivamente.
- Leia [fontes e conteúdo](references/fontes-e-conteudo.md) quando houver links, redes, manuais, menu ou fotos.
- Leia [implementação e segurança](references/implementacao-e-seguranca.md) ao criar site, carrinho, WhatsApp, painel ou persistência.
- Leia [validação e entrega](references/validacao-e-entrega.md) antes de testar, criar checkpoint ou entregar.
- Use [catálogo vazio](templates/catalogo-vazio.json) como estrutura genérica inicial, sem tratar campos vazios como dados prontos para publicar.
