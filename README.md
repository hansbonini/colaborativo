# API
Nós de acesso da API do servidor

## Sorteios

### Sorteio Atual
- URL:
```/games/current```
- Tipo: ```GET```
- Resposta:
```javascript
{
  "status":200, // Resposta válida de status 200
  "game": {
    "createdAt":1583690791524, // Data de Criação do Sorteio
    "updatedAt":1583691130064, // Data de Atualização do Sorteio
    "id":"5e6534274ad02000047aad14", // Chave do Sorteio para Consulta
    "sequence":2, // Sequencia do Sorteio exibida pro usuário
    "ScheduledTime":1609438500000, // Horário de Execução do Sorteio
    "Price":2, // Valor da doação do Sorteio
    "Prize1":5, // Valor Quadra do Sorteio
    "Prize2":20, // Valor da Linha do Sorteio
    "Prize3":50, // Valor do Bingo do Sorteio
    "Accumulated":1000, // Valor Acumulado do Sorteio
    "AccumulatedBalls":40, // Acumulando valendo até a bola número 40
    "Balls":    [83,46,90,27,53,9,32,11,43,85,50,65,36,57,8,28,3,33,34,80,58,25,38,17,44,15,47,64,72,76,87,19,21,73,23,12,39,62,75,84,1,13,18,4,35,59,37,61,79,56,74,49,14,82,30,51,7,41,20,48,86,81,24,2,77,70,52,69,71,63,10,67,54,45,40,55,89,42,88,16,31,60,68,26,6,66,78,5,22,29], // Números sorteados em ordem (90 Bolas)
    "Enabled":true, // Sorteio Ativo (sempre ativo para o cliente, inativas não retornam na consulta)
    "Finished":false // Sorteio Finalizado
  }
}
```

### Listar proximos sorteios
- URL:
```/games/next```
- Tipo: ```GET```
- Resposta:
```javascript
{
  "status":200, // Resposta válida de status 200
  "games":    [
    {
    "createdAt":1583690791524, // Data de Criação do Sorteio
    "updatedAt":1583691130064, // Data de Atualização do Sorteio
    "id":"5e6534274ad02000047aad14", // Chave do Sorteio para Consulta
    "sequence":2, // Sequencia do Sorteio exibida pro usuário
    "ScheduledTime":1609438500000, // Horário de Execução do Sorteio
    "Price":2, // Valor da doação do Sorteio
    "Prize1":5, // Valor Quadra do Sorteio
    "Prize2":20, // Valor da Linha do Sorteio
    "Prize3":50, // Valor do Bingo do Sorteio
    "Accumulated":1000, // Valor Acumulado do Sorteio
    "AccumulatedBalls":40, // Acumulando valendo até a bola número 40
    "Balls":    [83,46,90,27,53,9,32,11,43,85,50,65,36,57,8,28,3,33,34,80,58,25,38,17,44,15,47,64,72,76,87,19,21,73,23,12,39,62,75,84,1,13,18,4,35,59,37,61,79,56,74,49,14,82,30,51,7,41,20,48,86,81,24,2,77,70,52,69,71,63,10,67,54,45,40,55,89,42,88,16,31,60,68,26,6,66,78,5,22,29], // Números sorteados em ordem (90 Bolas)
    "Enabled":true, // Sorteio Ativo (sempre ativo para o cliente, inativas não retornam na consulta)
    "Finished":false // Sorteio Finalizado
  }
]}
```

### Listar sorteios anteriores
- URL:
```/games/finished```
- Tipo: ```GET```
- Resposta:
```javascript
{
  "status":200, // Resposta válida de status 200
  "games":    [
    {
    "createdAt":1583690791524, // Data de Criação do Sorteio
    "updatedAt":1583691130064, // Data de Atualização do Sorteio
    "id":"5e6534274ad02000047aad14", // Chave do Sorteio para Consulta
    "sequence":2, // Sequencia do Sorteio exibida pro usuário
    "ScheduledTime":1609438500000, // Horário de Execução do Sorteio
    "Price":2, // Valor da doação do Sorteio
    "Prize1":5, // Valor Quadra do Sorteio
    "Prize2":20, // Valor da Linha do Sorteio
    "Prize3":50, // Valor do Bingo do Sorteio
    "Accumulated":1000, // Valor Acumulado do Sorteio
    "AccumulatedBalls":40, // Acumulando valendo até a bola número 40
    "Balls":    [83,46,90,27,53,9,32,11,43,85,50,65,36,57,8,28,3,33,34,80,58,25,38,17,44,15,47,64,72,76,87,19,21,73,23,12,39,62,75,84,1,13,18,4,35,59,37,61,79,56,74,49,14,82,30,51,7,41,20,48,86,81,24,2,77,70,52,69,71,63,10,67,54,45,40,55,89,42,88,16,31,60,68,26,6,66,78,5,22,29], // Números sorteados em ordem (90 Bolas)
    "Enabled":true, // Sorteio Ativo (sempre ativo para o cliente, inativas não retornam na consulta)
    "Finished":true // Sorteio Finalizado
  }
]}
```
