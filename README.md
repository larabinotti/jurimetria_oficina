# Oficina de jurimetria: tempo do processo

Oficina prática em dois encontros de 1h30, para estudantes de jurimetria, sobre como medir o tempo do processo com dados públicos do DataJud (CNJ) e o pacote [ datajud ] ( https://github.com/jjesusfilho/datajud ) . Os recortes são processos cíveis do TJSP.

## PROGRAMAÇÃO

| Encontro | Tema | Materiais |
| --- | --- | --- |
| Dia 1 | Obter e preparar os dados do DataJud |  ` dia1.md ` , ` dia1.R `  |
| Dia 2 | Medir o tempo e fazer análise de sobrevivência |  ` dia2.md ` , ` dia2.R `  |

O ` roteiro.md ` traz o plano do professor, com tempos, falas e avisos.

## Antes de começar

1 . Instale o [ R ] ( https://cloud.r-project.org ) e o [ Positron ] ( https://positron.posit.co/download.html ) .
2. Instale os pacotes:

``` r
install.packages(c( " tidyverse " , " remotes " , " survival " , " ggsurvfit " ))
remotes :: install_github( " jjesusfilho/datajud " )
```

3 . Para consultar o DataJud ao vivo, guarde a chave da API no ` ~/.Renviron ` (variável ` DATAJUD_API_KEY ` ). Sem a chave, use as bases prontas em ` dados/ ` .

## Conteúdo do

-  ` dia1.R ` e ` dia2.R ` : scripts completos de cada encontro.
-  ` dia1.md ` e ` dia2.md ` : material de projeção.
-  ` coleta_dados.R ` : como as bases de ` dados/ ` foram geradas (rode uma vez, com internet).
-  ` dados/ ` : amostras pequenas, para trabalhar sem depender da rede.

## Avisos

- O DataJud é lento e assustador em local comercial; por isso a oficina usa as bases de ` dados/ ` .
- O DataJud informa a classe atual do processo e não traz processos sigilosos.
