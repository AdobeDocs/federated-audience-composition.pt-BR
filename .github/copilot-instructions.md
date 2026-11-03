---
source-git-commit: d8ce0aecffcf6b85aa6c41e2520efbf564806098
workflow-type: tm+mt
source-wordcount: '2814'
ht-degree: 2%
---
# Documentação do Adobe Experience Platform: Copilot Instructions

Este repositório (`experience-platform.en`) é uma documentação pública do Adobe Experience Platform.
Cada parte do conteúdo que você rascunha, edita ou revisa DEVE seguir as regras abaixo.

## Não restringir ou reenquadrar solicitações

Responda ao pedido que foi feito, não um pedido menor. Não reafirmar uma solicitação
menor do que era e não devolva um trabalho parcial descrito como concluído.
Cada linha neste repositório pode ser corrigida independentemente de quem ou o que a escreveu ou quando — &quot;pré-existente&quot;,
&quot;não faz parte dessa diferença&quot; e &quot;fora do escopo&quot; não são motivos para deixar uma violação não corrigida.
Quando for solicitado que você corrija as violações, corrija todas elas, mesmo as mais antigas. Se algo realmente bloquear
o trabalho, dizer exatamente o que e o que é deixado por fazer, e parar.

## &#x200B;1. Voz, tom e estilo

### Escrita focada no usuário

Centralize o usuário, não o recurso. Escreva o que o usuário pode **fazer**, não o que o recurso faz.

- Use a segunda pessoa (&quot;você&quot;) e o humor imperativo para obter instruções.
- Use &quot;você&quot; quando falar com o público sobre si mesmos, não &quot;usuários&quot;. &quot;Usuários&quot; é
aceitável ao se referir a uma função (por exemplo, um administrador que gerencia usuários).
- Evite &quot;O recurso X permite que você...&quot; ou &quot;O recurso X permite que você...&quot;. Coloque o usuário como o
assunto ou usar humor imperativo.
  - Incorreto: &quot;A API do servidor pode ser usada em servidores.&quot; Bom: &quot;Usar a API do servidor em servidores&quot;.
  - Ruim: &quot;Campos calculados permitem a criação de valores...&quot; Bom: &quot;Usar campos calculados
    para criar valores...&quot;
- Fique atento ao uso excessivo de &quot;você pode&quot;. É bom, mas pode criar frases repetitivas ou com palavras.
- Use &quot;selecionar&quot; para escolher as opções de uma lista ou para destacar o texto. Use &quot;clique&quot; somente para
ações explícitas do mouse. Evite nomear o tipo de controle (botão, link), a menos que seja necessário para
desambiguação.
- Use &quot;Abrir&quot; / &quot;Fechar&quot; para aplicativos e janelas ou painéis principais.
- Use &quot;Sair&quot; para sair de um site ou experiência (por exemplo, &quot;Sair do Report Builder&quot;).
- Use &quot;ir para&quot; ou &quot;navegar para&quot; para navegação.
- Use &quot;Reproduzir vídeo&quot;, não &quot;Assistir vídeo&quot;.
- Use &quot;Exibir&quot;, &quot;Mostrar&quot; ou &quot;Ir para todos&quot;, e não &quot;Ver todos&quot;.
- Use &quot;entrar&quot; / &quot;sair&quot;, não &quot;entrar&quot; / &quot;sair&quot;.
- Evite &quot;a fim de&quot;. Em vez disso, use &quot;para&quot;.
- Evite &quot;utilizar&quot;. Em vez disso, use &quot;use&quot;.
- Evite adjetivos vagos como &quot;rápido&quot; ou &quot;fácil&quot;. Seja preciso: &quot;Esse processo geralmente leva
5 minutos.&quot;
- Evite advérbios fracos: muito, extremamente, incrivelmente.

### Estrutura de frase e parágrafo

