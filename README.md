# Proj_IndM-dulo03
![image](https://github.com/G0lg4rthur/Proj_IndM-dulo03/assets/101434220/e425d276-ab38-4499-ad8e-c205d143ee66)


1. Entidades:
Empresa, Tecnologia, Utilização de Tecnologia, Colaborador

2. Principais campos e tipos:
- Empresa:
  - company_id: int
  - nome: varchar(100)
  - endereço: varchar(200)
  - contato: varchar(100)
  - other_details: varchar(255)

- Tecnologia:
  - tecnologia_id: int
  - nome: varchar(100)
  - área: varchar(100)
  - other_details: varchar(255)

- Utilização de Tecnologia:
  - company_id: int (chave estrangeira referenciando company_id da tabela Empresa)
  - technology_id: int (chave estrangeira referenciando technology_id da tabela Tecnologia)
  - start_date: data
  - date_term: data
  - other_details: varchar(255)

- Colaborador:
  - colaborador_id: int
  - nome: varchar(100)
  - cargo: varchar(100)
  - company_id: int (chave estrangeira referenciando company_id da tabela Empresa)
  - other_details: varchar(255)

3. Relacionamentos:
A tabela Utilização de Tecnologia possui chaves estrangeiras (company_id e technology_id) referenciando as chaves primárias das tabelas Empresa e Tecnologia, respectivamente. A tabela Colaborador possui uma chave estrangeira (company_id) referenciando a chave primária da tabela Empresa.

4. Exemplos de registros:
- Empresa:
  - company_id: 1
  - nome: "Empresa A"
  - endereço: "Rua X, 123"
  - contato: "empresa_a@example.com"
  - other_details: "Detalhes sobre a Empresa A"

- Tecnologia:
  - tecnologia_id: 1
  - nome: "Tecnologia A"
  - área: "Webdev"
  - other_details: "Detalhes sobre a Tecnologia A"

- Utilização de Tecnologia:
  - company_id: 1
  - technology_id: 1
  - start_date: "2023-01-01"
  - date_term: "2023-06-30"
  - other_details: "Detalhes sobre o uso da Tecnologia A pela Empresa A"

- Colaborador:
  - colaborador_id: 1
  - nome: "João Silva"
  - cargo: "Desenvolvedor"
  - company_id: 1
  - other_details: "Detalhes sobre o colaborador João Silva na Empresa A"
