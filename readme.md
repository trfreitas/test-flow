### Ideia

- Trabalhar com 3 branchs bloqueadas (development, staging e main)
- Branch principal sera a `development`
- `feature`, `chore`, `bugfix` e outros deve ser aberto PR para `development`
- `releasefix` deve ser aberto PR para `staging`
- `hotfix` deve ser aberto PR para `main`

### Validações

- Criar regra para o PR ser aberto apenas com as branches de sufixo relacionado a branch de origem
- PRs para `development` devem ser mergeado com a opção `Merge pull request`
- PRs de `development` para `staging` devem ser mergeado com a opção `Rebase and merge`
- PRs de `staging` para `main` devem ser mergeado com a opção `Rebase and merge`
- PRs de `releasefix` devem ser mergeado com a opção `Merge pull request` e deve ser imediatamente feito `rebease` na branch `development`
- PRs de `releasefix` devem ser mergeado com a opção `Merge pull request` e deve ser imediatamente feito `rebease` para as branchs `development` e `staging`

### Pipeline de qualidade de codigo
- Todos PRs para `development` devem rodar os pipelines
- PRs de `releasefix` devem rodar os pipelines
- PRs de `hotfix` dem rodar os pipelines
