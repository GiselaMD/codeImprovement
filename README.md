# Code Improvement

Por Gisela Miranda Difini

Para este desafio, escolhi demonstrar uma melhoria feita com TypeScript, utilizando o framework Angular 5. Havia a necessidade de apresentar uma lista de dados na p�gina HTML. 

## Problema

O problema estava na grande quantidade de listas criadas dentro do HTML que poderiam ser reduzidas.

## Solu��o

Com o ngFor, foi poss�vel reutilizar os elementos DOM da lista de dados no HTML. O ngFor tenta evitar a constante cria��o e destrui��o de elementos DOM e com isso, muitos dos elementos DOM existentes ser�o reutilizados e somente os valores dentro deles ser�o sobrescritos. Para implementar o ngFor, foram criadas classes externas (para n�o precisar repetir as classes em cada p�gina) contendo os valores das listas de dados, podendo ent�o chamar essas classes em cada p�gina e compartilhar seus dados por um �import�. No HTML, os elementos reutilizados foram os <ion-card>, os <ion-list> e os <ion- item>. 

Redu��o de 495 linhas!

Foram criados imports em uma p�gina typescript das classes utilizadas na mesma, com suas respectivas interfaces que nada mais s�o do que interfaces que possibilitam criar a "estrutura" da classe, removendo a necessidade de repeti��o caso duas ou mais classes tenham a mesma estrutura.