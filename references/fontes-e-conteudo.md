# Fontes, marca e conteúdo do cardápio

## Separar fontes pela finalidade

| Fonte fornecida | Usar para | Não inferir dela |
|---|---|---|
| Site ou link de referência | Navegação, hierarquia, experiência de busca/categoria/carrinho e etapas do pedido. Inspecionar até onde for público, sem concluir/enviar pedidos. | Marca, imagens, sabores, preços, telefone ou condições do outro negócio. Não copiar texto ou identidade. |
| Instagram/Facebook ou outro perfil social do cliente | Referências visuais: paleta, logotipo, tipografia aparente, composição, estilo fotográfico e tom. | Catálogo definitivo, preço vigente, estoque/disponibilidade, taxas, horário ou instruções de pedido, salvo confirmação explícita do cliente de que aquela publicação é a fonte oficial vigente. |
| Manual de marca/logo/arquivos de identidade | Aplicação visual autorizada: logotipo, cores, tipografia, margens e linguagem. | Informação comercial que não conste nesses documentos. |
| Cardápio anexado (PDF, foto, planilha) ou texto confirmado pelo cliente | Nomes, descrição, opções, preços, unidades, adicionais, variantes e condições claramente legíveis. | Texto ilegível, valor ambíguo, associação incerta de foto ou informação cortada. Marcar pendência e perguntar. |
| Foto de produto anexada | Imagem do item que o cliente associar a ela. Preservar sua identidade e conteúdo; otimizar formato/tamanho sem inventar decoração ou ingredientes. | Sabor, ingredientes, tamanho ou produto retratado quando a associação não estiver clara. |
| Resposta direta do cliente | Resolver lacunas e confirmar regras vigentes, número oficial, entrega/retirada e fluxo de finalização. | Não estender a confirmação a outras informações que não foram respondidas. |

Manter um mapa curto de evidências durante a execução: `campo → arquivo/link/trecho ou confirmação do cliente → estado (confirmado/pendente)`. Não usar busca pública ou conteúdo de terceiros para preencher campos comerciais faltantes.

## Coleta no início de uma criação nova

- Aplicar somente ao pedido de criar um cardápio novo. Antes do design/código, usar a [mensagem inicial](../templates/solicitacao-inicial-de-criacao.md); considerar tudo que já foi enviado e não solicitar de novo materiais presentes. Em manutenção de site/catálogo existente, reutilizar fontes e decisões aprovadas e perguntar apenas o necessário à mudança.
- Separar fotos de referência visual de fotos reais dos produtos. Solicitar o manual, o perfil Instagram para branding, imagens de referência e o cardápio oficial. Usar Instagram apenas para identidade visual, nunca para completar sabores/preços sem confirmação explícita de que é a fonte comercial vigente.
- Receber fotos reais dos produtos por etapas ou em lotes, depois ou durante a organização do catálogo. Para cada arquivo, manter a associação confirmada `foto → sabor`; atualizar apenas o produto identificado, deixar placeholders nos sabores sem foto e não atrasar o restante do trabalho esperando todas as imagens.

## Extração e conferência do catálogo

1. Ler o menu integralmente; revisar páginas/cortes/zoom quando a imagem ou texto estiver pouco legível.
2. Transcrever cada categoria, produto, variante, unidade, adicional e preço exatamente. Preservar acentos, nomes de marca e níveis/tamanhos.
3. Representar dinheiro como **inteiro em centavos** no armazenamento/API e formatar em BRL apenas na interface. Confirmar o que o preço inclui quando isso afeta pedido.
4. Manter imagens num mapeamento explícito `arquivo recebido → produto confirmado`. Nunca associar apenas por ordem de upload. Se houver dúvida, deixar placeholder ou perguntar. Preservar a arte original; para cards com texto incorporado, usar enquadramento que mostre a imagem inteira (`contain`), sem recorte que esconda conteúdo.
5. Se o sabor escrito na foto não existir no catálogo, não substituir automaticamente um produto parecido. Perguntar se é um novo sabor, uma troca de foto, ou uma renomeação. Ao incluir um sabor novo, usar o preço confirmado pelo cliente/menu; aceitar preço de faixa existente somente se a fonte define explicitamente que a faixa se aplica a esse tipo de produto. Caso contrário, perguntar antes de deixá-lo ativo para pedido.
6. Criar uma lista de lacunas: preço ausente, taxa por região, mínimo, horário, disponibilidade, tempo, entrega/retirada, meios de pagamento, troco e contato. Perguntar apenas decisões materiais e independentes; detalhes reversíveis podem ser adotados como padrões visíveis e documentados.
7. Fazer revisão produto por produto com o cliente ou contra a fonte oficial. Não publicar conteúdo inventado para preencher espaços.

## Uso de referência sem cópia

Inspecionar o link de referência para descrever padrões de experiência (ex.: categorias, card, carrinho, formulário condicional, resumo do pedido). Reimplementar a ideia com o sistema visual do cliente; não reutilizar marca, texto, fotografia ou catálogo proprietário. Se o site de referência estiver protegido por login ou indisponível, usar somente o que realmente foi observado e declarar a limitação.
