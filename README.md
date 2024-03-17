
# Visualização de Arquitetura de Microserviços

Abaixo está a representação de uma arquitetura de microserviços típica:

<div style="text-align:center;">
  <img src="https://github.com/Joaooh98/microservices/blob/main/introduction/simpleExample.png" style="width:750px; max-width:100%;" alt="Computador">
</div>

## Descrição da Arquitetura

- **Client**: O sistema pode ser acessado por clientes através de dispositivos como web e mobile, além de PCs.
- **API Gateway**: Atua como um ponto de entrada unificado para as solicitações dos clientes, direcionando-as para os serviços apropriados.
- **Microserviços**: Incluem serviços dedicados para funções específicas como 'Shopping Cart', 'Billing', 'User Profile' e 'Push Notification'.
- **Bancos de Dados**: Cada microserviço tem seu próprio banco de dados, seguindo o padrão de Database per Service para garantir a independência dos dados.
- **Identity Provider**: Autentica as solicitações dos usuários e emite tokens de acesso.
- **Service Registry & Discovery**: Permite que os microserviços registrem suas instâncias e descubram as dos outros para facilitar a comunicação interna.
- **Monitoring**: Monitora os microserviços para garantir a alta disponibilidade e o desempenho adequado do sistema.

Cada componente desempenha um papel vital para garantir que a arquitetura de microserviços seja escalável, resiliente e fácil de manter.

