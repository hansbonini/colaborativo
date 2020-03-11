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
    "sequence":2, // Numeração sequencia do Sorteio exibida pro usuário
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
    "sequence":2, // Numeração sequencia do Sorteio exibida pro usuário
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
    "sequence":2, // Numeração sequencia do Sorteio exibida pro usuário
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
## Ganhadores
### Listar ganhadores do sorteio
- URL:
```/winners/{chave do sorteio}```
- Tipo: ```GET```
- Resposta:
```javascript
{
  "winners":{
    "Prize1":{ // Prêmio da Quadra
      "Ball":53, // Bola em que saiu o prêmio
      "Cards": [{ // Cartelas que ganharam o prêmio da Quadra
        "createdAt":1583792885374, // Data de criação da cartela
        "updatedAt":1583793845554, // Data de atualizaçao da cartela
        "id":"5e66c2f6f2e0990004fdeae1", // Chave da cartela para consulta
        "sequence":2, // Numeração sequencia da cartela exibida ao usuário
        "GameID":"5e66c2f5f2e0990004fdeade", // Chave do Sorteio para Consulta
        "SellerID":"5e5d6366bddda10017e299ec", // Chave do Vendedor para Consulta
        "Numbers":[31,21,78,46,22,37,58,17,25,76,85,59,80,35,82], // Números da Cartela (15) (Exibidos em 3 linhas de 5)
        "Prize1":53, // Bola em que saiu o prêmio Quadra da Cartela
        "Prize2":60, // Bola em que saiu o prêmio Linha da Cartela
        "Prize3":89, // Bola em que saiu o prêmio Bingo da Cartela
        "Active":true, // Cartela Ativa
        "Processed":true, // Cartela Processada
       }]
    },
    "Prize2":{ // Prêmio da Linha
      "Ball":53, // Bola em que saiu o prêmio
      "Cards": [{ // Cartelas que ganharam o prêmio da Linha
        "createdAt":1583792885374, // Data de criação da cartela
        "updatedAt":1583793845554, // Data de atualizaçao da cartela
        "id":"5e66c2f6f2e0990004fdeae1", // Chave da cartela para consulta
        "sequence":2, // Numeração sequencia da cartela exibida ao usuário
        "GameID":"5e66c2f5f2e0990004fdeade", // Chave do Sorteio para Consulta
        "SellerID":"5e5d6366bddda10017e299ec", // Chave do Vendedor para Consulta
        "Numbers":[31,21,78,46,22,37,58,17,25,76,85,59,80,35,82], // Números da Cartela (15) (Exibidos em 3 linhas de 5)
        "Prize1":53, // Bola em que saiu o prêmio Quadra da Cartela
        "Prize2":60, // Bola em que saiu o prêmio Linha da Cartela
        "Prize3":89, // Bola em que saiu o prêmio Bingo da Cartela
        "Active":true, // Cartela Ativa
        "Processed":true, // Cartela Processada
       }]
     },
     "Prize3": { // Prêmio do Bingo
        "Ball":83, // Bola em que saiu o prêmio
        "Cards": [{ // Cartelas que ganharam o prêmio do Bingo
          "createdAt":1583792885374, // Data de criação da cartela
          "updatedAt":1583793845554, // Data de atualizaçao da cartela
          "id":"5e66c2f6f2e0990004fdeae0", // Chave da cartela para consulta
          "sequence":1,, // Numeração sequencia da cartela exibida ao usuário
          "GameID":"5e66c2f5f2e0990004fdeade", // Chave do Sorteio para Consulta
          "SellerID":"5e5d6366bddda10017e299ec", // Chave do Vendedor para Consulta
          "Numbers":[79,7,65,21,5,50,32,52,78,2,3,33,86,41,43], // Números da Cartela (15) (Exibidos em 3 linhas de 5)
          "Prize1":67, // Bola em que saiu o prêmio Quadra da Cartela
          "Prize2":81, // Bola em que saiu o prêmio Linha da Cartela
          "Prize3":83, // Bola em que saiu o prêmio Bingo da Cartela
          "Active":true, // Cartela Ativa
          "Processed":true // Cartela Processada
        }]
      },
      "Sellers":{"5e5d6366bddda10017e299ec":"Bar do Gordo"} // Nome dos Vendedores das cartelas vencedoras por Chave
  },
  "status":200 // Status da Resposta
 }
```
