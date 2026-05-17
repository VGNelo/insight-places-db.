# Insight Places Database

Este repositório contém o script SQL para criação do banco de dados **Insight Places**, desenvolvido em MySQL.  
O objetivo é estruturar as informações de hospedagens, clientes e proprietários de forma organizada e relacional.

---

##  Estrutura do Banco de Dados

### Tabelas principais
- **proprietarios** → dados dos donos das hospedagens (nome, CPF/CNPJ, contato)  
- **clientes** → informações dos clientes (nome, CPF, contato)  
- **enderecos** → endereços completos das hospedagens (rua, número, bairro, cidade, estado, CEP)  
- **hospedagens** → tipos de hospedagem, vínculo com endereço e proprietário, status ativo/inativo  
- **alugueis** → registros de aluguel, datas de início e fim, preço total, vínculo com cliente e hospedagem  
- **avaliacoes** → notas e comentários dos clientes sobre as hospedagens  

---

## Relacionamentos
- Cada **hospedagem** pertence a um **proprietário** e a um **endereço**.  
- Cada **aluguel** conecta um **cliente** a uma **hospedagem**.  
- Cada **avaliação** é feita por um **cliente** sobre uma **hospedagem**.  

---

## Como usar
1. Abra o MySQL Workbench ou VS Code com SQLTools.  
2. Crie o banco de dados:
   ```sql
   CREATE DATABASE insight_places;
   USE insight_places;
