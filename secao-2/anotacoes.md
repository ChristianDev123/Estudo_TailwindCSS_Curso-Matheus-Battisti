# Breakpoints:

Tailwind é um framework Mobile First, ou seja, por conceito é necessário desenvolver o projeto partindo da premissa de utilização de device mobile.

Para cada alteração no tamanho de tela, conforme for crescendo, tem de utilizar as classes a baixo:

- sm (menos frequentemente utiizada);
- md - superior à 768px;
- lg - superior à 1024px;
- xl - superior à 1280px;

Cada um dos breakpoints tem como base resoluções superiores, ou seja, md seria por exemplo, resoluções acima de 768px;

Para atingir responsividade no caso mobile não se utiliza breakpoint;

# Criação de componentes CSS:

Para criar componentes no tailwind é necessário adicionar diretivas no documento .css que importa o tailwind.

``` CSS
    @tailwind base;

    @tailwind components;

    @tailwind utilities;

    /* A diretiva Layer tem serve alterar um import no css */
    @layer  components {
        .classe-component{
            /* apply serve para adicionar a estilização que contém nas classes do tailwind ao código do componente que está sendo criado */
            @apply classes-do-tailwind;
        }
        /* Se necessário utilizar pseudo classe é necessário setar fora das classes de pseudo-classe do tailwind, um exemplo é o hover */
        .classe-component:pseudo-classe{
            @apply classes-do-tailwind-a-serem-ativadas;
        }
    }
```