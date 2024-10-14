Enunciado da Atividade: Sistema de Reserva de Vagas de Estacionamento

Você deve desenvolver uma aplicação que simule a gestão de um sistema de reserva de vagas de estacionamento em um condomínio. O estacionamento tem capacidade máxima de 15 vagas, e essas vagas devem ser atribuídas de acordo com as reservas feitas pelos moradores.

Regras:

1. O número de vagas disponíveis é limitado a 15, armazenadas em um arranjo chamado parkingSlots. Inicialmente, todas as vagas estão desocupadas (null).
2. Cada vaga pode ser reservada por um objeto da classe ReservationEntry, que contém o nome do morador e a placa do veículo.
3. A reserva de uma vaga deve seguir uma ordem de chegada: o primeiro a solicitar uma vaga ocupa a primeira disponível. Não pode haver "buracos" entre as vagas ocupadas; quando uma vaga é desocupada, as reservas subsequentes devem ser deslocadas para preencher os espaços.
4. Se todas as vagas estiverem ocupadas, uma nova reserva só poderá ser feita quando uma vaga for liberada (você deverá implementar uma função de cancelamento de reserva).
5. A aplicação deve permitir:
   - Reservar uma vaga para um morador (inserindo o nome e a placa do carro).
   - Cancelar uma reserva (liberar a vaga).
   - Listar todas as vagas ocupadas com seus respectivos moradores e placas de veículos.


Objetivos da Implementação:
- Gerenciar dinamicamente a lista de reservas, sempre garantindo que as vagas ocupadas estejam ordenadas sem espaços vazios no arranjo.
- Implementar as classes e métodos necessários para adicionar, remover e consultar reservas, respeitando as regras definidas.
