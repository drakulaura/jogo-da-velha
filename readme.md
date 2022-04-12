# jogo da velha 
O jogo da velha ou jogo do galo ou três em linha é um jogo e/ou passatempo popular.
É um jogo de regras extremamente simples,
que não traz grandes dificuldades para seus jogadores e é facilmente aprendido.

 - **HTML**: estrutura do site
- __CSS__: estilização do site  
- *_JS_*: funções do site 
- ~~BootStrap~~: nao foi utilizado

### disponibilizado em 
[githubpage] (https://drakulaura.github.io/lotecar/)

### prints da tela

| ID | primeira tela | segunda tela |
|----|---------------|----------------|
| 1  | início de jogo | fim de jogo |
| 2  | ![tela jogo](/home/aluno/Documentos/game/jogo.png) |![tela jogo](/home/aluno/Documentos/game/jogo2.png)     |


### funcão principal 
```
make_play: function(position) {
        if (this.gameover) return false;
        if (this.board[position] === ''){
            this.board[position] = this.simbols.options[this.simbols.turn_index];
            this.draw();
            let winning_sequences_index = this.check_winning_sequences( this.simbols.options[this.simbols.turn_index] );
            if (winning_sequences_index >= 0){
                this.game_is_over();
            } else{
                this.simbols.change();
            }
            return true;
        }
        else {
            return false;
        }
    },

```
