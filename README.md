# Insight Places Database

Este repositório contém o script SQL para criação do banco de dados **Insight Places**, desenvolvido em MySQL.  
O objetivo é estruturar informações de hospedagens, clientes e proprietários de forma organizada e relacional.

---

## 🗂️ Estrutura do Banco de Dados

### Tabelas principais
- 👤 **proprietarios** → dados dos donos das hospedagens  
- 👥 **clientes** → informações dos clientes  
- 🏠 **enderecos** → endereços completos das hospedagens  
- 🏨 **hospedagens** → tipos de hospedagem e vínculo com endereço e proprietário  
- 📅 **alugueis** → registros de aluguel, datas e valores  
- ⭐ **avaliacoes** → notas e comentários dos clientes  

---

## 🔗 Relacionamentos entre tabelas
PROPRIETARIOS ──< HOSPEDAGENS ──< ALUGUEIS
│                 │              │
│                 │              └── CLIENTES
│                 └──< AVALIACOES ── CLIENTES
│
ENDERECOS ──< HOSPEDAGENS

- Cada **hospedagem** pertence a um **proprietário** e a um **endereço**.  
- Cada **aluguel** conecta um **cliente** a uma **hospedagem**.  
- Cada **avaliação** é feita por um **cliente** sobre uma **hospedagem**.  

---

## 🚀 Como rodar o script

### ▶️ No MySQL Workbench
1. Abra o Workbench.  
2. Vá em **File → Open SQL Script**.  
3. Selecione `insight_places.sql`.  
4. Clique no raio ⚡ para executar.  
5. Confirme com:
   ```sql
   SHOW TABLES;
   ▶️ No VS Code com SQLTools
Instale a extensão SQLTools e o driver MySQL/MariaDB.

Configure a conexão (host: localhost, port: 3306, user: root).

Abra insight_places.sql.

Pressione Ctrl + A → clique direito → Run Query.

Confirme com:
SHOW TABLES;
👨‍💻 Autor
Projeto desenvolvido por Valdemir (VGNelo) - Alura/Oracle OCI - como parte dos estudos de MySQL.