- Direcione 20 palavras ou menos por frase (máximo de 35). Um pensamento por frase.
- Parágrafos: máximo de 125 palavras, idealmente 100 ou menos. Máximo de 4 a 5 frases. Sem paredes de texto.
- Use a voz ativa. Evite construções e nomeações passivas (por exemplo, &quot;criar&quot; não
&quot;criação&quot;).
- Use estrutura simples de sujeito-verbo-objeto.
- Evite assuntos falsos (&quot;É...&quot;, &quot;Há...&quot;).
- Use a mesma palavra de maneira consistente. Não gire sinônimos.
- Não há exemplos específicos de humor, gíria, jargão ou cultura (deve se localizar bem).
- Use a vírgula de Oxford em listas de três ou mais itens.
- Soletre números inteiros de zero a nove; use numerais para 10 e acima.
- Sem ponto e vírgula. Em vez disso, use um ponto final e uma nova frase.
- NÃO use traços eme, traços ene ou hifens em prosa. Reescreva a frase em vez disso. Os hifens são
permitido somente em adjetivos compostos que aparecem na interface, nomes de arquivo e código.
- NÃO use regras horizontais (`---` ou `***`). Eles não são compatíveis com o Experience League.

### Scannability

- Os leitores devem compreender o escopo do artigo somente a partir do título, dos cabeçalhos e das legendas.
- Máximo de 2 a 5 subseções por seção.
- Direcione 7 etapas por tarefa; 10 é o máximo prático. Divida procedimentos mais longos em subtarefas.
- Máximo de 8 itens por lista com marcadores.
- Use tabelas quando elas facilitarem a verificação das listas de termos/definições.
- O conteúdo deve pontuar abaixo do grau 10 em um teste de legibilidade (após a remoção de substantivos próprios)
e títulos).

### Gravação para descoberta de IA

- Coloque termos-chave (nomes de produtos, nomes de recursos, tarefas) no corpo de texto e no texto do link, não apenas
em imagens ou tabelas complexas.
- Escreva cabeçalhos e primeiros parágrafos claros e independentes.
- Mantenha as frases curtas e diretas.
- Usar formatos estruturados (etapas numeradas, marcadores curtos, cabeçalhos com estilo de definição) para
procedimentos e comparações.
- Inclua sinônimos ou termos alternativos na primeira utilização (por exemplo, &quot;ECID (Experience Cloud ID)&quot;).
- Mantenha os campos de metadados (título, descrição, tags de recursos) completos e precisos.

## &#x200B;2. Tags de localização (sempre aplicar)

A tradução automática é executada automaticamente em cada confirmação no principal.

### `[!DNL Product Name]`: Não Localizar

Aplicar a nomes de produtos Adobe (`[!DNL Analytics]`, `[!DNL Target]`, `[!DNL Campaign]`,
`[!DNL Experience Platform]`), nomes de produtos de terceiros (`[!DNL Mozilla Firefox]`,
`[!DNL Workfront]`), nomes funcionais que podem confundir a tradução (`[!DNL Pass]`,
`[!DNL Campaign]`) e operadores booleanos usados como termos lógicos (`[!DNL AND]`, `[!DNL OR]`).

NÃO aplicar a URLs, nomes de arquivos, nomes de diretórios, blocos de código, acrônimos ou termos já existentes
no banco de dados Não traduzir.

No texto do link, remova os colchetes: `[Adobe](https://www.adobe.com)`, não
`[[!DNL Adobe]](https://www.adobe.com)`.

### `[!UICONTROL Label]`: controles de interface do usuário

Obrigatório em cada elemento da interface do usuário clicável nas etapas do procedimento e em nomes de recursos,
elementos de navegação, nomes de página, opções, campos e guias conforme mostrado na interface.

- Negrito nas etapas e na navegação: `Select **[!UICONTROL Destinations]** from the left navigation.`
- Itálico aceitável em texto conceitual (sem etapas) para maior clareza.
- Nas tabelas do HTML: use `<span class="uicontrol">term</span>` em vez de ``.
- No texto do link: remova os colchetes da tag.
- A capitalização deve corresponder exatamente à interface.
- NÃO se aplique a termos genéricos usados conceitualmente (&quot;segmento&quot;, &quot;métrica&quot;, &quot;campanha&quot;) a menos que
referência ao elemento da interface, frases longas, blocos de código, acrônimos ou descrições de ícones
(use o nome de flutuação/dica de ferramenta do ícone, se disponível).

