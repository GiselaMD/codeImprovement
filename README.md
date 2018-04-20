# Code Improvement

Por Gisela Miranda Difini

Para este desafio, escolhi demonstrar uma melhoria feita com TypeScript, utilizando o framework Angular 5. Havia a necessidade de apresentar uma lista de dados na página HTML. 

## Problema

O problema estava na grande quantidade de listas criadas dentro do HTML que poderiam ser reduzidas.

## Solução

Com o ngFor, foi possível reutilizar os elementos DOM da lista de dados no HTML. O ngFor tenta evitar a constante criação e destruição de elementos DOM e com isso, muitos dos elementos DOM existentes serão reutilizados e somente os valores dentro deles serão sobrescritos. Para implementar o ngFor, foram criadas classes externas (para não precisar repetir as classes em cada página) contendo os valores das listas de dados, podendo então chamar essas classes em cada página e compartilhar seus dados por um “import”. No HTML, os elementos reutilizados foram os <ion-card>, os <ion-list> e os <ion- item>. 

Redução de 495 linhas!

Foram criados imports em uma página typescript das classes utilizadas na mesma, com suas respectivas interfaces que nada mais são do que interfaces que possibilitam criar a "estrutura" da classe, removendo a necessidade de repetição caso duas ou mais classes tenham a mesma estrutura.