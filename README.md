# Classificador de nível de Herói ⚔️✨

Programa em JavaScript desenvolvido e executado na **plataforma PlayCode.i.o** ▶️🖥️.
https://playcode.io/javascript-playground--019b81b9-21db-70fa-80ac-c3f3ec2ce894

---

## Objetivo 🎯
Armazenar o **nome** e a **quantidade de XP** de um herói e determinar o **nível** correspondente conforme faixas de XP definidas.

---

## Dados usados no desafio 🧾
- **Nome**: **Washinton Brito Miguel**  
- **XP**: **10.000**  
- **Nível resultante**: **Imortal** 🛡️

---

## Lógica implementada 🧭
1. **Modelagem**: variáveis `nome` (string) e `xp` (number).  
2. **Tabela de níveis**: array de objetos com `max` e `nivel` para facilitar manutenção.  
3. **Decisão**: percorremos a tabela com um `for` e selecionamos o primeiro nível cujo `max` é maior ou igual ao `xp`.  
4. **Caso padrão**: se `xp` for maior que todos os limites, o nível é **Radiante**.  
5. **Saída**: mensagem formatada com template string exibida no console.

---

## Código principal ✅

```javascript
// Dados do herói
const nome = "Washinton Brito Miguel";
const xp = 10000;

// Tabela de níveis (ordem crescente de XP)
const niveis = [
  { max: 1000, nivel: "Ferro" },
  { max: 2000, nivel: "Bronze" },
  { max: 5000, nivel: "Prata" },
  { max: 7000, nivel: "Ouro" },
  { max: 8000, nivel: "Platina" },
  { max: 9000, nivel: "Ascendente" },
  { max: 10000, nivel: "Imortal" }
];

// Determina o nível usando laço e decisão
let nivel = "";
for (let i = 0; i < niveis.length; i++) {
  if (xp <= niveis[i].max) {
    nivel = niveis[i].nivel;
    break;
  }
}

// Se não entrou em nenhum intervalo anterior, é Radiante
if (!nivel) nivel = "Radiante";

// Saída
console.log(`O Herói de nome ${nome} está no nível de ${nivel}`);

Créditos e ambiente de desenvolvimento 🏷️
Plataforma de execução: PlayCode.i.o ▶️🖥️

Linguagem: JavaScript

Autor do código: Washinton Brito Miguel (nome usado no desafio)
