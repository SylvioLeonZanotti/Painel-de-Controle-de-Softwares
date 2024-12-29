# Painel de Controle de Softwares

Este projeto é um **Painel de Controle Web** desenvolvido para gerenciar softwares clientes de maneira centralizada, permitindo controle sobre licenças, status de ativação e funcionalidade offline. O painel é integrado a um software cliente que interage diretamente com ele para validar seu status, operar no modo offline em casos de indisponibilidade do painel e registrar dados essenciais.

---

## Índice
1. [Funcionalidades Principais](#funcionalidades-principais)
2. [Como Funciona?](#como-funciona)
3. [Por Que Este Projeto é Bom?](#por-que-este-projeto-é-bom)
4. [Tecnologias Utilizadas](#tecnologias-utilizadas)
5. [Próxima implementação](#próxima-implementação)
6. [Capturas de Tela](#capturas-de-tela)

---

## Funcionalidades Principais

### Registro e Aprovação de Softwares
- **Registro Automático:** O painel registra automaticamente os softwares clientes ao iniciarem pela primeira vez.
- **Aprovação Manual:** Softwares pendentes precisam de aprovação manual antes de serem ativados.

### Autenticação e Controle de Licenças
- **Validação no Painel:** Verificação do status de ativação, data de expiração e validade da licença diretamente no painel.
- **Gestão de Licenças:** Controle sobre datas de expiração e renovação de licenças.

### Modo Offline
- O software cliente pode funcionar no modo offline por até **5 minutos (300 segundos)** utilizando um token local.
- Durante o modo offline, o cliente tenta reconectar-se ao painel a cada **10 segundos**.
- Caso não consiga reconectar após o tempo limite, o software é desligado automaticamente.

### Organização de Softwares
- **Softwares Aprovados:** Aparecem na aba principal do painel (**Menu**).
- **Softwares Pendentes:** Listados separadamente, aguardando aprovação manual.
- **Softwares Apagados:** Movidos para a aba **"Apagados"**, mantendo o histórico.

### Painel Web Intuitivo
- Desenvolvido com uma interface **moderna e responsiva**.
- Exibe **métricas detalhadas**, como dias restantes para expiração e status de cada software.

---

## Como Funciona?

1. O painel web é executado para **monitorar e gerenciar os softwares clientes**.
2. Os softwares clientes:
   - **Conectam-se ao painel** para verificar seus status e receber atualizações.
   - **Entram no modo offline** em caso de indisponibilidade do painel, tentando reconectar periodicamente.
3. O software cliente é desligado automaticamente se não conseguir reconectar ao painel após 300 segundos consecutivos.

---

## Por Que Este Projeto é Bom?

- **Centralização do Controle:**
  O painel fornece uma visão unificada e organizada de todos os softwares gerenciados, permitindo ações rápidas como aprovação, ativação e desativação.

- **Funcionalidade Offline Resiliente:**
  O modo offline garante que o software cliente continue funcionando mesmo em casos de indisponibilidade temporária do painel.

- **Segurança com Tokens:**
  Tokens temporários protegem o funcionamento do software cliente e evitam fraudes em licenças.

- **Flexibilidade:**
  Ideal para ambientes onde softwares precisam ser gerenciados remotamente, como em sistemas de automação industrial, ERP ou SaaS.

- **Escalável:**
  Pode ser facilmente adaptado para suportar novos recursos, como integração com sistemas de pagamento ou geração de relatórios detalhados.

---

## Tecnologias Utilizadas

### Backend
- **Python (Flask):** Framework leve e eficiente para o backend.
- **SQLAlchemy:** ORM para gerenciamento do banco de dados.

### Frontend
- **HTML, CSS, JavaScript:** Interface responsiva e moderna.

### Banco de Dados
- **SQLite:** Simples e eficiente para desenvolvimento inicial.
- **Compatível com PostgreSQL/MySQL:** Facilmente expansível para ambientes de produção.

## Próxima implementação
- Forma de pagamento para renovação de licenças através da página do cliente podendo escolher entre PIX, boleto ou cartão de crédito.

## Screenshots iniciais
![image](https://github.com/user-attachments/assets/e1fd9781-b349-458b-bf59-7ce8a2f7e4d8)

## Área do cliente
![image](https://github.com/user-attachments/assets/ce75ea11-219d-4652-82d7-06691dcc4777)


