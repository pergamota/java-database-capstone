Esta aplicação Spring Boot tem como objetivo um sistema inteligente de gerenciamento de clínica e utiliza uma arquitetura em três camadas. Na camada de apresentação, são utilizados templates Thymeleaf para dashboards (como Admin e Doctor) e APIs REST para outros módulos, permitindo integração com diferentes clientes. Na camada de aplicação, o Spring Boot gerencia controladores, serviços e a lógica de negócio. Já na camada de dados, são utilizados dois bancos: MySQL para dados estruturados (pacientes, médicos, consultas) e MongoDB para dados flexíveis (prescrições). Os controladores direcionam as requisições para a camada de serviço, que aplica regras de negócio e acessa os dados por meio dos repositórios.

1. Camada de Usuário: O usuário acessa o sistema através de dashboards (Thymeleaf) ou clientes REST (como aplicações externas)..
2. Camada de Controlador: A requisição é direcionada para o controlador apropriado (Thymeleaf Controller ou REST Controller), de acordo com a URL e método HTTP.
3. Camada de Serviço: O controlador recebe os dados, valida a requisição e encaminha para a camada de serviço.
4. Camada de Repositório: A camada de serviço aplica a lógica de negócio, realiza validações e coordena o fluxo entre diferentes entidades.
5. Banco de Dados: A camada de serviço chama os repositórios para acessar o banco de dados (MySQL ou MongoDB).
6. Vinculação de modelo: Os dados retornados são convertidos em objetos Java (model binding), como entidades JPA ou documentos MongoDB.
7. Modelos de aplicação em uso: O controlador retorna a resposta ao usuário, podendo ser uma página HTML (MVC) ou dados em JSON (REST).
