# Proj_IndM-dulo03
![image](https://github.com/G0lg4rthur/Proj_IndM-dulo03/assets/101434220/e425d276-ab38-4499-ad8e-c205d143ee66)


1. Entidades:
Empresa, Tecnologia, Utilização de Tecnologia, Colaborador

2. Principais campos e tipos:
- Empresa:
  - empresa_id: int
  - nome: varchar(100)
  - endereço: varchar(200)
  - contato: varchar(100)
  - outros_detalhes: varchar(255)

- Tecnologia:
  - tecnologia_id: int
  - nome: varchar(100)
  - área: varchar(100)
  - outros_detalhes: varchar(255)

- Utilização de Tecnologia:
  - empresa_id: int (chave estrangeira referenciando company_id da tabela Empresa)
  - tecnologia_id: int (chave estrangeira referenciando technology_id da tabela Tecnologia)
  - data_inicio: data
  - data_termino: data
  - outros_detalhes: varchar(255)

- Colaborador:
  - colaborador_id: int
  - nome: varchar(100)
  - cargo: varchar(100)
  - empresa_id: int (chave estrangeira referenciando empresa_id da tabela Empresa)
  - outros_detalhes: varchar(255)

3. Relacionamentos:
A tabela Utilização de Tecnologia possui chaves estrangeiras (empresa_id e tecnologia_id) referenciando as chaves primárias das tabelas Empresa e Tecnologia, respectivamente. A tabela Colaborador possui uma chave estrangeira (empresa_id) referenciando a chave primária da tabela Empresa.

4. Exemplos de registros:
- Empresa:
  - empresa_id: 1
  - nome: "Empresa A"
  - endereço: "Rua X, 123"
  - contato: "empresa_a@example.com"
  - outros_detalhes: "Detalhes sobre a Empresa A"

- Tecnologia:
  - tecnologia_id: 1
  - nome: "Tecnologia A"
  - área: "Webdev"
  - outros_detalhes: "Detalhes sobre a Tecnologia A"

- Utilização de Tecnologia:
  - empresa_id: 1
  - tecnologia_id: 1
  - data_inicio: "2023-01-01"
  - data_termino "2023-06-30"
  - outros_detalhes: "Detalhes sobre o uso da Tecnologia A pela Empresa A"

- Colaborador:
  - colaborador_id: 1
  - nome: "João Silva"
  - cargo: "Desenvolvedor"
  - empresa_id: 1
  - outros_detalhes: "Detalhes sobre o colaborador João Silva na Empresa A"