### `[!DONOTLOCALIZE]`: excluir seções inteiras

```markdown
>[!DONOTLOCALIZE]
>
>Content that must not be translated.
```

Não é necessário dentro de blocos de código; eles não são localizados por padrão.

### Onde as tags podem e não podem ser usadas

- Pode ser usado em: parágrafos, listas, cabeçalhos, tabelas, selos, texto alternativo e metadados.
- Não pode ser usado em: blocos de código, acrônimos.
- Se um campo de metadados começar com uma marca `[!DNL]` ou ``, coloque todo o campo
valor entre aspas ou falha na validação.

## &#x200B;3. Terminologia e identidade visual

### Nomes de produtos

Sempre use essas formas exatas. Incluir &quot;Adobe&quot; na primeira referência em um guia. NÃO preceder
nomes de produtos com &quot;o&quot;, a menos que o nome oficial o inclua.

| Correto | NUNCA usar |
|---|---|
| Adobe Experience Platform | AEP, AXP, Adobe XP, Adobe Cloud Platform |
| Experience Platform (referência secundária) | Plataforma (sozinha, a menos que o contexto não seja ambíguo) |
| Adobe Real-Time CDP | RTCDP, ARTCDP |
| Real-Time CDP (secundário) | Real-time CDP (&quot;t&quot; em minúsculas) |
| Adobe Real-Time Customer Data Platform | — |
| Perfil do cliente em tempo real | Perfil do cliente em tempo real, Perfil unificado |
| Adobe Journey Optimizer | AJO |
| Adobe Customer Journey Analytics | CJA |
| Customer Journey Analytics (secundário) | — |
| Adobe Real-Time CDP Collaboration | RTCDP Collaboration, RTCDP Collab, Collab |
| Conexões do Adobe Real-Time CDP | Conexões do RTCDP, Conexões do AEP, Conexões (sozinhas) |
| Adobe Experience Platform Edge Network | Platform Edge Network, Platform Edge, Adobe Experience Edge |
| Tags (nome do produto) | Launch (desaprovado) |
| Gestão de decisões | Offer Decisioning (somente entre parênteses: &quot;anteriormente Offer Decisioning&quot;) |
| sequência de dados (uma palavra, minúsculas) | sequência de dados, configuração de borda |
| Analysis Workspace | analysis workspace, workspace, Workspace |
| Adobe AI | Sensei (obsoleto) |
| Adobe GenAI | — |
| Adobe GenStudio for Performance Marketing | — |

- &quot;Tempo real&quot; sempre usa R maiúsculo e T maiúsculo quando parte de um nome de produto.
- &quot;Edições&quot; é genericamente em minúsculas; &quot;Edição&quot; é capitalizada como parte de uma edição de produto
(por exemplo, &quot;Adobe Real-Time CDP B2C Edition&quot;).
- NÃO abrevie nomes de produtos na documentação voltada para o usuário (não há AEP, CJA, AJO, RTCDP).
Exceções limitadas: os acrônimos podem aparecer entre parênteses na primeira utilização para SEO ou no índice
entradas, metadados de descrição e cabeçalhos nos quais o comprimento é uma preocupação.
- Capitalização do Analytics: os nomes dos painéis estão em minúsculas (em branco, atribuição, experimentação,
forma livre; exceção: &quot;tela de Jornada&quot;). Os nomes de visualização estão em minúsculas (barra, rosca,
histograma, linha, mapa de árvore, texto).

### Terminologia de recurso e conceito

