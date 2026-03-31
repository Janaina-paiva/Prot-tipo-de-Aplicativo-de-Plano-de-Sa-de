# Atividade Prática: Desbloqueando o Raciocínio (CoT)

## Simulação de Chat (Etapa 3)
**Prompt:** Qual é a terceira letra da quinta palavra da frase "O rato roeu a roupa do Rei de Roma"?

**Raciocínio Passo a Passo (CoT):**
1. Frase: "O rato roeu a roupa do Rei de Roma"
2. Lista de palavras: [1:O], [2:rato], [3:roeu], [4:a], [5:roupa]...
3. Quinta palavra selecionada: "roupa"
4. Decomposição de "roupa": R-O-U-P-A
5. Terceira letra: "U"

**Resultado:** U

---

## Conclusão: Tokens vs. Precisão
A IA muitas vezes erra contagens simples porque ela não "lê" letras, mas sim **tokens** (pedaços de palavras). A palavra "roupa" pode ser um único token para o modelo, o que torna difícil para ele "enxergar" o que está dentro dela sem ajuda.

Ao utilizarmos o **Chain-of-Thought (CoT)**, forçamos a IA a transformar esse token em uma sequência de caracteres individuais no rascunho. Isso aumenta a precisão porque cada etapa do raciocínio gera um novo contexto visual para o modelo, permitindo que ele corrija a própria percepção e chegue à resposta exata.
