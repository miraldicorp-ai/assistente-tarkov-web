# Tarkov · Itens, Hideout e Trocas

Aplicação em português para consultar itens e preços de Escape from Tarkov e organizar os materiais necessários para o Hideout.

## Funcionalidades

- Consulta de itens e preços nos modos PVE e PVP.
- Filtros por categoria, busca por nome e ordenação por preço ou valor por espaço.
- Marcações independentes por estação e nível do Hideout.
- Quantidade que já tenho, quantidade que falta e custo restante.
- Consulta de trocas e requisitos das construções.
- Missões por trader, com foto, nomes em português e inglês, nível mínimo do jogador e caixa de conclusão.
- Guias de apoio por objetivo, com imagens de referência da missão e dos itens, condições de execução e acesso à Wiki e aos mapas.
- Progresso de missões salvo separadamente para PVE e PVP, com filtros por nível e conclusão.
- Salvamento automático de marcações e progresso no navegador.
- Aba Raid com missões à esquerda e no centro e stash de quatro colunas à direita, com tamanho padrão dos itens e novas linhas automáticas.
- Prepare for Escape: ícones dos quatro finais, árvores das rotas, ramos de provas e porcentagem de conclusão ligada às marcações em Missões.

## Como usar

Baixe o arquivo `index.html` e abra no navegador. A consulta dos dados precisa de internet; não é necessário instalar dependências nem configurar uma chave de API.

Os dados dos itens são consultados em [json.tarkov.dev](https://json.tarkov.dev/endpoints). Os preços representam a última coleta disponível e podem diferir dos valores no jogo.

## Salvamento

As marcações, quantidades, categorias selecionadas e estados do Hideout ficam no armazenamento local do navegador (`localStorage`). Cada pessoa tem seu próprio progresso, sem conta ou servidor de sincronização.

Use o mesmo arquivo ou endereço no mesmo perfil do navegador para continuar de onde parou. Limpar os dados do navegador pode apagar o progresso. O armazenamento de um arquivo local é separado do armazenamento de uma versão hospedada na internet; as marcações não são transferidas automaticamente entre eles.

## Estrutura

`index.html` contém a interface, os estilos e o comportamento da aplicação. Não há etapa de compilação.

## Aprender com o código

O `index.html` inclui comentários em português nas principais partes de HTML, CSS e JavaScript. Comece pelo [guia do código](GUIA-DO-CODIGO.md), com um mapa das funções, explicações das ferramentas, exemplos de cálculos e exercícios para experimentar.

## Missões

Na aba **Missões**, selecione a foto de um trader. As tarefas são agrupadas pelo nível mínimo do jogador e mostram os nomes em português e inglês. Abra **Como fazer e fotos** para consultar instruções por objetivo, fotos da missão e dos itens envolvidos, quantidades, condições e pré-requisitos fornecidos pelo tarkov.dev. A busca aceita ambos os nomes. Marque **Concluída** para registrar o progresso; desmarque para desfazer.

O nível mínimo não garante que a missão esteja liberada: facção, missões anteriores e outros requisitos também podem ser necessários. O progresso é manual e fica salvo neste navegador, separadamente para PVE e PVP. As instruções de apoio explicam as ações descritas nos objetivos; não são rotas verificadas individualmente para cada missão. As imagens são referências da missão e dos itens. Para localização exata e fotos de pontos do cenário, use o link da Wiki incluído no guia.

## Raid

Marque **Na Raid** na aba Missões para acompanhar a tarefa na aba **Raid**. Expanda a missão para consultar o mesmo guia, objetivos e fotos. A seleção é independente da caixa **Concluída** e fica salva por modo PVE/PVP.

Todos os itens marcados aparecem no stash, somando as quantidades das diferentes origens. Cada clique em um item soma uma unidade em **Tenho**, assim como na aba Marcados. Durante a coleta, a borda fica amarela; ao completar, as necessidades são desmarcadas e uma ficha verde permanece na Raid. O próximo clique confirma e mantém a ficha; o seguinte a remove. O andamento e essas confirmações ficam salvos ao fechar o navegador.

## Prepare for Escape

Clique no ícone de Savior, Debtor, Survivor ou Fallen para abrir o roteiro correspondente. Informe a escolha da caixa em Falling Skies para adaptar as etapas condicionais. Use **Ver em Missões** e marque **Em andamento** (amarelo) ou **Concluída** (verde) no grupo **História · Prepare for Escape**, acima dos traders. As tarefas comuns dos traders também ganharam a opção Em andamento.

O percentual conta etapas e provas concluídas do roteiro selecionado, sem contar tarefas em andamento. As provas são alternativas: Savior conta oito e Debtor duas, sem exigir todos os nove ramos. Na rota Savior, a cadeia de conclusão de The Price of Independence vem da API e usa os mesmos IDs das tarefas dos traders. Aguarde o carregamento dessas tarefas para o denominador incluir essa cadeia. PVE e PVP têm progresso independente.

Os capítulos da história não são fornecidos pelo endpoint de tarefas dos traders. O catálogo das rotas foi organizado no próprio código a partir dos guias da [Wiki](https://escapefromtarkov.fandom.com/wiki/The_Ticket) e do [TarkovForge](https://tarkovforge.web.app/story-guide/endings/savior), revisados em 18/10/2026; nomes em português são traduções de apoio. A árvore resume etapas, sem substituir os objetivos internos dos capítulos. O percentual é uma organização manual, não uma confirmação de acesso no jogo. As escolhas do jogo podem ser irreversíveis e os requisitos podem mudar com atualizações. Ícones das conquistas: tarkov.dev / Battlestate Games.

## Créditos

Dados e imagens fornecidos pelo projeto [tarkov.dev](https://tarkov.dev/). Escape from Tarkov e seus materiais pertencem à Battlestate Games. Este é um projeto independente, sem vínculo oficial com o jogo.

