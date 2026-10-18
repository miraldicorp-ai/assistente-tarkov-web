# Tarkov · Itens, Hideout e Trocas

Aplicação em português para consultar itens e preços de Escape from Tarkov e organizar os materiais necessários para o Hideout.

## Funcionalidades

- Consulta de itens e preços nos modos PVE e PVP.
- Filtros por categoria, busca por nome e ordenação por preço ou valor por espaço.
- Marcações independentes por estação e nível do Hideout.
- Quantidade que já tenho, quantidade que falta e custo restante.
- Consulta de trocas e requisitos das construções.
- Salvamento automático de marcações e progresso no navegador.

## Como usar

Baixe o arquivo `index.html` e abra no navegador. A consulta dos dados precisa de internet; não é necessário instalar dependências nem configurar uma chave de API.

Os dados dos itens são consultados em [json.tarkov.dev](https://json.tarkov.dev/endpoints). Os preços representam a última coleta disponível e podem diferir dos valores no jogo.

## Salvamento

As marcações, quantidades, categorias selecionadas e estados do Hideout ficam no armazenamento local do navegador (`localStorage`). Cada pessoa tem seu próprio progresso, sem conta ou servidor de sincronização.

Use o mesmo arquivo ou endereço no mesmo perfil do navegador para continuar de onde parou. Limpar os dados do navegador pode apagar o progresso. O armazenamento de um arquivo local é separado do armazenamento de uma versão hospedada na internet; as marcações não são transferidas automaticamente entre eles.

## Estrutura

`index.html` contém a interface, os estilos e o comportamento da aplicação. Não há etapa de compilação.

## Créditos

Dados e imagens fornecidos pelo projeto [tarkov.dev](https://tarkov.dev/). Escape from Tarkov e seus materiais pertencem à Battlestate Games. Este é um projeto independente, sem vínculo oficial com o jogo.
