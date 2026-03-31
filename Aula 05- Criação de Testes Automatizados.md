# Aula 05: Criação de Testes Automatizados

O objetivo desta aula foi comparar a eficácia de um prompt vago contra um prompt técnico e específico para a geração de código de teste.

## 1. Implementação do Teste Unitário

**Prompt Refinado:** "Crie um teste unitário em Python usando a biblioteca unittest para verificar se a função calcular_media(lista) retorna corretamente a média dos valores. Inclua casos de teste para lista vazia e lista com valores negativos."

### Código Gerado:
```python
import unittest

def calcular_media(lista):
    if not lista:
        return 0
    return sum(lista) / len(lista)

class TestCalculoMedia(unittest.TestCase):
    
    def test_media_padrao(self):
        self.assertEqual(calcular_media([10, 20, 30]), 20)

    def test_lista_vazia(self):
        # Verifica se o código lida com divisões por zero ou listas vazias
        self.assertEqual(calcular_media([]), 0)

    def test_valores_negativos(self):
        self.assertEqual(calcular_media([-10, -20]), -15)

if __name__ == '__main__':
    unittest.main()
