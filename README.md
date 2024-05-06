css
/*CRIANDO VARIAVEIS PARA AS CORES*/
:root {
    --cor-de-fundo: #1E1E1E;
    --verde: #6FFF57;
    --branco: #FFFFFF;
    --botao-ativo: #3A375E;
    --botao-inativo: rgba(58, 55, 94, 0.5);
    --texto-fundo: rgba(58, 55, 94, 0.3);
}


/*ESTILIZANDO A PAGINA, COR DE FUNDO E DA FONTE*/
body {
    background-color: var(--cor-de-fundo);
    color: var(--branco);
    font-family: 'Chakra Petch', sans-serif;
}

/*ORGANIZANDO POSIÇOES DO CONTEUDO PRINCIPAL NO SITE*/
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
    text-align: center;
    width: 100%;
    font-size: 32px;
}

/*MUDANDO COR DE PARTE DO TITULO PRINCIPAL*/
.titulo-principal span {
    color: var(--verde);
}

/*ESTILIZANDO BOTOES*/
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

    /*ESTILIZANDO CONTORNO DOS BOTOES*/
    border-bottom: 4px solid var(--botao-ativo);
    border-left: 2px solid var(--botao-ativo);
    border-right: 2px solid var(--botao-ativo);
    border-top: none;
}

/*ESTILIZANDO BORDAS DOS BOTOES E AJUSTE PARA CELULAR*/
.botao:first-child {
    border-radius: 40px 40px 0 0;
}

@media screen and (min-width: 768px) {
    .botoes {
        display: flex;
    }

    .botao:first-child {
        border-radius: 40px 0 0 0;
    }

    .botao:last-child {
        border-radius: 0 40px 0 0;
    }
}
.ativo{
    background-color: var(--botao-ativo);
    border-bottom: 4px solid var(--verde);
    }
     .contador{
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
      }
      .contador-digito{
        padding: 0 16px;
        text-align: center;
        min-width: 100px;
      }
      .contador-digito-número{
        font-size: 80px;
        margin: 0;
      }
      .contador-digito-texto{
        color: var(--verde);
        font-size: 20px;
        margin: 0;
      }


      main
      const botoes = document.querySelectorAll(".botao");
const textos = document.querySelectorAll(".aba-conteudo");

for (let i = 0; i < botoes.length; i++) {
    botoes[i].onclick = function () {

        for (let j = 0; j < botoes.length; j++) {
            botoes[j].classList.remove("ativo");
            textos[j].classList.remove("ativo");
        }

        botoes[i].classList.add("ativo");
        textos[i].classList.add("ativo");
    }
}

const contadores = document.querySelectorAll(".contador");
const tempoObjetivo1 = new Date("2023-10-05T00:00:00");
let tempoAtual = new Date();

contadores[0].textContent = tempoObjetivo1 - tempoAtual;
function calculaTempo(tempoObjetivo)
    let tempoAtual = new Date();
    let tempoFinal = tempoObjetivo - tempoAtual;
    let segundos = Math.floor(tempoFinal / 1000);
    let minutos = Math.floor(segundos / 60);
    let horas = Math.floor(minutos / 60);
    let dias = Math.floor(horas / 24);

    segundos %= 60;
    minutos %= 60;
    horas %= 24;
    if (tempoFinal > 0){
        return [dias,horas,minutos,segundos];
    } else
        return [0,0,0,0];
 
function atualizaCronometro()
    document.getElementById("dias0").textContent = calculaTempo(tempos[0])[0];
    document.getElementById("horas0").textContent = calculaTempo(tempos[0])[1];
    document.getElementById("min0").textContent = calculaTempo(tempos[0])[2];
    document.getElementById("seg0").textContent = calculaTempo(tempos[0])[3];

    for (let i=0; i<contadores.length;i++){
       // contadores[i].textContent = calculaTempo(tempos[i]);  
    }
    if (tempoFinal > 0){
        return [dias,horas,minutos,segundos];
    } else {
        return [0,0,0,0];
    }
    function atualizaCronometro(){
        for (let i=0; i<contadores.length;i++){
            document.getElementById("dias"+i).textContent = calculaTempo(tempos[i])[0];
            document.getElementById("horas"+i).textContent = calculaTempo(tempos[i])[1];
            document.getElementById("min"+i).textContent = calculaTempo(tempos[i])[2];
            document.getElementById("seg"+i).textContent = calculaTempo(tempos[i])[3];
            console.log("seg"+i);
        }
    }

    
index
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

        <div class="abas-textos">
            <div class="aba-conteudo ativo">
                    <h3 class="aba-conteudo-titulo-principal">Estudar 4 cursos na Alura</h3>
                    <h4 class="aba-conteudo-titulo-secundario">Tempo para completar o objetivo</h4>
                    <div class="contador">
                        <div class="contador-digito">
                            <p class="contador-digito-numero" id="dias0">30</p>
                            <p class="contador-digito-texto">dias</p>
                          </div>
                          <div class="contador-digito">
                             <p class="contador-digito-numero" id="horas0">4</p>
                             <p class="contador-digito-texto">horas</p>
                          </div>
                          <div class="contador-digito">
                             <p class="contador-digito-numero" id="horas0">5</p>
                             <p class="contador-digito-texto">horas</p>
                          </div>
                          <div class="contador-digito">
                              <p class="contador-digito-numero" id="min0">7</p>
                              <p class="contador-digito-texto">min</p>
                          </div>
                          <div class="contador-digito">
                              <p class="contador-digito-numero" id="seg0">7</p>
                              <p class="contador-digito-texto">seg</p>
                          </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>


        <div class="abas-textos">
                <div class="aba-conteudo">
                    <h3 class="aba-conteudo-titulo-principal">Estudar 4 cursos na Alura</h3>
                    <h4 class="aba-conteudo-titulo-secundario">Tempo para completar o objetivo</h4>
                </div>
                <div class="aba-conteudo">
                    <h3 class="aba-conteudo-titulo-principal">Criar 5 projetos em JavaScript</h3>
                    <h4 class="aba-conteudo-titulo-secundario">Tempo para completar o objetivo</h4>
                </div>
                <div class="aba-conteudo">
                    <h3 class="aba-conteudo-titulo-principal">Criar um portfolio com os meus 3 melhores projetos</h3>
                    <h4 class="aba-conteudo-titulo-secundario">Tempo para completar o objetivo</h4>
                </div>
                <div class="aba-conteudo">
                    <h3 class="aba-conteudo-titulo-principal">Atualizar meu currículo com os certificados da Alura</h3>
                    <h4 class="aba-conteudo-titulo-secundario">Tempo para completar o objetivo</h4>
                </div>
            </div>



        </div>



    </section>
    <script src="main.js"></script>
</body>


</html>

                           
