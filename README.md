

## Índice
- [Guia para rodar o site local](#Guia-para-rodar-o-site-local)
- [Guia de criação do Site Hugo e implementação do Tema Roxo](#Guia-de-criação-do-Site-Hugo-e-implementação-do-Tema-Roxo)
- [Guia de desenvolvimento do Site](#Guia-de-desenvolvimento-do-Site)


### Guia para rodar o site local 

- Clonar o repositório
- Acesse a pasta raiz do diretório
- use o seguinte comando:
```bash 
hugo server
```
- Basta abrir o navegador e digitar http://localhost:1313
    
### Guia de criação do Site Hugo e implementação do Tema Roxo
- Tema [Hugo Roxo](https://themes.gohugo.io/themes/roxo-hugo/)    
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
 

### Guia de desenvolvimento do Site
#### **config.toml** 
- É o arquivo que guarda a estrutura do site. Títulos, menus..... São todos definidos aqui.

#### **Gerindo e criando Conteúdo**
- Cada página tem sua estrutura de pastas para armazenar o conteúdo em documentos markdown
![image](https://github.com/uiro-bi/uiro-roxo/assets/153785820/37710568-aaa1-4d9f-9da4-b7dae19e70c2)
- Cada pasta de **content** tem um arquivo **_index.MD** que contém o heading das páginas seguindos por aquivos **MD** com o conteúdo

#### **Customizando o site**
- folder **data**
- folder **static/images**
armazena imagens usadas no background e nos tópicos do site. As pastas tem o mesmo nome dos menus de navegação
![image](https://github.com/uiro-bi/uiro-roxo/assets/153785820/89c7e542-9d0e-4079-8d3b-c7b9310f3e6b)

