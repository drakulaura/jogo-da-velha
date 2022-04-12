# jogo da velha 
O jogo da velha ou jogo do galo ou três em linha é um jogo e/ou passatempo popular.
É um jogo de regras extremamente simples,
que não traz grandes dificuldades para seus jogadores e é facilmente aprendido.

 - **HTML**: estrutura do site
- __CSS__: estilização do site  
- *_JS_*: funções do site 
- ~~BootStrap~~: nao foi utilizado

### disponibilizado em 
[githubpage] (https://github.com/drakulaura/jogo-da-velha)

###criado por Aline Roa e Guilherme Mateus

### prints da tela

| ID | primeira tela | segunda tela |
|----|---------------|----------------|
| 1  | início de jogo | fim de jogo |
| 2  | ![jogo](https://user-images.githubusercontent.com/99741182/162993996-6c48fb48-2d11-4b6e-bcfd-6b309b059d90.png)|![jogo2](https://user-images.githubusercontent.com/99741182/162994056-52a55b92-61a6-4b96-9008-b487e7989b84.png)   |


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
