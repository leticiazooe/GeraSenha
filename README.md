# Gerador de Senhas

> Aplicação desktop em Python/Tkinter para gerar senhas aleatórias de 12 a 18 caracteres e copiá-las para a área de transferência.

## Sobre o projeto

Este repositório contém um utilitário desktop simples para criação de senhas com combinação obrigatória de letras maiúsculas, letras minúsculas, números e caracteres especiais.

A interface permite escolher o tamanho da senha e gera um novo valor que é exibido na tela e copiado automaticamente para a área de transferência.

## Funcionalidades identificadas

- interface gráfica com Tkinter;
- seleção de tamanho entre 12 e 18 caracteres;
- geração aleatória de senha;
- exigência de ao menos uma letra minúscula;
- exigência de ao menos uma letra maiúscula;
- exigência de ao menos um número;
- exigência de ao menos um caractere especial;
- exibição da senha gerada;
- cópia automática para a área de transferência após a geração;
- botão dedicado para copiar novamente a senha;
- confirmação visual após a cópia.

## Tecnologias

- Python
- Tkinter
- `random`
- `string`

O projeto utiliza apenas módulos da biblioteca padrão do Python.

## Estrutura

```text
GeraSenha/
├── gerador-de-senhas
└── README.md
```

## Como executar

Requisito: Python 3 com suporte a Tkinter.

Clone o repositório:

```bash
git clone https://github.com/leticiazooe/GeraSenha.git
cd GeraSenha
```

Execute o arquivo principal:

```bash
python gerador-de-senhas
```

## Como usar

1. escolha uma das opções de tamanho, entre 12 e 18 caracteres;
2. clique em **Gerar Senha**;
3. a senha será criada, exibida e copiada para a área de transferência;
4. use **Copiar Senha** quando quiser copiá-la novamente.

## Observação de segurança

O código utiliza o módulo `random` da biblioteca padrão. Ele é adequado para este projeto como utilitário demonstrativo, mas **não é um gerador criptograficamente seguro**. Para geração de credenciais reais de alta criticidade, uma evolução recomendada é utilizar o módulo `secrets` do Python.

A aplicação não persiste as senhas em arquivo ou banco de dados, mas o valor gerado é colocado na área de transferência do sistema operacional.

## Possíveis evoluções

- utilizar `secrets` para geração criptograficamente segura;
- permitir informar o tamanho livremente;
- permitir escolher quais grupos de caracteres serão utilizados;
- adicionar indicador de força da senha;
- adicionar opção para limpar automaticamente a área de transferência após um intervalo.

## Autoria

Desenvolvido por **Letícia Vitória**.

GitHub: **@leticiazooe**
