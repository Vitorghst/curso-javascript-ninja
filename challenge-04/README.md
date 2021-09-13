# Desafio da semana #4

```js
/*
Declare uma variável chamada `isTruthy`, e atribua a ela uma função que recebe
um único parâmetro como argumento. Essa função deve retornar `true` se o
equivalente booleano para o valor passado no argumento for `true`, ou `false`
para o contrário.
*/
var isTruthy = function( a ) {
return !!a;
};

// Invoque a função criada acima, passando todos os tipos de valores `falsy`.
isTruthy(0)
isTruthy(-0)
isTruthy(null)
isTruthy("")
isTruthy(undefined)
isTruthy(NaN)
isTruthy('')
/*
Invoque a função criada acima passando como parâmetro 10 valores `truthy`.
*/
isTruthy(10) // True

/*
Declare uma variável chamada `carro`, atribuindo à ela um objeto com as
seguintes propriedades (os valores devem ser do tipo mostrado abaixo):
- `marca` - String
- `modelo` - String
- `placa` - String
- `ano` - Number
- `cor` - String
- `quantasPortas` - Number
- `assentos` - Number - cinco por padrão
- `quantidadePessoas` - Number - zero por padrão
*/
carros
{
  marca: 'Fiat',
  modelo: 'Strada',
  placa: 'AVN1575',
  ano: 2020,
  cor: 'Branco',
  quantasportas: 2,
  assentos: 5,
  quantidadedePessoas: 0
}

/*
Crie um método chamado `mudarCor` que mude a cor do carro conforme a cor
passado por parâmetro.
*/
 carros.mudarCor = function(cor) {
... carros.cor = cor;
... };

/*
Crie um método chamado `obterCor`, que retorne a cor do carro.
*/
carros.obterCor = function() {
... return carros.cor;
... };

/*
Crie um método chamado `obterModelo` que retorne o modelo do carro.
*/
 carros.obterModelo = function() {
... return carros.modelo;
... };

/*
Crie um método chamado `obterMarca` que retorne a marca do carro.
*/
carros.obterMarca = function() {
... return carros.marca;
... };

/*
Crie um método chamado `obterMarcaModelo`, que retorne:
"Esse carro é um [MARCA] [MODELO]"
Para retornar os valores de marca e modelo, utilize os métodos criados.
*/
carros.obterMarcaModelo = function() {
... return "Esse carro é um " + carros.marca + ' ' + carros.modelo
... };

/*
Crie um método que irá adicionar pessoas no carro. Esse método terá as
seguintes características:
- Ele deverá receber por parâmetro o número de pessoas entrarão no carro. Esse
número não precisa encher o carro, você poderá acrescentar as pessoas aos
poucos.
- O método deve retornar a frase: "Já temos [X] pessoas no carro!"
- Se o carro já estiver cheio, com todos os assentos já preenchidos, o método
deve retornar a frase: "O carro já está lotado!"
- Se ainda houverem lugares no carro, mas a quantidade de pessoas passadas por
parâmetro for ultrapassar o limite de assentos do carro, então você deve
mostrar quantos assentos ainda podem ser ocupados, com a frase:
"Só cabem mais [QUANTIDADE_DE_PESSOAS_QUE_CABEM] pessoas!"
- Se couber somente mais uma pessoa, mostrar a palavra "pessoa" no retorno
citado acima, no lugar de "pessoas".
*/
carros.adicionarPessoas = function (numeroPessoas) {
  var totalPessoas = carros.quantidadedePessoas + numeroPessoas;

  if (carros.quantidadedePessoas === carros.assentos && totalPessoas >= carros.assentos) {
    return 'O carro já está lotado!';
  }

  if (totalPessoas > carros.assentos) {
    var quantasPessoasCabem =  carros.assentos - carros.quantidadedePessoas;
    var pluralOuSingular = quantasPessoasCabem === 1 ? ' pessoa' : ' pessoas';
    return 'Só cabem mais ' + quantasPessoasCabem + pluralOuSingular + '!';
  }

  carros.quantidadedePessoas += numeroPessoas;

  return 'Já temos ' + carros.quantidadedePessoas + ' pessoas no carro!';
};

/*
Agora vamos verificar algumas informações do carro. Para as respostas abaixo,
utilize sempre o formato de invocação do método (ou chamada da propriedade),
adicionando comentários _inline_ ao lado com o valor retornado, se o método
retornar algum valor.

Qual a cor atual do carro?
*/
carros.obterCor()
'Branco'

// Mude a cor do carro para vermelho.
carros.mudarCor('Vermelho')

// E agora, qual a cor do carro?
Vermelho

// Mude a cor do carro para verde musgo.
carros.mudarCor('Verde musgo')

// E agora, qual a cor do carro?
Verde musgo

// Qual a marca e modelo do carro?
carros.obterMarcaModelo()

// Adicione 2 pessoas no carro.
carros.adicionarPessoas(2)

// Adicione mais 4 pessoas no carro.
carros.adicionarPessoas(4)

// Faça o carro encher.
carros.adicionarPessoas(1)
'O carro já está lotado!'

// Tire 4 pessoas do carro.
carros.adicionarPessoas(1)
'O carro já está lotado!'

// Adicione 10 pessoas no carro.
carros.adicionarPessoas(10)
'Só cabem mais 4 pessoas!'
// Quantas pessoas temos no carro?
carros.quantidadePessoas; 
```
