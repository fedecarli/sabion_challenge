# SABION_CHALLENGE

## Desafio Sabion

### O Problema:

Em uma empresa de locação de carros recém inaugurada, para cada locação é atribuído um ID único (um inteiro positivo) em uma matriz. Quando o carro é devolvido o ID único é novamente adicionado ao mesmo array.
No final do primeiro mês, ao ser feita a contagem dos carros, de 100 apenas 99 estavam no pátio. Para rastrear esse carro que não retornou ao pátio, precisamos encontrar o código de entrega dele. 

Dado o array de IDs, que contém muitos inteiros duplicados e um inteiro único, encontre o inteiro único.

### Resolução

Chamei a função **myFunction** passando como parâmetro a lista de números de controle. 
Ordenei a lista recebida.
Depois verifiquei cada elemento da lista ordenada se ele era igual ao seu sucessor, caso fosse igual ambos eram excluídos.

```js
function myFunction(list) {
	var arr = list;
	var sorted_arr = arr.slice().sort();
	console.log(sorted_arr);
	var results = [];
	for (var i = 0; i < sorted_arr.length - 1; i++) {
		if (sorted_arr[i + 1] == sorted_arr[i]) {
			delete sorted_arr[i];
			delete sorted_arr[i + 1];
		}
	}
	console.log(sorted_arr);
	document.getElementById('demo').innerHTML = sorted_arr;
}
```