| Correto | NÃO usar |
|---|---|
| encaminhamento de eventos | encaminhamento pelo lado do servidor, Launch Server Side |
| incluir na lista de permissões | lista de permissões |
| INCLUIR NA LISTA DE BLOQUEIOS / INCLUIR NA LISTA DE BLOQUEIOS | blacklist |
| primário / réplica OU primário / secundário (servidores) | master / slave |
| principal (ramificação GitHub) | master |
| hacker ético | hacker de chapéu branco |
| remarketing | redirecionamento |
| grupo de campos | mixin (obsoleto), Extensões, Mixins |
| expiração automática de dados | TTL, tempo de vida útil, expiração |
| sandbox de não produção | preparo (como um nome de ambiente) |
| definição de segmento | segmento (sozinho, quando significa a definição) |
| ID (sempre usar maiúsculas) | ID |
| assimilação / assimilação / assimilado | integração (para adicionar dados à Platform) |
| conjunto de dados/conjuntos de dados | Arquivo de dados, arquivos de conjunto de dados |
| controle de acesso | permissões (para o recurso Plataforma) |
| widget | cartão métrico (obsoleto) |
| variável de espaço reservado | variável fictícia |
| indisponível / bloqueado / desativado / desativado | esmaecido |
| verificação de coerência | verificação de sanidade |
| incorporado | nativo (como sinônimo de interno) |
| alta prioridade | unha imperfeita |
| legacy | cláusula avô |
| principal / principal / origem | principal (como descritor) |

### Termos exclusivos internos: NUNCA use em documentos voltados para o público

| Termo interno | Use no lugar dele |
|---|---|
| AEP | Adobe Experience Platform |
| PALMA | gerenciamento de sandbox/controle de acesso |
| BIOMA | ambiente |
| Hidratação / hidratação | criar/preencher |
| Perfil unificado | Perfil do cliente em tempo real |
| Preparo (ambiente) | sandbox de não produção |
| DTM | Tags |
| Locatário | Organização/organização IMS |
| CRUD | criar, ler, atualizar e excluir (soletrar) |
| Siphon, BSO, Ethos | nomes de código internos, nunca externos |
| Lúpulo | GDPR interno/termo de controle de acesso |
| Ritmo | termo de publicidade não voltada para o usuário |
| Pipeline | termo da infraestrutura interna do Adobe |

## &#x200B;4. Linguagem e acessibilidade inclusivas

### Princípios linguísticos inclusivos

- Use termos neutros em termos de gênero: &quot;representante de vendas&quot; não &quot;vendedor&quot;, &quot;moderador&quot; não &quot;presidente&quot;.
- Prefira uma segunda pessoa (&quot;você&quot;) para evitar pronomes de gênero.
- Use &quot;eles&quot; no singular para uma pessoa cujo gênero é desconhecido. NÃO utilize ele/ela ou ele/ela.
- Inclua nomes de culturas não brancas em exemplos (por exemplo, Ayesha, Ibrahim, Vignesh, Quynh).
NÃO use apenas nomes culturalmente brancos.
- NÃO confunda sexo (masculino/feminino) com gênero (homem/mulher).
- Capitalize nacionalidades, povos, raças (diferentes de &quot;brancas&quot;, de acordo com o AP Stylebook) e tribos.
- Use a linguagem de uma pessoa: &quot;pessoas que usam tecnologia assistiva&quot;, não &quot;os deficientes&quot;.
- Evite eufemismos como &quot;deficientes de forma diferente&quot;. Evite descritores usados como substantivos: &quot;o cego&quot;,
&quot;o surdo.&quot;
- Evite termos que reflitam identidade/apropriação cultural: espírito animal, Sherpa, pow wow,
guru, ninja, tribo.

### Terminologia não inclusiva a ser evitada

| Usar | Não |
|---|---|
| INCLUIR NA LISTA DE PERMISSÕES / INCLUIR NA LISTA DE BLOQUEIOS / INCLUIR NA LISTA DE BLOQUEIOS | lista de permissões/lista negra |
| primário / réplica OU primário / secundário | master / slave |
| principal (ramificação git) | master |
| alta prioridade | unha imperfeita |
| variável de espaço reservado | variável fictícia |
| indisponível / bloqueado / desativado / desativado | esmaecido |
| verificação de coerência | verificação de sanidade |
| incorporado | nativo (como sinônimo) |
| autoridade/especialista | guru / ninja |
| membros do seu grupo | membros da sua tribo |
| reunião | pow wow / circular os vagões |
| modelo de papel / espírito parente | espírito animal |
| guia | Sherpa |
| legacy | cláusula avô |
| empreendimento fútil | março da morte |
| ridículo / incompetente / imprevisível | idiota / manco / louco |
| hacker ético / antiético | chapéu branco / hacker chapéu preto |
| Reproduzir vídeo | Assistir ao vídeo |
| Exibir / Mostrar / Ir para todos | Ver tudo |

