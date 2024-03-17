
# Arquitetura de Microserviços com Tecnologias Específicas

## Camadas da Arquitetura de Microserviços

### 1. Hardware
Utilizando serviços de nuvem como a Amazon Web Services (AWS), esta camada fornece a infraestrutura necessária, como computação (EC2), armazenamento (S3) e rede (VPC).

### 2. Comunicação
Kafka, uma plataforma de streaming distribuído, facilita a comunicação assíncrona entre microserviços, garantindo escalabilidade e tolerância a falhas. Além disso, a implementação de um sistema de Service Registry e Discovery é crucial nesta camada para permitir que os serviços se localizem e comuniquem dinamicamente.
## Comunicação Assíncrona vs. Síncrona

### Comunicação Assíncrona
- **Definição**: O emissor envia uma mensagem sem esperar por uma resposta imediata.
- **Impactos**: Reduz a dependência entre serviços, aumenta a escalabilidade e tolerância a falhas. Porém, pode complicar o fluxo de dados e o gerenciamento de erros.
- **Como lidar**: Utilizar sistemas de mensagens como Kafka para enfileiramento e processamento de mensagens. Implementar mecanismos robustos de tratamento de erros e confirmações de entrega.

### Comunicação Síncrona
- **Definição**: O emissor espera por uma resposta imediata após enviar uma mensagem.
- **Impactos**: Facilita o entendimento do fluxo de comunicação, mas aumenta o acoplamento e pode afetar a escalabilidade.
- **Como lidar**: Utilizar para operações que requerem resposta imediata. Implementar timeouts e circuit breakers para lidar com falhas e evitar a espera indefinida.

### Diferenças Principais
- **Acoplamento**: A comunicação síncrona tende a criar um acoplamento mais forte entre serviços.
- **Escalabilidade**: A assíncrona favorece a escalabilidade, permitindo que os serviços operem de forma mais independente.
- **Complexidade de Gerenciamento**: A comunicação assíncrona pode aumentar a complexidade, exigindo sistemas de mensagens e tratamento de erros mais sofisticados.


### Service Registry e Discovery
- **Função**: Permitir que os serviços se registrem e sejam descobertos dinamicamente, facilitando a comunicação entre eles.
- **Implementação Sugerida**:
  - **AWS Cloud Map**: Para integração com outros serviços AWS.
  - **Kubernetes**: Quando utilizando Quarkus, aproveitando suas capacidades nativas de integração com Kubernetes.

### 3. Plataforma da Aplicação
- **Java**: A linguagem de programação base.
- **Quarkus**: Otimizado para containers, ideal para microserviços.
- **Hibernate**: Framework ORM para a gestão de banco de dados.
- **Keycloak**: Gestão de identidade e acesso.

### 4. Microsserviços
Desenvolvidos, implantados e operados independentemente, implementam funcionalidades de negócios, utilizando as tecnologias mencionadas.


