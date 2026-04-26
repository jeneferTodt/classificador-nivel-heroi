# 🧙‍♂️ Escrevendo as Classes de um Jogo

Projeto desenvolvido como parte dos desafios da DIO, com foco em **Programação Orientada a Objetos (POO)** utilizando JavaScript.

---

## 🎯 Objetivo

Criar uma classe que represente um herói de uma aventura, contendo:

- Nome  
- Idade  
- Tipo (guerreiro, mago, monge, ninja)  

Além disso, implementar um método que simule um ataque, exibindo uma mensagem personalizada conforme o tipo do herói.

---

## 🛠 Tecnologias utilizadas

- JavaScript  

---

## 🧠 Lógica aplicada

Este projeto utiliza:

- Variáveis  
- Operadores  
- Estruturas condicionais (if / else)  
- Funções  
- Classes e Objetos (POO)  

---

## ⚙️ Como funciona

1. Um herói é criado com:
   - Nome  
   - Idade  
   - Tipo  

2. O método de ataque é executado  

3. O sistema exibe uma mensagem baseada no tipo do herói  

---

## 📊 Tipos de ataque

| Tipo | Ataque |
|------|--------|
| mago | magia |
| guerreiro | espada |
| monge | artes marciais |
| ninja | shuriken |

---

## 📌 Exemplo de saída

mago atacou usando magia  
guerreiro atacou usando espada  

---

## ⚠️ Observações

- O tipo do herói define diretamente o tipo de ataque  
- Caso o tipo não seja reconhecido, pode ser tratado como ataque desconhecido

---

## Código

```
class Heroi {
    constructor(nome, idade, tipo) {
        this.nome = nome;
        this.idade = idade;
        this.tipo = tipo;
    }

    atacar() {
        let ataque = "";

        if (this.tipo === "mago") {
            ataque = "magia";
        } else if (this.tipo === "guerreiro") {
            ataque = "espada";
        } else if (this.tipo === "monge") {
            ataque = "artes marciais";
        } else if (this.tipo === "ninja") {
            ataque = "shuriken";
        } else {
            ataque = "ataque desconhecido";
        }

        console.log(`O ${this.tipo} atacou usando ${ataque}`);
    }
}

// Criando heróis
let heroi1 = new Heroi("Arthas", 30, "guerreiro");
let heroi2 = new Heroi("Merlin", 150, "mago");

// Executando ataque
heroi1.atacar();
heroi2.atacar();

```