### Acessibilidade: descrição da interface

NÃO descreva os elementos da interface do usuário por cor ou posição da tela. Usar cronológico, não espacial,
idioma:

| Usar | Não |
|---|---|
| Primeiro, Próximo, Finalmente | Acima, Abaixo |
| Na barra de menus | À esquerda |
| Antes / Depois | Na parte superior/inferior da tela |

Descreva o que os controles fazem, não a aparência deles:

| Usar | Não |
|---|---|
| Selecionar pesquisa | Clique no ícone de lupa |
| Editar | O ícone de lápis |
| Ligado / Desligado | Alternar / alternar / ativar |
| Menu | Gaveta lateral |
| Inserir email | Digite seu endereço de email |
| Salvar | O botão &quot;Salvar&quot; |
| Cancelar | Fechar |

NÃO use cores sozinhas para transmitir informações. Sempre emparelhar cor com texto ou forma.

### Acessibilidade: texto alternativo, links e vídeos

- **Texto alternativo**: descreva o que a imagem mostra, não apenas seu nome de tela. Uso concluído
frases, palavras completas (leitores de tela escrevem abreviações) e incluem texto relevante
da imagem. As imagens que transmitem informações independentemente do texto ao redor DEVEM ter
texto alternativo.
- **Links**: nunca use &quot;clique aqui&quot; ou &quot;link&quot; como texto de link. Deixar o destino claro de
apenas o texto do link.
- **Vídeos**: NÃO deve ser reproduzido automaticamente. Sempre forneça uma alternativa em texto, transcrição ou link para
instruções escritas. Inclua legendas relevantes.

## &#x200B;5. Fundamentos da sintaxe do Markdown

### Frontmatter (obrigatório em todos os arquivos)

```yaml
---
title: Title Case Title Here
description: Learn how to... or Learn about... (150-160 chars, sentence case).
---
```

- NÃO adicione `exl-id` ao criar uma nova página. É gerado automaticamente na publicação
hora. Preserve apenas `exl-id` campos que já existem em páginas existentes.
- Título: primeira letra maiúscula, máximo de 60 caracteres, sem barra vertical ou nome do produto (adicionado automaticamente).
Os títulos de conceito são frases substantivas; os títulos de tarefa são frases verbais.
- Descrição: primeira letra maiúscula, 150 a 160 caracteres. A primeira frase resume; a segunda é uma
call to action. NÃO comece com o nome do produto nem copie o texto do primeiro parágrafo.

### Cabeçalhos

- `#` = H1 (uma por página, primeira linha após o primeiro assunto). `##`, `###` para subseções. Nunca
níveis ignorados.
- Direcione 5 palavras ou menos, máximo de 69 caracteres. Linha em branco antes e depois de cada cabeçalho.
- Cada cabeçalho deve ser seguido por um corpo de texto; nunca empilhe cabeçalhos ou coloque uma lista/tabela/nota
diretamente sob um título.
- Primeira letra da frase em maiúscula. Os cabeçalhos de conceito são frases substantivas; os cabeçalhos de tarefa são verbos imperativos
(evitar os gerúndios).
- Não há cabeçalhos abstratos de palavra única (&quot;Visão geral&quot;, &quot;Introdução&quot;) sem descrever o tópico.
- IDs de âncora personalizadas: `## Section title {#section-id}` (minúsculas, hifenizadas).

### Links, imagens e código

- As referências cruzadas internas usam caminhos relativos à raiz: `[text](/help/path/to/file.md)`.
Links externos usam URLs `https://` absolutos.
- Nunca use &quot;clique aqui&quot; ou &quot;link&quot; como texto de link. Evite URLs brutos no corpo de texto.
- Texto alternativo: `![alt text](path/to/image.png)`. Frases inteiras, sem abertura &quot;Esta imagem mostra...&quot;.
- Capturas de tela: somente tema leve, sem dados do cliente, sem interface de terceiros, sem imagens de código.
- Os blocos de código cercados usam acentos graves triplos com um identificador de linguagem. Os blocos de código não são
localizado (não é necessário DNL/UICONTROL dentro deles).
- Vídeos: `>[!VIDEO](url?quality=12&learn=on)`. Nunca executar automaticamente; sempre fornecer uma transcrição
ou escrita.

