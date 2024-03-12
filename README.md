## Configuração do Eslint em Projetos React com Typescript

1. Apague tudo que tiver no arquivo .eslintrc e troque a extensão para .json

2. Se não tiver o arquivo .eslintrc, instale o Eslint com o comando:
```
npm i eslint -D 
```
3. Instale o plugin de configuração da Rocket:
```
npm i @rocketseat/eslint-config -D
```
4. Dentro do arquivo .eslintrc.json vazio, implemente o objeto:
```
{
  "extends":"@rocketseat/eslint-config/react"
}
```
5. Vá lá no settings.json e acrescente a seguinte linha:
```
 "editor.codeActionsOnSave": {
    "source.fixAll.eslint": "explicit"
  },
```
6. No seu terminal, rode o comando para verificar os erros:
```
npx eslint src --ext .ts,.tsx 
```
7. Para corrigir todos os erros, basta digitar o comando:
```
npx eslint src --ext .ts,.tsx --fix
```
8. Para ficar mais prático, esse comando pode ser configurado dentro seu projeto, acrescentando no seu arquivo package.json, a linha:
```
   "scripts": {
   --------------
   "lint": "eslint src --ext .ts,.tsx"
  },
  ```
10. Quando for executar o lint, basta digitar no terminal:
```
npm run lint
```
11. E quando for corrigir todos os arquivos, basta dá o comando no terminal:
```
npm run lint --fix
```

