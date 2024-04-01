

INDEX
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Objetivo para 2024</title>
</head>
<body>
    <section class="conteudo-principal">
    <h2 class="titulo-principal">Meus Objetivos do ano_</h2>
    <div class="botoes">
        <button class="botao">Cursos na Alura</button>
        <button class="botao">Criar projetos em JavaScript</button>
        <button class="botao">Criar um portfólio</button>
        <button class="botao">Atualizar meu currículo</button>
    </div>
    </section>


</body>


</html>


CSS
<link rel="stylesheet" href="style.css">
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
:root {
    --cor-base: #ff6347;
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
    font-size: 32px;
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

@media screen and (min-width: 768px) {
    .botoes {
        display: flex;
    }
}
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
   