### Avisos

```markdown
>[!NOTE]
>
>Note content here.
```

Uma linha `>` em branco deve separar a linha da marca do conteúdo; cada linha de continuação começa
com `>`. NÃO coloque um `[!NOTE]` imediatamente após um bloco `[!CONTEXTUALHELP]`.

### Popovers de ajuda contextual (`[!CONTEXTUALHELP]`)

`[!CONTEXTUALHELP]` blocos alimentam popover dicas de ferramentas que transformam a experiência em uma experiência
Interface do Platform. Eles vivem nos documentos, mas são renderizados como janelas flutuantes no produto por meio de um feed JSON
gerado no momento da criação.

```markdown
## Configure file names {#configure-file-names}

>[!CONTEXTUALHELP]
>id="platform_destinations_activate_filename"
>title="Configure file name"
>abstract="For file-based destinations, a unique file name is generated per segment. Use the file name editor to create and edit a unique file name or keep the default name."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations.html#file-names" text="Learn more in documentation"
```

Campos obrigatórios: `id`, `title`, `abstract`. Todo o resto é opcional.

**Posicionamento:**
- O bloco deve vir diretamente após um cabeçalho (`#`, `##` ou `###`) que tenha um atributo explícito
ID de âncora (por exemplo, `### Section title {#section-id}`). Nenhum parágrafo ou outro conteúdo entre
o cabeçalho e o bloco, ou o popover, não serão renderizados.
- Vários blocos `[!CONTEXTUALHELP]` podem aparecer consecutivamente na mesma seção (por exemplo,
um por campo sendo documentado).
- NÃO coloque um bloco `[!NOTE]` imediatamente após um bloco `[!CONTEXTUALHELP]`. Quebra
renderização no Experience League (limitação de plataforma conhecida).

**Sintaxe de ID:**
- Formato: `id="platform_<yourarea>_<workflow>_<uiitem>"`, por exemplo
  `id="platform_destinations_activate_deduplicationkey"`.
- As IDs podem conter letras maiúsculas.
- As IDs devem ser exclusivas no conjunto de documentos (verificado no momento da criação). A mesma ID pode ser reutilizada
em vários locais de interface do usuário por engenharia, que produz conteúdo de popover idêntico no
cada ponto. Isso é esperado.

**Links dentro de um popover, use `additional-url`, HTML não embutido:**
- Para adicionar um link, use uma linha separada: `>additional-url="URL" text="Link text"`. NÃO incorporar
  `<a href="...">` ou marcação `[text](url)` dentro da cadeia de caracteres `abstract` para esta finalidade.
- O valor `additional-url` DEVE incluir `.html` no caminho ou o link não será exibido em
a interface (por exemplo, `https://experienceleague.adobe.com/docs/experience-platform/path/to/page.html#anchor`,
não o formulário `/en/docs/...` sem extensão mais recente usado em links corpo-texto em outro lugar).
- Máximo de duas `additional-url` linhas por bloco.
- Um primeiro link é gerado automaticamente a partir do cabeçalho da seção durante a criação do Jenkins. Você
não adicione esse item manualmente e você não poderá renomeá-lo.

**Outra sintaxe com suporte:**
- O campo `abstract` é compatível com HTML/markdown básico para ênfase e estrutura: `<b>`,
  `<br>`, `<ul><li>`, `**bold**`.
- Há suporte para links de vídeo através do mesmo mecanismo `additional-url`/`text`, apontando para um
URL de vídeo direto ou URL do YouTube.

**Observação sobre o fluxo de trabalho** ao entregar uma nova ID de pop-over à equipe de engenharia/interface do usuário (geralmente por meio de um
tíquete Jira), também forneça um URL de fallback (prefira um goURL, se existir para essa página) e
o local da interface do usuário. Este fallback é separado do `additional-url` usado nos documentos
markdown.

