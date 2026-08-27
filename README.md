# 📚 Study Flow

**Plataforma de E-commerce B2C de Cursos e Conteúdos Digitais**

> Projeto acadêmico desenvolvido para a disciplina de **Gestão e Qualidade de Software** — Centro Universitário UNA.

![Status](https://img.shields.io/badge/status-especifica%C3%A7%C3%A3o-yellow)
![Licença](https://img.shields.io/badge/Licença-MIT-blue?style=for-the-badge)

---

## 📖 Sobre o projeto

O **Study Flow** é uma plataforma de comércio eletrônico B2C voltada à comercialização de cursos e conteúdos digitais. A solução permite que clientes se cadastrem, naveguem pelo catálogo, comprem cursos, acompanhem seus pedidos e acessem os conteúdos adquiridos. Instrutores gerenciam cursos e materiais, enquanto administradores controlam publicação, usuários, relatórios e configurações.

### 🎯 Objetivo

Disponibilizar uma experiência segura e confiável de compra e consumo de cursos digitais, integrando **catálogo, checkout, pagamento, matrícula, conteúdo e acompanhamento de progresso**.

### 👥 Público-alvo

- **Cliente/Aluno** — compra e consome cursos.
- **Instrutor** — cria e gerencia cursos e materiais.
- **Administrador** — governa a plataforma (aprovação, usuários, relatórios).

---

## 🗂️ Estrutura do repositório

| Arquivo/Pasta | Finalidade |
|---|---|
| `docs/Study_Flow_Especificacao_QA.pdf` | Documento completo de especificação, requisitos, DER, diagrama de classes e plano de QA. |
| `docs/Apresentacao_Ecommerce_B2C_III.pptx` | Apresentação (slides) resumindo o projeto conforme roteiro da Atividade III. |
| `README.md` | Este arquivo — visão geral e guia de navegação do repositório. |


---

## ✅ Escopo funcional

- Cadastro, autenticação e perfil de usuário
- Catálogo e categorização de cursos
- Gestão de cursos e conteúdo (instrutor)
- Carrinho, checkout, pedidos e pagamentos
- Matrícula e controle de acesso ao conteúdo
- Progresso, certificados e avaliações
- Notificações
- Chatbot/FAQ e suporte
- Relatórios administrativos
- Segurança, disponibilidade, backup, logs e conformidade (LGPD/GDPR)

---

## 🧩 Requisitos

O projeto documenta **25 requisitos funcionais (RF01–RF25)** e **14 requisitos não funcionais (RNF01–RNF14)**, todos com critérios de aceitação verificáveis. Alguns destaques:

| ID | Requisito | Prioridade |
|---|---|---|
| RF01–RF04 | Cadastro, login, perfil e recuperação de senha | Alta |
| RF05–RF11 | Catálogo, gestão de cursos e conteúdo | Alta |
| RF12–RF16 | Carrinho, checkout, pagamento e pedido | Alta |
| RF17–RF20 | Matrícula, progresso e certificados | Alta |
| RF21–RF25 | Avaliações, notificações, relatórios e reembolso | Média |

Detalhes completos, critérios de aceitação e requisitos não funcionais estão no documento de especificação (`docs/Study_Flow_Especificacao_QA.pdf`).

---

## 🗃️ Modelagem de dados (DER)

Principais entidades: `Usuario`, `Curso`, `Categoria`, `Modulo`, `Conteudo`, `Carrinho`, `ItemCarrinho`, `Pedido`, `ItemPedido`, `Pagamento`, `Matricula` e `Progresso`.

O modelo conceitual completo (DER) está disponível no documento de especificação.

---

## 🏗️ Arquitetura

O projeto propõe uma arquitetura em camadas, separando regras de negócio de detalhes de infraestrutura:

| Camada | Responsabilidade | Exemplos |
|---|---|---|
| **Apresentação** | Telas, APIs e validação de entrada | Login, catálogo, carrinho, checkout |
| **Aplicação** | Orquestra casos de uso | FinalizarCompra, MatricularAluno, PublicarCurso |
| **Domínio** | Entidades e regras de negócio | Curso, Pedido, Pagamento, Matrícula, Progresso |
| **Infraestrutura** | Banco, gateways e serviços externos | Repository, gateway de pagamento, e-mail/SMS |

---

## 🌿 Estratégia de versionamento (Git)

| Branch | Finalidade |
|---|---|
| `main` | Versão estável — apenas código revisado e aprovado |
| `develop` | Integração de features concluídas e testadas |
| `feature/*` | Uma branch por nova funcionalidade |
| `fix/*` | Correções de defeitos |
| `hotfix/*` | Correções urgentes em produção |

**Convenção de commits:**
feat: adiciona carrinho de compras
fix: corrige cálculo do total do pedido
test: adiciona cenário de checkout
docs: atualiza matriz de requisitos
refactor: reorganiza serviço de pagamento


**Critérios mínimos para merge:**
- Pull Request associado a um requisito ou correção
- Build sem erros
- Testes automatizados aprovados
- Code Review por pelo menos 1 integrante
- Sem conflitos de merge e sem credenciais versionadas

---

## 🧪 Plano de Garantia da Qualidade (QA)

Estratégia de testes cobrindo unidade, integração, sistema, segurança, desempenho e usabilidade, com foco nos fluxos críticos: **autenticação, compra/pagamento e acesso ao conteúdo**.

| Cenário | Descrição |
|---|---|
| CT01 | Cadastro e login |
| CT02 | Compra e pagamento |
| CT03 | Bloqueio de conteúdo por pré-requisito |
| CT04 | Reprovação de curso pelo administrador |
| CT05 | Controle de acesso por perfil |
| CT06 | Cálculo do carrinho/total |

A rastreabilidade entre requisitos e cenários de teste está detalhada no documento de especificação.

---

## 👨‍💻 Equipe

- Erick Souza
- Geovane Santos
- Kauan de Andrade

**Disciplina:** Gestão e Qualidade de Software — Centro Universitário UNA
