# Odonto Dashboard

Dashboard interativa de preços odontológicos em português, com visual preto e vermelho.

## Usar

Abra `index.html` no Chrome ou Edge. Funciona sem internet e não precisa de instalação nem de servidor.

## Recursos

- 58 procedimentos e preços de 8 instituições na base MÉDIA.
- 17 itens na base SUGESTÃO, com valores pendentes preservados.
- Filtros por base, instituição, procedimento e faixa de preço.
- Seletor suspenso com busca, seleção múltipla e remoção de itens selecionados.
- Linha das médias por procedimento, com o maior valor destacado.
- KPIs e gráficos sincronizados com a seleção.
- Os gráficos exibem tooltips e não alteram os filtros ao clicar.
- Segmentação visual de procedimentos com busca, seleção múltipla e chips removíveis.
- Botão **Redefinir dados** restaura a base MÉDIA e limpa instituição, procedimentos, faixa e buscas.
- Tema visual acompanha a cor da instituição selecionada e volta ao vermelho ao redefinir.
- KPIs e gráficos reaparecem com animação suave após cada mudança de seleção.
- As duas tabelas usam a cor de cada instituição em cabeçalhos e células; a instituição selecionada recebe destaque mais forte.
- Os cinco KPIs laterais assumem a cor, o brilho e o nome da instituição selecionada; ao redefinir, voltam à paleta original.
- Um painel comparativo mostra KPI e minibarra gráfica individual de cada instituição e acompanha a segmentação de procedimentos. Os cartões possuem espaçamento amplo e se reorganizam conforme a largura da tela.
- Sem procedimentos selecionados, os KPIs individuais exibem a média geral de preços de cada instituição; o cartão escolhido é totalmente preenchido pela cor forte do respectivo órgão.
- O gráfico de média por procedimento usa curva suavizada, traço reforçado, brilho discreto e pontos arredondados.
- A coluna lateral de KPIs possui largura fixa, textos contidos e separação reforçada da área dos gráficos para evitar sobreposição.
- A segmentação de procedimentos adapta busca, caixas, chips, rolagem, bordas e ícone à cor da instituição em foco.
- Ao adicionar um procedimento, a instituição volta para “Todas” para evitar uma tela vazia e permitir a comparação; qualquer KPI individual pode focar novamente um órgão.
- Uma tabela lateral **Procedimentos filtrados** aparece durante a seleção, lista os nomes escolhidos e some quando o filtro é limpo.
- Aba DADOS com as colunas na ordem do Excel, busca e exportação CSV.
- A aba DADOS possui botões próprios para baixar PDF paginado em A4 horizontal e Excel `.xlsx` formatado, com filtros, cabeçalho fixo, moeda, larguras ajustadas e cores por instituição.
- O fundo da segmentação de procedimentos e o ícone do dente acompanham a cor da instituição selecionada, mantendo textos brancos e contraste reforçado.
- Ao selecionar uma instituição, os cartões destacados pulsam uma vez e o fundo completo do dashboard muda suavemente para uma tonalidade escura da cor predominante escolhida.
- O fundo externo atrás do painel também recebe um degradê forte da instituição, enquanto os gráficos preservam a base escura e o contraste dos textos.
- A exportação Excel usa estrutura Office Open XML compatível, sem reparo automático, com título premium, grade oculta, aba colorida e impressão horizontal ajustada.
- Logos locais por instituição e ícones ilustrativos com cores fixas.

## Dados e cálculos

Os dados da planilha `MÉDIA -SUGESTÃO.xlsx` recebida estão incorporados ao arquivo. Valores zero são preservados e excluídos das médias, seguindo o critério da coluna MÉDIA original. A base não possui datas; a linha apresenta procedimentos na ordem da planilha.

A aba DADOS conserva os valores de origem e não depende dos filtros da dashboard. As médias por instituição podem considerar cestas diferentes de procedimentos.

## Atualizações

Para atualizar os dados, substitua o conteúdo JSON do elemento `source-data` em `index.html`, mantendo os campos e relacionamentos. Logos enviados pelo botão + ficam no armazenamento local do navegador; não são enviados para um servidor.

## Estrutura

O projeto é um único HTML com CSS, JavaScript, ícones SVG e logo PNG incorporados. Não usa dependências externas, ferramentas de build ou serviços de IA durante o uso.
