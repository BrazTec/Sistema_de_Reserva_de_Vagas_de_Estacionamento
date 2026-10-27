# Reserva de vagas de estacionamento

Exercício de Java com uma implementação inicial de reservas em memória para um estacionamento de condomínio com **15 vagas**.

## Conteúdo real

- `code`: arquivo de texto sem extensão, contendo o pacote `Vagas_reservadas`, a classe pública `VagasReservadas<E extends ReservationEntry>` e a classe auxiliar `ReservationEntry`.
- `README.md`: documentação do exercício.

## Regras do exercício e implementação

Cada reserva guarda nome do morador e placa do veículo. O arranjo `parkingSlots` começa com posições nulas.

| Método | Comportamento presente |
| --- | --- |
| `size()`, `isEmpty()` | Consultam a quantidade de reservas |
| `reservarVaga(name, placa)` | Insere na primeira posição livre; retorna falso quando cheio |
| `liberarVaga(placa)` | Remove a primeira reserva com a placa e reorganiza o arranjo |
| `reorganizarVagas()` | Método privado que compacta as reservas preservando sua ordem |
| `listarReservas()` | Imprime posições ocupadas, nomes e placas no console |

A ordem de chegada é representada pela inserção na primeira posição livre. Não existe fila de espera: ao atingir 15 reservas, uma nova solicitação é recusada até haver liberação.

## Estrutura Java e uso

Para experimentar sem alterar o arquivo original, copie `code` para uma pasta de trabalho como `Vagas_reservadas/VagasReservadas.java`. O nome do arquivo deve corresponder à classe pública. Configure um JDK e compile essa cópia:

```sh
javac -encoding UTF-8 -d build Vagas_reservadas/VagasReservadas.java
```

O uso de conversões para o tipo genérico pode gerar avisos de compilação. Não há `main`, menu ou teste automatizado versionado; para chamar os métodos, é necessário um programa de exemplo separado. `ReservationEntry` tem acesso de pacote, o que também deve ser considerado ao criar esse exemplo.

## Limitações

Os dados só existem em memória. Não há banco de dados, interface gráfica, autenticação, validação de nomes/placas ou bloqueio de placas duplicadas. A capacidade é fixa e a posição exibida pode mudar após um cancelamento. O parâmetro genérico é limitado a `ReservationEntry`, mas o método de reserva instancia diretamente essa classe auxiliar.

O enunciado pede adicionar, cancelar e listar reservas sem deixar espaços entre posições ocupadas; o código contém esses métodos, sem comprovação por testes automatizados. Esta revisão documental preserva o arquivo `code` e a privacidade do repositório.
