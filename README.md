# Resultados das loterias da Caixa

#### Repositório com atualização automática de arquivos com todos resultados das loterias da Caixa no formato JSON e CSV. 

#### Os arquivos com todos os resultados dos sorteios até <b><dia>08/03/2024 21h32m</dia></b> estão disponiveis no link abaixo:

- [Latest Release](https://github.com/rabuchaim/resultados_loterias_caixa/releases/latest) - https://github.com/rabuchaim/resultados_loterias_caixa/releases/latest - <b><diahora>08/03/2024 às 21:32:56</diahora></b>

### Atualizações

As verificações por novos resultados ocorrem diariamente a partir 20h00, fazendo consultas na API da Caixa de 15 em 15 minutos até 00h00 (horário de Brasília). Sempre que existir um novo resultado de qualquer sorteio, é gerado uma [release](https://github.com/rabuchaim/resultados_loterias_caixa/releases/latest) (link no lado direito dessa página) contendo todos esses arquivos atualizados e compactados.

### De onde os dados são coletados?

Todos os resultados são coletados diretamente dos servidores de [API dos resultados](#endere%C3%A7o-dos-servidores-de-api-de-resultados-da-caixa) da Caixa.

Esse repositório foi criado pois a API da Caixa retorna erro 500 com muita frequência, os dados vem com muita sujeira em unicode (na Timemania tem muito), retorno, quebra de linhas e vírgulas no campo observação (o que quebra a conversão para CSV), e os dados aqui já estão com todos esses problemas corrigidos.

Aqui são disponibilizados arquivos contendo todos os resultados de cada loteria nos formatos CSV (separado por vírgulas) e JSON (igual ao formato retornado pela API da Caixa).

```
[
   {
      "numero": 1,
      "acumulado": true,
      "dataApuracao": "11/03/1996",
      "dataProximoConcurso": "",
      "dezenasSorteadasOrdemSorteio": [
         "41",
         "05",
         "04",
         "52",
         "30",
         "33"
      ],
      "exibirDetalhamentoPorCidade": true,
      "id": null,
      "indicadorConcursoEspecial": 1,
      "listaDezenas": [
         "04",
         "05",
         "30",
         "33",
         "41",
         "52"
      ],
      "listaDezenasSegundoSorteio": null,
      "listaMunicipioUFGanhadores": [],
      "listaRateioPremio": [
         {
            "descricaoFaixa": "6 acertos",
            "faixa": 1,
            "numeroDeGanhadores": 0,
            "valorPremio": 0.0
         },
         {
            "descricaoFaixa": "5 acertos",
            "faixa": 2,
      .
      .
      .
      "valorAcumuladoProximoConcurso": 1714650.23,
      "valorEstimadoProximoConcurso": 0.0,
      "valorSaldoReservaGarantidora": 0.0,
      "valorTotalPremioFaixaUm": 0.0
   },
   {
      "numero": 2,
      "acumulado": false,
      "dataApuracao": "18/03/1996",
      .
      .
      .
```

E para o formato CSV, é o mesmo formato disponibilizado para download ao final da página de cada loteria. A primeira linha de cada arquivo indica a descrição do campo. Exemplo abaixo para a Lotofácil:

```
Concurso,Data Sorteio,Bola1,Bola2,Bola3,Bola4,Bola5,Bola6,Bola7,Bola8,Bola9,Bola10,Bola11,Bola12,Bola13,Bola14,Bola15,Ganhadores 15 acertos,Cidade / UF,Rateio 15 acertos,Ganhadores 14 acertos,Rateio 14 acertos,Ganhadores 13 acertos,Rateio 13 acertos,Ganhadores 12 acertos,Rateio 12 acertos,Ganhadores 11 acertos,Rateio 11 acertos,Acumulado 15 acertos,Arrecadacao Total,Estimativa Prêmio,Acumulado sorteio especial Lotofácil da Independência,Observação
1,29/09/2003,18,20,25,23,10,11,24,14,06,02,13,09,05,16,03,5,BA;PR;SP,49765.82,154,689.84,4645,10.0,48807,4.0,257593,2.0,0.0,0.0,0.0,0.0,Estimativa de prêmio (15 ACERTOS) próximo concurso: R$250.000,00.
2,06/10/2003,23,15,05,04,12,16,20,06,11,19,24,01,09,13,07,1,SP,596323.7,184,1388.95,6232,10.0,81252,4.0,478188,2.0,0.0,0.0,0.0,0.0,ESTIMATIVA DE PRÊMIO PARA O PRÓXIMO CONCURSO (15 ACERTOS): R$500.000,00
3,13/10/2003,20,23,12,08,06,01,07,11,14,04,16,10,09,17,24,2,SP,400623.7,158,2173.36,6897,10.0,96244,4.0,608211,2.0,0.0,0.0,0.0,0.0,Estimativa de prêmio (15 ACERTOS) próximo concurso: R$700.000,00.
.
.
.
2984,20/12/2023,23,24,07,06,09,20,13,15,14,08,18,03,02,25,05,4,ARAPIRACA/AL;FEIRA DE SANTANA/BA;INDEPENDENCIA/CE;CUIABA/MT,307110.27,325,1132.2,11785,30.0,128872,12.0,618720,6.0,0.0,19475994.0,1700000.0,36182149.07,
2985,21/12/2023,19,03,07,21,14,04,12,15,24,18,25,05,02,11,22,1,BACABAL/MA,1540162.83,227,2032.33,7590,30.0,99430,12.0,530440,6.0,0.0,18805680.0,1700000.0,36554769.12,
2986,22/12/2023,22,23,07,13,12,10,16,25,19,20,04,01,18,03,14,0,,0.0,519,792.97,12597,30.0,124041,12.0,601236,6.0,1373965.73,19929960.0,4000000.0,36887180.2,
```

### Endereço dos servidores de API de resultados da Caixa

Se você acessar os links abaixo, vai ter acesso ao resultado mais recente de cada uma das loterias da Caixa. Para acessar sorteios anteriores, basta adicionar o número do sorteio ao final do respectivo endereço. O resultado é bem completo e é o mesmo utilizado nesse repositório, só que aqui é disponibilizado um pacote com todos os resultados.

- Dia de Sorte: https://servicebus2.caixa.gov.br/portaldeloterias/api/diadesorte/

- Dupla Sena: https://servicebus2.caixa.gov.br/portaldeloterias/api/duplasena/

- Federal: https://servicebus2.caixa.gov.br/portaldeloterias/api/federal/

- Loteca: https://servicebus2.caixa.gov.br/portaldeloterias/api/loteca/

- Lotofácil: https://servicebus2.caixa.gov.br/portaldeloterias/api/lotofacil/

- Lotomania: https://servicebus2.caixa.gov.br/portaldeloterias/api/lotomania/

- +Milionária: https://servicebus2.caixa.gov.br/portaldeloterias/api/maismilionaria/

- Megasena: https://servicebus2.caixa.gov.br/portaldeloterias/api/megasena/

- Quina: https://servicebus2.caixa.gov.br/portaldeloterias/api/quina/

- Super Sete: https://servicebus2.caixa.gov.br/portaldeloterias/api/supersete/

- Timemania: https://servicebus2.caixa.gov.br/portaldeloterias/api/timemania


### Qualquer dúvida, sugestões ou problemas nos resultados

E-mail: ricardoabuchaim at gmail dot com