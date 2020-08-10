Declare uma variável chamada `isTruthy`, e atribua a ela uma função que recebe
um único parâmetro como argumento. Essa função deve retornar `true` se o
equivalente booleano para o valor passado no argumento for `true`, ou `false`
para o contrário.

```
const isTruthy = function (i) {
  if (i){
    return true;
  } else {
    return false;
  }
}
```

 Invoque a função criada acima, passando todos os tipos de valores `falsy`.

```
isTruthy(false);
isTruthy(0);
isTruthy(null);
```
Invoque a função criada acima passando como parâmetro 10 valores `truthy`.

```
isTruthy(true);
isTruthy(1);
...
```

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

```
const carro = {
  marca: 'Volkswagen',
  modelo: 'Golf',
  placa: 'XXXXXXX',
  ano: 2020,
  cor: 'Azul',
  quantasPortas: 4,
  assentos: 5,
  quantidadePessoas: 0
};
```

Crie um método chamado `mudarCor` que mude a cor do carro conforme a cor
passado por parâmetro.

```
const carro = {
  marca: 'Volkswagen',
  modelo: 'Golf',
  placa: 'XXXXXXX',
  ano: 2020,
  cor: 'Azul',
  quantasPortas: 4,
  assentos: 5,
  quantidadePessoas: 0,
  mudarCor: function (cor) {
    if (typeof(cor) !== 'string'){
      return 'Valor informado não é uma cor';
    } else {
      this.cor = cor;
      return `Cor alterado para ${this.cor}`;
    }
  }
};
```

Crie um método chamado `obterCor`, que retorne a cor do carro.

```
const carro = {
  marca: 'Volkswagen',
  modelo: 'Golf',
  placa: 'XXXXXXX',
  ano: 2020,
  cor: 'Azul',
  quantasPortas: 4,
  assentos: 5,
  quantidadePessoas: 0,
  mudarCor: function (cor) {
    if (typeof(cor) !== 'string'){
      return 'Valor informado não é uma cor';
    } else {
      this.cor = cor;
      return `Cor alterado para ${this.cor}`;
    }
  },
  obterCor: function () {
    return this.cor;
  }
};
```

Crie um método chamado `obterModelo` que retorne o modelo do carro.

```
const carro = {
  marca: 'Volkswagen',
  modelo: 'Golf',
  placa: 'XXXXXXX',
  ano: 2020,
  cor: 'Azul',
  quantasPortas: 4,
  assentos: 5,
  quantidadePessoas: 0,
  mudarCor: function (cor) {
    if (typeof(cor) !== 'string'){
      return 'Valor informado não é uma cor';
    } else {
      this.cor = cor;
      return `Cor alterado para ${this.cor}`;
    }
  },
  obterCor: function () {
    return this.cor;
  },
  obterModelo: function () {
    return this.modelo;
  },
};
```

Crie um método chamado `obterMarca` que retorne a marca do carro.

```
const carro = {
  marca: 'Volkswagen',
  modelo: 'Golf',
  placa: 'XXXXXXX',
  ano: 2020,
  cor: 'Azul',
  quantasPortas: 4,
  assentos: 5,
  quantidadePessoas: 0,
  mudarCor: function (cor) {
    if (typeof(cor) !== 'string'){
      return 'Valor informado não é uma cor';
    } else {
      this.cor = cor;
      return `Cor alterado para ${this.cor}`;
    }
  },
  obterCor: function () {
    return this.cor;
  },
  obterModelo: function () {
    return this.modelo;
  },
  obterMarca: function () {
    return this.marca;
  },
};
```

Crie um método chamado `obterMarcaModelo`, que retorne:
"Esse carro é um [MARCA] [MODELO]"
Para retornar os valores de marca e modelo, utilize os métodos criados.

```
const carro = {
  marca: 'Volkswagen',
  modelo: 'Golf',
  placa: 'XXXXXXX',
  ano: 2020,
  cor: 'Azul',
  quantasPortas: 4,
  assentos: 5,
  quantidadePessoas: 0,
  mudarCor: function (cor) {
    if (typeof(cor) !== 'string'){
      return 'Valor informado não é uma cor';
    } else {
      this.cor = cor;
      return `Cor alterado para ${this.cor}`;
    }
  },
  obterCor: function () {
    return this.cor;
  },
  obterModelo: function () {
    return this.modelo;
  },
  obterMarca: function () {
    return this.marca;
  },
  obterMarcaModelo: function () {
    return `Esse carro é um ${this.obterMarca()} ${this.obterModelo()}`;
  },
};
```

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

```
const carro = {
  marca: 'Volkswagen',
  modelo: 'Golf',
  placa: 'XXXXXXX',
  ano: 2020,
  cor: 'Azul',
  quantasPortas: 4,
  assentos: 5,
  quantidadePessoas: 0,
  mudarCor: function (cor) {
    if (typeof(cor) !== 'string'){
      return 'Valor informado não é uma cor';
    } else {
      this.cor = cor;
      return `Cor alterado para ${this.cor}`;
    }
  },
  obterCor: function () {
    return this.cor;
  },
  obterModelo: function () {
    return this.modelo;
  },
  obterMarca: function () {
    return this.marca;
  },
  obterMarcaModelo: function () {
    return `Esse carro é um ${this.obterMarca()} ${this.obterModelo()}`;
  },
  adicionarPessoas: function (qtd) {
    if(this.quantidadePessoas === this.assentos ) {
      return 'O carro já está lotado!';
    } else {
      if(qtd > this.assentos || (this.quantidadePessoas + qtd) > this.assentos){
        assentosLivres = this.assentos - this.quantidadePessoas;
        return `Só cabem mais ${assentosLivres} pessoa${assentosLivres === 1 ? '' : 's'}`
      }
      
      this.quantidadePessoas = this.quantidadePessoas + qtd;
      
      return `já temos ${this.quantidadePessoas} pessoas no carro!`;
    }
  }
};
```

Agora vamos verificar algumas informações do carro. Para as respostas abaixo,
utilize sempre o formato de invocação do método (ou chamada da propriedade),
adicionando comentários _inline_ ao lado com o valor retornado, se o método
retornar algum valor.

Qual a cor atual do carro?

`carro.obterCor(); //'Azul'`

Mude a cor do carro para vermelho.

`carro.mudarCor('vermelho');`

E agora, qual a cor do carro?

`carro.cor; // 'vermelho'`

Mude a cor do carro para verde musgo.

`carro.mudarCor('verde musgo');`

E agora, qual a cor do carro?

`carro.cor; // 'verde musgo'`

Qual a marca e modelo do carro?

`carro.obterMarcaModelo(); // 'Esse carro é um Volkswagen Golf'`

Adicione 2 pessoas no carro.

`carro.adicionarPessoas(2); // 'já temos 2 pessoas no carro!'`

Adicione 4 pessoas no carro.

`carro.adicionarPessoas(4); // 'Só cabem mais 3 pessoas'`

Faça o carro encher.

`carro.adicionarPessoas(3); // 'já temos 5 pessoas no carro!'`

Tire 4 pessoas do carro.

`carro.quantidadePessoas = 1;`

Adicione 10 pessoas no carro.

`carro.adicionarPessoas(10); // 'Só cabem mais 4 pessoas'`

Quantas pessoas temos no carro?

`carro.quantidadePessoas; //1`