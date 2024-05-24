# Operações de Conjuntos com Polimorfismo em Python

Este projeto demonstra como realizar operações comuns de teoria dos conjuntos (interseção, união, diferença e negação da interseção) em Python usando o conceito de polimorfismo.

## Visão Geral

O código consiste em uma classe base abstrata `Conjunto` e duas subclasses (`ConjuntoLista` e `ConjuntoDict`) que implementam essa classe base. Além disso, há uma função externa `aplicar_operacao` que atua como um filtro, aplicando as operações desejadas em diferentes instâncias de conjuntos.

## Funcionalidades

- **Interseção**: Retorna os elementos comuns a dois conjuntos.
- **União**: Retorna todos os elementos que estão em pelo menos um dos conjuntos.
- **Diferença**: Retorna os elementos que estão em um conjunto, mas não no outro.
- **Negação da Interseção**: Retorna os elementos que estão em um conjunto ou no outro, mas não em ambos.

## Detalhes de Implementação

- A classe `Conjunto` define métodos abstratos para as operações de conjuntos.
- As subclasses `ConjuntoLista` e `ConjuntoDict` implementam esses métodos de acordo com suas representações de conjuntos.
- A função `aplicar_operacao` recebe dois conjuntos e o nome da operação a ser realizada, aplicando a operação correspondente usando polimorfismo.

## Exemplos de Uso

```python
conj_lista1 = ConjuntoLista([1, 2, 3, 4])
conj_lista2 = ConjuntoLista([3, 4, 5, 6])

conj_dict1 = ConjuntoDict({1: True, 2: True, 3: True, 4: True})
conj_dict2 = ConjuntoDict({3: True, 4: True, 5: True, 6: True})

# Aplicando operações usando a função filtro
print("Interseção (Lista):", aplicar_operacao(conj_lista1, conj_lista2, 'intersecao'))
print("União (Lista):", aplicar_operacao(conj_lista1, conj_lista2, 'uniao'))
print("Diferença (Lista):", aplicar_operacao(conj_lista1, conj_lista2, 'diferenca'))
print("Negação da Interseção (Lista):", aplicar_operacao(conj_lista1, conj_lista2, 'negacao_intersecao'))

print("Interseção (Dict):", aplicar_operacao(conj_dict1, conj_dict2, 'intersecao'))
print("União (Dict):", aplicar_operacao(conj_dict1, conj_dict2, 'uniao'))
print("Diferença (Dict):", aplicar_operacao(conj_dict1, conj_dict2, 'diferenca'))
print("Negação da Interseção (Dict):", aplicar_operacao(conj_dict1, conj_dict2, 'negacao_intersecao'))
```
