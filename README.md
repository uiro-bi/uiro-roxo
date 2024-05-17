
- Tema [Hugo Roxo](https://themes.gohugo.io/themes/roxo-hugo/)

### Rodar o site local 
- Comandos
    - Para inicializar o site localmente
    - Clone o repositório
    - use o seguinte comando:
	- ```bash 
        hugo server
        ```
    - inicializa o site na porta 1313
    
### Criar repositório padrão do Hugo com Site
    
- [Ver guia](https://medium.com/@kiaeisinga/publishing-a-hugo-website-with-the-papermod-theme-to-gitlab-pages-efb9c7ae102e)
1. hugo new site uiro-roxo
2. cd uiro-roxo
3. git init


- Adicionar o tema como submódulo do repo
    1. Um submodulo git é uma forma de manter um repo git como um subdiretório de outro repo. Nesse caso, o thema hugo-roxo fica como um subdiretório do dir principal com Hugo
    2. O submodulo é um repositório independente do principal
    ```bash
    git submodule add git@github.com:StaticMania/roxo-hugo.git themes/roxo-hugo
    ```
- Como resultado foi criado o submodulo roxo-hugo dentro do tema;
- Agora é preciso copiar os arquivos do ExampleSite para o diretório principal com o site Hugo. Isto é feito p/ settar o site com o tema pré definido e com o conteúdo padrão;
    1. ```bash
        cp -a themes/roxo-hugo/exampleSite/* .
        ```

- Explicação dos arquivos que estão sendo copiados
    - *data*: contem arquivos de configs (TOML, YAML ou JSON)
    - *content*: onde fica o conteúdo como posts, páginas...
    - *static*: contém elementos estáticos como imagens, CSS, JavaScript, fontes... O hugo não processa esses arquivos ele só compila;
    - *resources*: Arquivos processados e cache do Hugo. Ex minified CSS/JS, imagens modificadas;
    - *config.toml:* configs do site e parâmetros que definem como o site é construido e como ele se comporta;
        
