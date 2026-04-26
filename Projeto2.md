# 🧮 Calculadora de Partidas Rankeadas

Projeto desenvolvido como parte dos desafios da DIO, com foco em **lógica de programação** utilizando JavaScript.

---

## 🎯 Objetivo

Criar um sistema que:

- Calcula o **saldo de vitórias** de um jogador  
- Define seu **nível ranqueado** com base na quantidade de vitórias  

---

## 🚀 Demonstração

https://jenefertodt.github.io/classificador-nivel-heroi/

---

## 🛠 Tecnologias utilizadas

- JavaScript  
- HTML (versão interativa via navegador)  

---

## 🧠 Lógica aplicada

Este projeto utiliza:

- Variáveis  
- Operadores matemáticos  
- Estruturas condicionais (`if / else`)  
- Funções  
- Validação de dados  

---

## ⚙️ Como funciona

1. O usuário informa:
   - Número de vitórias  
   - Número de derrotas  

2. O sistema calcula o saldo de vitórias  

3. O jogador é classificado conforme a quantidade de vitórias  

---

## 📊 Classificação de níveis

| Vitórias | Nível |
|----------|------|
| ≤ 10     | Ferro |
| 11 - 20  | Bronze |
| 21 - 50  | Prata |
| 51 - 80  | Ouro |
| 81 - 90  | Diamante |
| 91 - 100 | Lendário |
| ≥ 101    | Imortal |

---

## 🖥 Versão interativa

O projeto possui uma versão com entrada de dados via `prompt()` no navegador.

---

## 📌 Exemplo de saída

O Herói tem de saldo de 55 está no nível de Ouro

---

## ⚠️ Observações

- Insira apenas valores numéricos válidos  
- Valores inválidos podem resultar em erro (`NaN`)  

---

## 👩‍💻 Código
```
<script>
function calcularRank(vitorias, derrotas) {
    let saldo = vitorias - derrotas;
    let nivel = "";

    if (vitorias <= 10) nivel = "Ferro";
    else if (vitorias <= 20) nivel = "Bronze";
    else if (vitorias <= 50) nivel = "Prata";
    else if (vitorias <= 80) nivel = "Ouro";
    else if (vitorias <= 90) nivel = "Diamante";
    else if (vitorias <= 100) nivel = "Lendário";
    else nivel = "Imortal";

    return { saldo, nivel };
}

let vitorias = parseInt(prompt("Digite o número de vitórias:"));
let derrotas = parseInt(prompt("Digite o número de derrotas:"));

if (isNaN(vitorias) || isNaN(derrotas)) {
    alert("Por favor, digite apenas números válidos!");
} else {
    let resultado = calcularRank(vitorias, derrotas);
    alert(`O Herói tem de saldo de ${resultado.saldo} está no nível de ${resultado.nivel}`);
}
</script>

```
