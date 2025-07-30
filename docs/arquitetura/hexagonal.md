# Arquitetura Hexagonal (Ports and Adapters)

A Arquitetura Hexagonal, proposta por Alistair Cockburn, busca separar regras de negócio (core) de detalhes de infraestrutura (como banco, API, mensageria, etc).

## 📌 Conceitos

- **Domínio (core)**: onde ficam os casos de uso e entidades.
- **Portas (ports)**: interfaces que descrevem o que o domínio precisa ou oferece.
- **Adaptadores (adapters)**: implementações das portas — como controladores REST, repositórios, etc.

## 🧱 Exemplo de Estrutura

```
src/
├── application/
│   └── usecases/
├── domain/
│   ├── model/
│   └── ports/
├── infrastructure/
│   ├── persistence/
│   ├── rest/
│   └── messaging/
```

## 📎 Benefícios

- Testabilidade: facilita testes de unidade do core.
- Independência tecnológica.
- Facilidade de manutenção e evolução.

## 🔗 Projetos que usam

- [pedido-service](https://github.com/seuusuario/pedido-service): Implementa portas para Kafka e REST.
