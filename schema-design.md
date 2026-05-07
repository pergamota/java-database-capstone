Tabela: pacientes
id: INT, Primary Key, Auto Increment
nome: VARCHAR(100), NOT NULL
idade: INT, NOT NULL
telefone: VARCHAR(20)
email: VARCHAR(100), UNIQUE
status: ENUM('ATIVO', 'INATIVO')


Tabela: doutores
id: INT, Primary Key, Auto Increment
nome: VARCHAR(100), NOT NULL
crm: VARCHAR(20), UNIQUE, NOT NULL
especialidade: VARCHAR(100)
status: ENUM('TRABALHANDO', 'FERIAS')


Tabela: agendamento
id: INT, Primary Key, Auto Increment
paciente_id: INT, Foreign Key → patients(id)
doutor_id: INT, Foreign Key → doctors(id)
data_agendamento: DATETIME, NOT NULL
tipo_exame: VARCHAR(100)
status: ENUM('AGENDADO', 'EM_ANDAMENTO', 'FINALIZADO', 'CANCELADO')


Tabela: administração
id: INT, Primary Key, Auto Increment
nome: VARCHAR(100), NOT NULL
email: VARCHAR(100), UNIQUE
senha: VARCHAR(255), NOT NULL
