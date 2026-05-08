# 🛠️ Sistema de Banco de Dados: Oficina Mecânica

Este projeto consiste na implementação de um banco de dados relacional para o gerenciamento operacional de uma **Oficina Mecânica**. O sistema permite o controle total desde o cadastro de clientes e seus veículos até a emissão de ordens de serviço e análise de produtividade da equipe.

Projeto desenvolvido como atividade prática para a disciplina de **Programação de Banco de Dados** (Anhanguera Marte), sob orientação do **Prof. Nicolas Vogiantzis**.

---

## 📌 Estrutura do Projeto

O banco de dados foi modelado para garantir a integridade referencial e evitar a duplicidade de informações. A estrutura conta com as seguintes tabelas:

*   **`clientes`**: Armazena dados dos proprietários.
*   **`veiculos`**: Registro dos automóveis vinculados aos clientes.
*   **`mecanicos`**: Cadastro de profissionais e suas especialidades.
*   **`servicos`**: Tabela de referência com descrições e preços base.
*   **`ordem_servico`**: Documento principal que une o veículo, o mecânico e o status do reparo.
*   **`itens_servicos`**: Tabela associativa que permite inserir vários serviços em uma única Ordem de Serviço.

---

## 🚀 Como Utilizar

1.  **Criação do Schema:** Execute a primeira parte do script para criar o banco de dados `OficinaMecanicaFellipe` e todas as tabelas.
2.  **População de Dados:** O script contém comandos `INSERT` para 50 registros em cada tabela principal, permitindo testar o banco com um volume real de dados.
3.  **Consultas (Queries):** Utilize os scripts de desafio localizados ao final do arquivo para gerar relatórios.

---

## 📊 Relatórios e Desafios (Queries de Negócio)

Abaixo estão os desafios de negócio resolvidos através de consultas SQL avançadas presentes no projeto:

### 1. Relatório de Frota por Cliente
Lista todos os clientes e seus veículos, garantindo que mesmo clientes sem veículos cadastrados apareçam no relatório.
> **Técnica:** `LEFT JOIN`.

### 2. Produtividade dos Mecânicos
Exibe o nome de cada mecânico e a quantidade total de Ordens de Serviço vinculadas a eles.
> **Técnica:** `COUNT` e `GROUP BY`.

### 3. Faturamento por Cidade
Calcula o valor total gerado em ordens de serviço por clientes residentes na cidade de **São Paulo**.
> **Técnica:** `JOIN` múltiplo e `SUM`.

### 4. Detalhamento de Serviços em Aberto
Relaciona o modelo do veículo, o nome do mecânico e a descrição do serviço para todas as ordens com status 'Aberto'.
> **Técnica:** Filtro `WHERE` com `JOIN` entre 4 tabelas.

### 5. Clientes VIP (Análise de Gasto)
Lista os nomes dos clientes que gastaram acima da média global da oficina.
> **Técnica:** Subconsulta (`Subquery`) e cláusula `HAVING`.

---

## 🛠️ Tecnologias Utilizadas

*   **Linguagem SQL:** (DDL e DML)
*   **DB Engine:** MySQL / MariaDB (ou qualquer banco relacional compatível).

---

## 👨‍💻 Autor

**Fellipe**  
*Estudante de Tecnologia – Anhanguera Marte*
*Programação em Banco de Dados - Nicolas Vogiatzis*
