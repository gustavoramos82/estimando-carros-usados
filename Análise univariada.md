# Estimando preço dos carros - análise univariada e verificação inicial

## Verificação do dataset

Temos um dataset de 13 colunas e 5847 linhas o que não é um dataset muito grande e que temos uma variavel taget que o preço do carro, abaixo temos 
um dicionário dos dados para verificar como cada coluna se trata

### Dicionário dos dados

- **Name**: Marca e modelo do carro
- **Location**:Cidade em que o carro foi listado
- **Year**: Ano em que o carro foi produzido
- **Kilometers_Driven**: Total de quilômetros dirigidos
- **Fuel_Type**: Tipo de combustivel
- **Transmission**: Tipo de transmissão se é manual ou automático
- **Owner_Type**: Tipo do proprietário
- **Mileage**: Quilometragem padrão oferecida pela montadora em kmpl ou km/kg
- **Engine**: Volume de cilindrada do motor em CC
- **Power**: Numer de power da máquina
- **Seats**: Número de assentos no carro
- **Price**: Preço do carro em INR Lakhs (Rúpia indiana)
- **New_Price**: Preço de um carro novo de um mesmo modelo

### Sobre o dataset

Verificando sobre se o dataset tem valores em brancos, temos que uma coluna tem muitos valores em branco, então o mesmo será excluido, e os outros que tem algum
valores em branco vão ser tratados posteriormente

![image](https://github.com/gustavoramos82/estimando-carros-usados/assets/39843884/aa0d5d24-e01a-406b-aa8f-6c8b4c3bc428)

Depois de ser feito isso verificaremos uma olhada nas medidas-resumo

![image](https://github.com/gustavoramos82/estimando-carros-usados/assets/39843884/85d344c6-24e9-4dc8-9cbe-0d7a254d0add)

Podemo ver que algumas colunas como: Preço, Engine, e quilometros dirigidos não seria interessante usar a média como refere^ncia , enquanto outros como o ano,
a média pode ser uma referência

Foi criado uma coluna de marca do carro, com base na primeira coluna e fala sobre o modelo do carro

## Análise univariado

![image](https://github.com/gustavoramos82/estimando-carros-usados/assets/39843884/c74baef1-90bb-4cf5-b461-edfa3a611f9b)

Podemos ver que, em relação ao preço, temos que a maioria dos valores, em sua maioria, estão até 20, percebe-se que há valores muito caros de carro, dai será verificado
se é um tipo diferente de carro ou é devido a quilometragem rodada, por exemplo

A maioria dos carros foram produzidos entre 2013 a 2016, em sua maioria

![image](https://github.com/gustavoramos82/estimando-carros-usados/assets/39843884/caad0476-3e7f-441e-9b5e-fdb2bf603aca)

Poucos carros é do tipo elétrico

![image](https://github.com/gustavoramos82/estimando-carros-usados/assets/39843884/3268f040-4ef3-4c15-9e2e-e55ef499d9c9)

A maioria tem tipo de transmissão manual

![image](https://github.com/gustavoramos82/estimando-carros-usados/assets/39843884/42ef5ec7-f827-4971-af46-24d7e2a972fb)

Em volume de cilidradas, a maioria dos motores está em torno de 1000

![image](https://github.com/gustavoramos82/estimando-carros-usados/assets/39843884/06924684-d5ac-4707-a58c-f19e538b8d60)

Em questão de marca, amioria é da Maruti ou da Hyundai

![image](https://github.com/gustavoramos82/estimando-carros-usados/assets/39843884/88e5dee4-3f42-460a-bc62-e31ab1931d75)

A maioria dos carros tem 5 assentos

![image](https://github.com/gustavoramos82/estimando-carros-usados/assets/39843884/c63a5707-9930-4b21-a34a-81cd8827f861)

A potência da máquina está em torno de 100 em sua maioria

![image](https://github.com/gustavoramos82/estimando-carros-usados/assets/39843884/64c9ac08-9176-441a-a6fa-a6961c02bb38)

Em questão de Quilometros rodados, temos que temos valores extremos, no qual será verificado que isso tem relação com o preço e se faz sentido manter esses
valores e procurar entender alguma relação com o preço ou o numero de assentos

## Conclusões da análise

A partir dessa analise inicial,temos que:

- A mioria dos carros tem 5 assentos
- a maioria do preço é de até 20
- A maioria so tem um motorista antes para utilizar o carro
- A maioria dos carros ou da da Hyundai e Maruti
- Poucos carros são do tipo elétrico

Com isso, vai se ter a seguinte análise

- Verificar quais atributos tem relação com a variavel target (preço)
- Verificar se o preço do carro mais altos tem alguma diferença com o geral
- Fazer uma análise sobre os quilometrois rodados se tem relação com preço ou outros fatores
