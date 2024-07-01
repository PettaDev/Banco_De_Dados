
<div align="center">
  <h4>Banco de Dados</h4>
  <img src="Vel.png" width="70px" align="center">
</div>

## 💡 Projeto

O banco de dados `VEL` foi projetado para gerenciar as operações de uma plataforma de gestão para empresas de motos e restaurante. Este banco de dados cobre funcionalidades essenciais como: Associação das empresas com os planos, registro de empresa, entregador e coordenador, atribuição de pedidos e geração de comandas virtuais.

## 🔧 Tecnologias Utilizadas

- **BrModelo**: Utilizado para a criação dos modelos conceituais.
- **MySQL**: Utilizado para o gerenciamento de Banco de Dados Relacional.
- **SQL**: Linguagem utilizada para definir e manipular os dados no banco de dados.

## 🗃️ Estrutura do Banco de Dados

### 📊 Tb_Plano
Tabela para associar a empresa ao plano.

- **Colunas Principais**:
  - `Pk_id`
  - `nome`
  - `beneficio`

### 🏢 Tb_Empresa
Tabela para alocar a empresa.

- **Colunas Principais**:
  - `Pk_id_cnpj`
  - `email`
  - `senha`
  - `endereco`
  - `telefone`
  - `proprietario`
  - `Fk_id_plano`
  - `Fk_faturamento`
  - `Fk_cpf_coord`
  - `Fk_cpf`
  - `Fk_contrato`

### 👨‍💼 Tb_Coordenador
Tabela para alocar o coordenador.

- **Colunas Principais**:
  - `Pk_id_cpf`
  - `nome`
  - `telefone`
  - `email`
  - `senha`
  - `conta_bancaria`

### 🛵 Tb_Entregador
Tabela para alocar o entregador.

- **Colunas Principais**:
  - `Pk_id_cpf`
  - `nome`
  - `telefone`
  - `cnh`
  - `email`
  - `senha`
  - `status`
  - `conta_bancaria`
  - `turno`
  - `Fk_id_cnpj`

### 📈 Tb_Faturamento
Tabela para alocar o faturamento.

- **Colunas Principais**:
  - `Pk_id`
  - `despesa`
  - `ganho`
  - `data`
  - `Fk_cnpj_id`
  - `Fk_id_cpf`

### 🛒 Tb_Pedido
Tabela para alocar o pedido.

- **Colunas Principais**:
  - `Pk_id`
  - `nome`
  - `telefone`
  - `endereco`
  - `forma_pagamento`
  - `idUsuario`
  - `descricao`
  - `entregue`
  - `Fk_id_cpf`

### 📄 Tb_Contrato
Tabela para alocar o contrato.

- **Colunas Principais**:
  - `Pk_id`
  - `nome`
  - `caminho_contrato`
  - `data_criacao`
  - `Fk_id_plano`
  - `Fk_id_cnpj`

### 📋 Tb_Comanda
Tabela para alocar a comanda.
- **Colunas Principais**:
  - `Pk_id`
  - `endereco_entrega`
  - `informacao_pagamento`
  - `Fk_id_cpf`
  - `Fk_id_pedido`

### 📋 Tb_Faturamento_empresa
Tabela para associar a empresa com o faturamento
- **Colunas Principais**:
  - `Fk_id_cnpj`
  - `Fk_id`
