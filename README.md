# Controle do Almoxarifado de Química

Sistema web criado como projeto acaêmico para auxiliar no controle do 
**Almoxarifado do Laboratório de Ensino Química da Universidade de Santa Cruz do Sul (UNISC)**.

## Objetivo

O objetivo do software é facilitar a organização e o controle dos
reagentes químicos do almoxarifado, centralizando em uma única
aplicação o cadastro dos frascos, a consulta do estoque e o registro das
movimentações.

O sistema permite identificar individualmente os frascos por código e
subcódigo, acompanhar as quantidades disponíveis, registrar retiradas e
devoluções e consultar quais reagentes estão atualmente em uso. Também
mantém o histórico das movimentações, possui uma relação específica para
reagentes PF e oferece recursos de relatórios e backup.

A proposta é tornar o controle do almoxarifado mais organizado e
prático, reduzindo a dependência de registros manuais e facilitando a
consulta das informações durante a rotina do laboratório.

O projeto funciona localmente em **HTML, CSS e JavaScript**, sem
necessidade de servidor ou banco de dados externo. Os dados são
armazenados no navegador e podem ser exportados em JSON para backup.

## Funcionalidades

-   Painel com resumo do almoxarifado e movimentações recentes.
-   Consulta e busca de reagentes.
-   Relação específica de reagentes PF.
-   Cadastro e gerenciamento individual de frascos.
-   Controle de código e subcódigo.
-   Registro de conteúdo, tara, massa total, massa real, tipo e
    densidade.
-   Retirada de um ou vários frascos.
-   Campos adicionais obrigatórios para reagentes PF.
-   Devolução com cálculo da quantidade utilizada ou adicionada.
-   Controle de frascos disponíveis e em uso.
-   Histórico de movimentações e relatórios.
-   Pesquisa e filtros nas principais listas.
-   Exportação de consultas em CSV.
-   Backup e restauração em JSON.
-   PIN opcional para ações protegidas.
-   Atalhos de teclado.

## Consulta

A área **Consultar** possui duas visualizações.

### Busca de reagentes

Apresenta uma visão consolidada dos reagentes, agrupando os frascos pelo
código:

-   Código
-   Reagente
-   Fórmula molecular
-   Número de frascos
-   Quantidade no almoxarifado

### Relação de reagentes PF

Apresenta as movimentações dos reagentes PF com informações de retirada
e devolução, incluindo código, subcódigo, peso, datas, laboratório,
disciplina, diversos, complemento, responsável e quantidade gasta.

## Retiradas e devoluções

É possível selecionar um ou vários frascos para retirada. Quando houver
pelo menos um reagente **PF**, o sistema apresenta campos adicionais
obrigatórios, atribuídos somente aos PF selecionados.

As retiradas em aberto ficam disponíveis para devolução. O sistema
utiliza o peso informado e os dados do frasco para atualizar seu
conteúdo, inclusive permitindo registrar acréscimo de material.

## Armazenamento e backup

Os dados são mantidos no navegador utilizando `localStorage`.

> **Importante:** limpar os dados do navegador pode apagar as
> informações armazenadas. Faça backups periódicos pela área de
> configurações.

Os backups podem ser exportados e restaurados em arquivos JSON. Os dados
cadastrados no navegador não são enviados automaticamente para o GitHub.

## Como executar

Não é necessário instalar dependências.

1.  Baixe o arquivo HTML.
2.  Abra-o em um navegador moderno.
3.  O sistema estará pronto para uso.

## Tecnologias

-   HTML5
-   CSS3
-   JavaScript
-   Web Storage API (`localStorage`)

## Atalhos

  Atalho      Função
  ----------- -----------------------
  `Alt + E`   Consultar
  `Alt + R`   Retirar
  `Alt + D`   Devolver
  `Alt + K`   Cadastrar novo frasco
  `Alt + H`   Histórico
  `Alt + P`   Relatórios