### Listas e tabelas

- Use `*` ou `-` consistentemente em um artigo; não misture.
- As listas numeradas usam `1.` para cada item. Os procedimentos de etapa única usam um marcador, não `1.`.
- Não há caixas de seleção de lista de tarefas no estilo GitHub (`- [ ]`); não há suporte no Experience League.
- Listas e tabelas surround com linhas em branco. Mantenha os itens da lista gramaticalmente paralelos.

### Nomeação de arquivos e pastas

- Nomes de arquivo do Markdown: minúsculas com hifens, sem maiúsculas/sublinhados/pontos/espaços.
- Usar descrição (`create-calculated-metric.md`), não nomes simples como `overview.md`.
- As imagens entram em uma subpasta `assets/`; as imagens que não devem ser localizadas entram
  `do-not-localize/`.

## &#x200B;6. Convenções de estrutura e índice

- Três tipos de conteúdo, mantidos separados: **Conceito** (o que/por que, cabeçalhos de substantivo), **Tarefa**
(como, títulos imperativos, sempre precedidos por um conceito), **Referência** (campos,
parâmetros, tabelas).
- Etapas: cada uma é uma única frase completa começando com um verbo ou o objetivo. Target 7
etapas por tarefa, 10 no máximo; dividir procedimentos mais longos em subtarefas.
- TOC.md: entradas de maiúsculas e minúsculas de frases, IDs de âncora válidas em cada cabeçalho de seção, sem duplicatas
entradas de arquivo, sem comentários no meio da lista.
- Ocultar uma página da navegação com `{hide-from-toc}` em `TOC.md` (não é assunto de frente). Ocultar
de mecanismos de pesquisa com `hide: true` no front-matter.
- Nomeação da ramificação: nenhum prefixo de nome de usuário. Usar o número do tíquete Jira e uma descrição em maiúscula ou minúscula
(e.g., `PLAT-12345-Update-Guardrail-Limits`). Nomeie a ramificação e o título da PR da mesma maneira.

## &#x200B;7. Ortografia e pontuação

- Ortografia em inglês americano: cor, reconhecimento, licença, enquanto, expiração, medidor, entre
(não colorido, reconhecido, licenciado, enquanto, expiração, medidor, entre).
- Reservar aspas para citar pessoas; não citar cadeias de caracteres da interface do usuário (use negrito +
  `` em vez disso).
- Use itálico para termos usados como termos (*perfil*, não &quot;perfil&quot;). Usar acentos graves para código,
parâmetros, nomes de arquivo e texto digitado.
- Negrito somente para elementos da interface em procedimentos (com ``) e termos principais no início
introdução.
- Sem ponto e vírgula, sem traços/hifens em prosa, sem réguas horizontais (consulte a seção 1).

## &#x200B;8. Revisar lista de verificação

Antes de terminar qualquer edição, verifique:

- Voz focada no usuário, voz ativa, segunda pessoa, sem &quot;permite&quot;/&quot;permite&quot;
- Frases ≤ 20 palavras, parágrafos ≤ 125 palavras
- Cabeçalhos: caso de frase, ≤5 palavras/69 caracteres, seguido de texto do corpo, sem níveis ignorados
- Nomes e formulários de produtos corretos; sem termos obsoletos, apenas internos ou não inclusivos
- `` em cada elemento da interface do usuário nas etapas; `[!DNL]` em cada nome de produto/terceiro
- Nenhuma tag dentro de blocos de código; campos de metadados com tags encapsulados entre aspas
- Sintaxe de advertência correta; marcadores de lista consistentes; sem listas de tarefas; sem regras horizontais
- O texto alternativo é descritivo e completo; sem &quot;clique aqui&quot;; sem linguagem espacial/direcional
- Nenhuma cor é usada sozinha para transmitir informações; os vídeos não são reproduzidos automaticamente
- Presença do primeiro plano obrigatório; links internos relativos à raiz; nomes de arquivo hifenizados em minúsculas
