
- Tema [Hugo Roxo](https://themes.gohugo.io/themes/roxo-hugo/)
- Comandos
    - Para inicializar o site localmente, use o seguinte comando:
	- ```bash 
        hugo server
        ```
    - inicializa o site na porta 1313
    
1. Criar site
	1. hugo new site uiro-roxo
	2. cd uiro-roxo
	3. git init


2. Uma vez criado o site e inicializado o repo
	3. Adicionar o tema como submódulo do repo
		1. Um submodulo git é uma forma de manter um repo git como um subdiretório de outro repo. Nesse caso, o thema hugo-roxo fica como um subdiretório do dir principal com Hugo
		2. O submodulo é um repositório independente do principal
	4. ```bash
    		git submodule add git@github.com:StaticMania/roxo-hugo.git themes/roxo-hugo
           ```
		 ![[Pasted image 20240517185417.png]]
	6. Como resultado foi criado o submodulo roxo-hugo dentro do tema;
3. Agora é preciso copiar os arquivos do ExampleSite para o diretório principal com o site Hugo. Isto é feito p/ settar o site com o tema pré definido e com o conteúdo padrão;
	1. `cp -a themes/roxo-hugo/exampleSite/* .`
	2. Explicação dos arquivos que estão sendo copiados
		1. data: contem arquivos de configs (TOML, YAML ou JSON)
		2. content: onde fica o conteúdo como posts, páginas...
		3. static: contém elementos estáticos como imagens, CSS, JavaScript, fontes... O hugo não processa esses arquivos ele só compila;
		4. resources: Arquivos processados e cache do Hugo. Ex minified CSS/JS, imagens modificadas;
		5. config.toml: configs do site e parâmetros que definem como o site é construido e como ele se comporta;
		6. 
