CSS
:root {
    --cor-de-fundo: #1E1E1E;
    --verde: #6FFF57;
    --branco: #FFFFFF;
    --botao-ativo: #3A375E;
    --botao-inativo: rgba(58, 55, 94, 0.5);
    --texto-fundo: rgba(58, 55, 94, 0.3);
}

@import url('https://fonts.googleapis.com/css2?family=Chakra+Petch:wght@400;700&display=swap');

body {
    background-color: var(--cor-de-fundo);
    color: var(--branco);
    font-family: 'Chakra Petch', sans-serif;
}

.conteudo-principal {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    max-width: 1200px;
    width: 100%;
    margin: 0 auto;
}

.titulo-principal {
    text-align: left;
    width: 100%;
}

.titulo-principal span {
    color: var(--verde);
}

.botao {
    font-family: "Crakra Petch", sans-serif;
    background-color: var(--botao-inativo);
    color: var(--branco);
    display: flex;
    justify-content: center;
    padding: 1em;
    font-size: 18px;
    align-items: center;
    width: 100%;
    border-bottom: 4px solid var(--botao-ativo);
    border-left: 2px solid var(--botao-ativo);
    border-right: 2px solid var(--botao-ativo);
    border-top: none;
}

.botoes {
    display: block;
}

@media screen and (min-width: 768px) {font-size: 32px;}

.botao:first-child {
    border-radius: 40px 40px 0 0;
}
    .botao:first-child {
        border-radius: 40px 0 0 0;
    }

    .botao:last-child {
        border-radius: 0 40px 0 0;
    }
    border-bottom: 4px solid var(--botao-ativo); 
    border-left: 2px solid var(--botao-ativo); 
    border-right: 2px solid var(--botao-ativo); 
    border-top: none;
    .ativo{
        background-color: var(--botao-ativo);
        border-bottom: 4px solid var(--verde);
        }


        INDEX
        <!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meus objetivos do ano</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>
    <section class="conteudo-principal">
        <h2 class="titulo-principal">Meus Objetivos do ano<span>_</span></h2>
        <div class="botoes">
            <button class="botao ativo">Cursos na Alura</button>
            <button class="botao">Criar projetos em Javascript</button>
            <button class="botao">Criar um portfolio</button>
            <button class="botao">Atualizar meu currículo</button>
        </div>
    </section>
</body>
</html>

MAIN
const botoes = document.querySelectorAll(".botao");

for(let i=0;i <botoes.length;i++){
    botoes[i].onclick = function(){
        
        for(let j=0;j<botoes.length;j++){
            botoes[j].classList.remove("ativo");
        }
        botoes[i].classList.add("ativo");
    }
    console.log();
}
