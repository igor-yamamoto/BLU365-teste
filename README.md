<div style="text-align:center"><img src="img/índice.png" /></div>

# BLU365 - Teste
Este repositório contém a minha solução para o teste proposto pela [BLU365](https://blu365.com.br/). Maiores informações podem ser encontradas no [documento de proposta do teste](descricao.pdf).

## O desafio
O desafio consiste em analisar um banco de dados, em formato `csv`, o qual contém diversos campos relacionados a acordos estabelecidos entre clientes e credores. Os atributos são:

| Atributo | Descrição |
| - | - |
| **documento** | Documento que identifica o usuário, pode ser um CPF ou CNPJ. Nesse campo contém apenas números, porém não deve ser considerado um inteiro |
| **nome** | Nome do usuário que realizou o acordo |
| **contrato** | Código que os credores usam para identificar uma dívida |
| **ValorAcordo** | Valor que usuário negociou sua dívida |
| **ContratoPlano** | Quantidade de vezes que usuário escolheu parcelar seu acordo, sendo de 1 a 24 vezes |
| **ValorParcela** | Valor de cada parcela do acordo |
| **DataVencimento** | É a data máxima que o usuário pode pagar uma parcela, após essa data o acordo pode quebrar. (Apenas o vencimento da primeira parcela foi disponibilizada) |

Alguns acordos podem ser invalidados dependendo de critérios. Eles são:
- O Valor do Acordo deve ser igual a soma dos valores de cada parcela do acordo
- A Data de vencimento deve ser sempre um dia útil

Assim, o teste consiste em averiguar quais acordos estão ou não validados, dependendo dos dados fornecidos.

## Implementação
O problema foi resolvido em duas implementações distintas, sendo elas em `pandas`, no arquivo [`teste-pandas.ipynb`](teste-pandas.ipynb), e `pyspark`, no arquivo [`teste-pyspark.ipynb`](teste-pyspark.ipynb). Para que os *notebooks* possam rodar, recomenda-se a instalação dos pacotes listados no arquivo [`requirements.txt`](requirements.txt). Para tal, utilize o comando `pip3 isntall -r requirements.txt`.

**Obs**: O driver do `pyspark` deve ter como configuração o jupyter. Para tal, [siga estas instruções, utilizando o método 1](https://www.sicara.ai/blog/2017-05-02-get-started-pyspark-jupyter-notebook-3-minutes).

***

Caso queiram saber mais informações, sintam-se à vontade para me contatar.

:dragon_face: *Code on!* :dragon_face:
