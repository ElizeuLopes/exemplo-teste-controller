
# Agendador de Notificações

Esse projeto foi desenvolvido para um desafio técnico visando apresentar habilidades de desenvolvedor java backend e tem como escopo o cadastro de notificações para posterior envio.

## Rodando localmente

Clone o projeto

```bash
  git clone https://link-para-o-projeto
```

Entre no diretório do projeto

```bash
  docker-compose up --build
```


## Documentação da API

#### Cadastra notificações pendentes

```http
  POST /agendamento
```

| Body   | Tipo       | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `emailDestinatario` | `string` | **Obrigatório**. Email do destinatário da notificação |
| `telefoneDestinatario` | `string` | **Obrigatório**. Telefone do destinatário da notificação |
| `mensagem` | `string` | **Obrigatório**. Mensagem da notificação |
| `dataHoraEvento` | `LocalDateTime` | **Obrigatório**. Data hora do evento no formado dd-MM-yyyy HH:mm:ss |

#### Retorna uma notificação por id

```http
  GET /agendamento/${id}
```

| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `id`      | `string` | **Obrigatório**. O ID do item que você quer buscar |

#### Cancela uma notificação por id

```http
  DELETE /agendamento/${id}
```

| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `id`      | `string` | **Obrigatório**. O ID do item que você quer cancelar |


## Rodando os testes

Para rodar os testes, rode o seguinte comando

```bash
  mvn test
```




Título do PR (Pull Request)

✨ [FEATURE] Adiciona componente de carrinho de compras
Descrição

Objetivo:
Adiciona um novo componente de carrinho de compras responsivo com funcionalidades básicas.

Alterações realizadas:

    ✅ Criado componente ShoppingCart.vue

    ✅ Implementada lógica para adicionar/remover itens

    ✅ Adicionada animação de transição

    ✅ Criados testes unitários básicos

Tarefas relacionadas:
Resolve #123 (Issue: "Carrinho de compras não existe")
Screenshots/Preview
Desktop	Mobile
Desktop	Mobile
Checklist de revisão

    O código segue nossos padrões de estilo

    Os testes passam localmente

    Documentação atualizada (se aplicável)

    Responsividade testada em múltiplos dispositivos

Observações adicionais

Este PR depende da merge da branch feature/product-api para funcionar corretamente.
Sugiro revisar primeiro os arquivos principais:

    src/components/ShoppingCart.vue

    tests/unit/ShoppingCart.spec.js
