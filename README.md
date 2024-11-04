# Validador de CPF

Este é um script em Python que realiza a validação de um número de CPF (Cadastro de Pessoa Física) brasileiro, aplicando a fórmula padrão para verificar a validade dos dígitos verificadores no console (prompt de comando)

## Como Funciona

O CPF é composto de 11 dígitos, sendo que os dois últimos são os dígitos verificadores. O script calcula esses dígitos e os compara com os dígitos fornecidos para determinar se o CPF é válido.

O código:
1. Solicita ao usuário um CPF com 11 dígitos, apenas números.
2. Verifica se o CPF inserido é válido ou inválido.

## Regras de Validação

### Cálculo do Primeiro Dígito Verificador

1. Utiliza os primeiros 9 dígitos do CPF.
2. Multiplica cada dígito por uma sequência decrescente de 10 a 2.
3. Soma todos os resultados.
4. Multiplica a soma por 10 e tira o módulo 11.
5. Se o resultado for maior que 9, o dígito verificador é 0; caso contrário, é o resultado obtido.

### Cálculo do Segundo Dígito Verificador

1. Usa os primeiros 10 dígitos do CPF, incluindo o primeiro dígito verificador.
2. Multiplica cada dígito por uma sequência decrescente de 11 a 2.
3. Soma todos os resultados.
4. Multiplica a soma por 10 e tira o módulo 11.
5. Se o resultado for maior que 9, o dígito verificador é 0; caso contrário, é o resultado obtido.

### Validação Final

Compara o CPF digitado com o CPF calculado para confirmar sua validade.

## Exemplo de Uso
Ao executar, o programa solicitará a entrada do CPF e mostrará passo a passo os cálculos e o resultado final, indicando se o CPF é VÁLIDO ou INVÁLIDO.

Estrutura do Código
Entrada e validação inicial.
Cálculo do primeiro dígito verificador.
Cálculo do segundo dígito verificador.
Verificação e impressão do resultado.
Exemplo de Saída
plaintext
Copiar código
>>>>>>>>>>>>>> VALIDADOR DE |CPF| <<<<<<<<<<<<<<

Digite seu CPF (Apenas números e com 11 digitos): 12345678909
Total da SOMA é: [210]
Cáculo do primeiro Dígito é: 1

Total da SOMA é: [255]
Cáculo do segundo Dígito é: 9

===========================
| CPF | Digitado é VÁLIDO |
===========================
## Requisitos
### Python 3.x
### Notas
Este validador é baseado em um algoritmo básico para ilustrar a lógica de validação de CPF e não inclui validações avançadas.