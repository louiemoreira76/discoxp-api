# 🎮 DiscoXP API – Backend do E‑commerce de Games

<div align="center">

[![GitHub stars](https://img.shields.io/github/stars/louiemoreira76/discoxp-api?style=for-the-badge)](https://github.com/louiemoreira76/discoxp-api/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/louiemoreira76/discoxp-api?style=for-the-badge)](https://github.com/louiemoreira76/discoxp-api/network)
[![GitHub license](https://img.shields.io/github/license/louiemoreira76/discoxp-api?style=for-the-badge)](LICENSE)

**API RESTful para gerenciar produtos, pedidos, usuários e endereços de uma loja virtual de jogos.**

</div>

## 📖 Sobre o projeto

A `discoxp-api` é o backend de uma plataforma de e‑commerce focada na venda de jogos.  
Ela fornece endpoints seguros para:

- Cadastro e autenticação de usuários (clientes, estoquistas, administradores)
- CRUD de produtos com upload de imagens
- Gerenciamento de carrinho e pedidos
- Endereços de cobrança e entrega
- Controle de estoque
- Validações robustas (CPF, e‑mail, senha, etc.)

O projeto foi construído com **Spring Boot**, seguindo os princípios REST e utilizando boas práticas como DTOs, validação em camadas, tratamento global de exceções e testes de integração.

## ✨ Funcionalidades

### Para clientes
- Cadastro/atualização de perfil (dados pessoais, endereços)
- Visualização de produtos com filtros e avaliações
- Adicionar/remover produtos do carrinho
- Finalizar pedido com escolha de endereço e forma de pagamento
- Acompanhamento de pedidos

### Para estoquistas
- Gerenciamento de quantidades em estoque
- Visualização de produtos cadastrados

### Para administradores
- Cadastro/edição/remoção de produtos e imagens
- Gestão de usuários (clientes, estoquistas, admins)
- Visualização de todos os pedidos
- Upload de imagens para produtos

## 🛠️ Tecnologias

| Camada          | Tecnologia                                                                 |
|-----------------|----------------------------------------------------------------------------|
| Linguagem       | Java 17                                                                     |
| Framework       | Spring Boot 3 (Web, Data JPA, Security, Validation)                         |
| Banco de dados  | PostgreSQL (ou MySQL) – configurável via `application.yml`                  |
| Autenticação    | Spring Security                                    |
| Mapeamento      | Hibernate / JPA                                                             |
| Build           | Maven                                                                       |
| Testes          | JUnit 5, Mockito, Testcontainers, Selenium (para alguns testes end‑to‑end) |


## 🚀 Como rodar localmente

### Pré‑requisitos
- JDK 17+
- Maven 3.8+
- Mysql
- Git

## 📁 Project Structure

```
discoxp-api/
├── src/main/java/com/github/sintaxenervosa/discoxp/
│   ├── controller/      # Endpoints REST (Admin, Client, Order, Product, User...)
│   ├── dto/             # Objetos de transferência (request/response)
│   ├── exception/       # Exceções customizadas e handler global
│   ├── model/           # Entidades JPA (User, Product, Order, Address...)
│   ├── repository/      # Interfaces Spring Data JPA
│   ├── security/        # Configurações de segurança e JWT
│   ├── service/         # Regras de negócio
│   └── validations/     # Validadores específicos (CPF, e‑mail, produto, pedido...)
└── src/test/            # Testes unitários, de integração e Selenium
```
