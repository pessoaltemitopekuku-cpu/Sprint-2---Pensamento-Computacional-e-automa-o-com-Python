# Solari - EV Charger Management SaaS 🚗⚡

Uma plataforma inovadora no modelo SaaS (Software as a Service) voltada para a gestão inteligente, monitoramento e compartilhamento de carregadores de veículos elétricos em ambientes corporativos e residenciais.

---

## 👥 Integrantes do Grupo

| Nome Completo | RM |
| :--- | :--- |
| **Carlos Eduardo Affonso** | 569676 |
| **Temitope Kuku da Silva Ogunbanjo** | 573772 |
| **Igor Massone Monteiro** | 573853 |
| **Gabriel O. G. F. dos Santos** | 573747 |
| **Gabrieli de Lima Pettena de Oliveira** | 569799 |

---

## 📝 Resumo do Projeto

O **Solari** nasceu para resolver o desafio da infraestrutura de recarga elétrica urbana através de uma simulação fluida e realista. A plataforma atua em duas vertentes principais:

1. **Prédios/Condomínios (Administração):** Uma área de gerenciamento onde os síndicos ou gestores prediais realizam o cadastro de novos pontos de recarga, monitoram a saúde dos carregadores e controlam as métricas financeiras.
2. **Usuários/Funcionários (Consumidores):** Uma interface intuitiva para que motoristas naveguem pelos carregadores disponíveis no seu respectivo bloco predial e iniciem sessões de recarga em tempo real.

### 🌟 O Grande Diferencial: "Clusters" de Condomínios
Ao contrário de soluções tradicionais isoladas, o Solari introduz o conceito de **Clusters**. Isso permite que um grupo de um ou mais prédios/empresas compartilhem a mesma rede de carregadores. Desse modo, funcionários ou moradores integrados ao mesmo cluster podem usufruir de pontos de recarga vizinhos de forma colaborativa, otimizando o uso do espaço e da energia disponível.

---

## 🚀 O que foi Desenvolvido

Para dar vida à proposta mantendo a agilidade, o projeto foi dividido estrategicamente em duas partes desacopladas:

* **Frontend (Protótipo Interativo):** Desenvolvido na plataforma **Lovable**, servindo como uma demonstração visual de alta fidelidade da experiência do usuário (UX), simulando telas de login customizadas por nível de acesso, dashboards analíticos, consumo em *Moedas Solari* e alertas de rede.
* **Backend (Arquitetura Sugerida):** Construído do zero em **Python** e hospedado de forma independente no **Render**. Ele serve como a "sugestão técnica de motorização real" para o sistema, demonstrando como os dados seriam tratados nativamente por uma API de mercado.

---

## 🔄 Fluxo da Plataforma (Passo a Passo)

O ecossistema Solari opera de forma integrada seguindo as seguintes etapas simples:

```text
[ Passo 1: Autenticação ]
       │
       ├──► Se Admin ──────► Dashboard de Métricas Globais e Rateio de Custos
       └──► Se Funcionário ──► Dashboard de Consumo e Monitoramento de Vagas
       │
[ Passo 2: Consulta de Status ]
       │
       └──► Sistema lista carregadores em tempo real (Disponível, Em Uso ou Offline)
       │
[ Passo 3: Ativação Assíncrona ]
       │
       └──► Usuário seleciona vaga ativa e dispara comando "Iniciar Recarga"
       │
[ Passo 4: Processamento Analítico ]
       │
       └──► Backend Python/Pandas simula a alteração de status e calcula consumo e moedas
