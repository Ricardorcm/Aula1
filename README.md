# Aula1
Unitins
class Stack:
    def __init__(self):
        self.items = []

    def push(self, item):
        self.items.append(item)

    def pop(self):
        if not self.is_empty():
            return self.items.pop()

    def peek(self):
        if not self.is_empty():
            return self.items[-1]

    def is_empty(self):
        return len(self.items) == 0

def reverse_string(input_string):
    stack = Stack()
    reversed_string = ""

    # Insere cada caractere da string na pilha
    for char in input_string:
        stack.push(char)

    # Remove cada caractere da pilha e adiciona ao resultado
    while not stack.is_empty():
        reversed_string += stack.pop()

    return reversed_string

# Função para testar a reversão de strings
def test_reverse_string():
    test_strings = ["hello", "world", "python", "stacks"]
    for test_string in test_strings:
        print(f"String original: {test_string}")
        print(f"String invertida: {reverse_string(test_string)}")
        print()

# Testando a função de reversão de strings
test_reverse_string()
