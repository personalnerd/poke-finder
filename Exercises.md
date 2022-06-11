## Exercícios

A fim de confirmar a participação nas aulas e poder lançar uma nota final, é necessário que os alunos da disciplina "Vue.js Development", do curso de pós-graduação "Web Development", realizem os exercícios estipulados a seguir, sugerindo-se clonar este repositório, efetuar as modificações necessárias, e por fim entregar a URL do repositório modificado.

1. Acrescentar botões para alternar ordenação na lista de Pokémons (por número em ordem crescente ou por nome em ordem alfabética). A lista deve reagir reativamente conforme forem clicados tais botões.
2. Fazer a pesquisa de Pokémons ocorrer em tempo real, durante a digitação, a cada alteração no valor informado. O <kbd>Enter</kbd> na caixa de pesquisa ou o clique na lupa não serão mais necessários.

Enviar para [erickpetru@gmail.com](mailto:erickpetru@gmail.com) o endereço do clone com a solução. Entrega até **19/06/2022**.

&nbsp;

### Solução 1 - ordenação

Criei um componente `SortButtons` e registrei dentro do componente `ItemList`, acima da lista.

O componente `SortButtons` emite os valores `"id"` ou `"name"` no clique nos botões.

O valor é recebido no componente pai, que executa uma função que atualiza uma variável reativa `sortBy`, que foi adicionada no `filteredItems`, ordenando os itens antes do filtro.

&nbsp;

### Solução 2 - pesquisa em tempo real

Alterar o `@keyup.enter="updateModelValue"` para `@keyup="updateModelValue"` no componente `SearchField`, fazendo com que o `updateModelValue` seja chamado a cada letra digitada, em vez de esperar a tecla Enter.

&nbsp;

Tarcisio Uchoa - 11/06/2022
