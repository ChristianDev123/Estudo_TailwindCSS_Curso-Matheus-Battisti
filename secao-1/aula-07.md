# Criação de arquivo de configuração:

Para criar o arquivo de configuração do tailwind deve-se utilizar o comando abaixo:

``` CMD
    npx tailwindcss init
```

Será necessário buildar o arquivo para conseguir utilizar as configurações criadas;

# Build de configurações do tailwind:

Para realizar build utilize o comando a baixo:

> o argumento -o significa output (determina a saída do comando);

``` CMD
    npx tailwindcss build arquivo.css -o path/de/build.css
```

# Inicialização do projeto:

Para iniciar um projeto com tailwind adicione a linha a baixo no arquivo tailwind.config.js

``` JS
{
    content: ["./src/*.html"],
}
```

e então acione o watcher do tailwind com o comando a abaixo:

``` CMD
    npx tailwindcss build arquivo.css -o path/de/build.css --watcher
```

Assim qualquer alteração nos arquivos .html ou .js o tailwind irá realizar build para adicionar a classe no arquivo de saída.

