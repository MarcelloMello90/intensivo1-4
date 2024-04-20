/*HTML*/
<div class="square"></div>


/*CSS*/
body{
  background-color: black;
}

.square{
  width: 4rem;
  height: 4rem;
  background-color: white;
  opacity: .6;
}

.square{
  /* animation-name: move, blink; nome da animaçao
  animation-duration: 1s, 200ms; /* tempo da animaçao
  animation-fill-mode: forwards; propriedade que sera seguida quando a animaçao terminar
  -informaçoes anteriores, 0%, backwards
  -informaçoes posteriores, 100%, forwards
  

  animation-direction: alternate;propriedade de direçao da animaçao. pode ser em numeros (ex. 2, sera realizada 2 vezes)

  animation-iteration-count: infinite;definir a quantidade de vezes que sera exibida a animaçao

  animation-delay: 2s; tempo de espera 

  animation-timing-function: steps(10);como a animaçao ira se comportar*/

  animation: move 1s forwards alternate infinite, blink 100ms infinite; /*todas as propriedades acima em uma so linha de codigo*/
}

.square:hover{
  animation-play-state: paused;/*utilizada para o estado do elemento. podemos deixar ele parado ao passar o mouse*/
}
@keyframes move{
  0%{

  }

  100%{
  transform: translateX(calc(100vw - 100% - 16px));
    
  }
}

@keyframes blink{
  0%, 100%{
    opacity: .1;
  }
  
  50%{
    opacity: 1;
  }
}
