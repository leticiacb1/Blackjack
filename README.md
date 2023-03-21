##  blackjack-reply98 🃏️

<div align="center" style="max-width:68rem;">
<table>
  <tr>
    <td align="center"><a href="https://github.com/matheus-1618"><img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/matheus-1618" width="100px;" alt=""/><br /><sub><b>Matheus Oliveira</b></sub></a><br /><a href="https://github.com/matheus-1618" title="Matheus Silva M. Oliveira"></a> Developer</td>
   <td align="center"><a href="https://github.com/niveaabreu"><img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/niveaabreu" width="100px;" alt=""/><br /><sub><b>Nívea de Abreu</b></sub></a><br /><a href="https://github.com/niveaabreu" title="Nívea de Abreu"></a>Developer</td>
      <td align="center"><a href="https://github.com/leticiacb1"><img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/leticiacb1" width="100px;" alt=""/><br /><sub><b>Letícia Côelho</b></sub></a><br /><a href="https://github.com/leticiacb1" title="Letícia Côelho"></a>Developer</td>

  </tr>
</table>
</div>


### Bibliotecas ⚙️

Instale as dependências:

```bash
  pip install -r requirements.txt
```

### Parâmetros para o código 📌️

Nas primeiras linhas do código temos o seguinte:

```bash
    # Condições do programa:
    treino = True
    method = 'qlearning'
```

O parâmetro de treino indica se será feita uma GridSearch para a busca dos melhores parâmetros (**treino = True**) , ou se deseja utilizar a tabela já pronta em `data/q-table-blackjack.csv` (**treino = False**).

o parâmetro método define com qual algorítimo o treino será feito Sarsa (**method = sarsa**) ou QLearning (**method = qlearning**).

### Melhores Hyperparâmetros - 64% de "não derrotas" (Soma de vitórias e empates)

<div align="center" style="max-width:68rem;">

| Atributo        |  Valor     |
|:----------------|:----------:|
| Algoritmo       | Qlearning  |
| alpha           |  0.0001    |
| gamma           |    0.4     |
| epsilon         |    0.95    |
| epsilon_dec     |   0.9999   |
| epsilon_min     |  0.0001    |
| qtd_episodios   |   100000   |

O arquivo `data/info_parameters.json` apresenta o desempenho de cada um dos hyperparâmetros utiliazdos para o treino.

<img src="best_result.png" />

</div>

### Gráfico Qtable
Foram plotadas as situações encontradas pela Qtable, gerando assim duas visualizações distintas dos estados possíveis (Soma da mão do jogador vs Carta apresentada pelo Dealer):



* Quando o ás é uma carta útil, as ações tomadas pelo algoritmo são descritas pela figura abaixo, onde quadrados verdes representam a **ação de continuar pedindo cartas** e quadrados roxos representam a **ação de parar o jogo**.

<div align="center" style="max-width:68rem;">

<img src='Usable_ace.png'/>

</div>

* Já a figura abaixo, mostra a representação de ações tomadas quando o ás não é útil, seguindo a mesma representação anterior: 
<div align="center" style="max-width:68rem;">
<img src='Not_usable_ace.png'/>
</div>