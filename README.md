# React + Vite deploy

## Como Rodar o projeto em modo DEV?
npm run dev

## Como Rodar o projeto em modo PROD?
npm run preview

## Conhecendo as configurações do package-json         
 >''scripts'': {
    >''dev'': ''vite'',
    >''build'': ''vite build'',
    >''preview'': ''vite preview'',
    >''deploy'': ''gh-pages -d dist''
  >},

>Esse é o --package-json arquivo de configuração do projeto, nele você pode adicionar novos scripts(blocos de códigos para rodar comandos), como por exemplo: test, lint, etc...
>Em nosso script temos 3 comandos:
>dev: Roda o projeto em modo de desenvolvimento
>build: Builda o projeto para produção
>preview: Roda o projeto buildado em modo de produção
>deploy: Faz o deploy do projeto para o github pages 

## Como buildar o projeto para produção?
npm build

## Como fazer o deploy do projeto?
npm run deploy

>Como configurar o Vite para fazer o deploy para o github pages?
>1. Instale a dependência gh-pages
>npm install gh-pages --save-dev
>2. Adicione o script de deploy no package.json
>''scripts'': {
    >''dev'': ''vite'',
    >''build'': ''vite build'',
    >''preview'': ''vite preview'',
    >''deploy'': ''gh-pages -d dist''
  >},
>3. Adicione a propriedade base no arquivo vite.config.js
>export default defineConfig({
  >base: '/react-vite-deploy/'
>})
>A propriedade base é o caminho do projeto no github pages, por exemplo: https://seu-usuario.github.io/nome-do-repositorio/
> Então a base seria: /nome-do-repositorio/
> Assim Ex:
>export default defineConfig({
  >base: 'https://seu-usuario.github.io/nome-do-repositorio/'
>})
