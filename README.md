<div align="center">
  <img src="https://user-images.githubusercontent.com/61476935/207375452-8b965f99-b054-4aef-9885-b8bce6c0e9c2.png" >
</div>
<br>
<img src="https://img.shields.io/static/v1?label=Git&message=flow&color=red&style=for-the-badge&logo="/>

O git flow é um modelo de workflow comumente utilizado por squads de desenvolvimento com o intuito de maximizar e aprimorar o versionamento de código, visando uma maior organização e segurança. Antes de mais nada, para uma melhor compreenção do assunto, é importante entender que o git flow não se trata da ferramenta git, mas sim de uma estratégia que se aplica a esta. 

De forma sucinta, a estratégia consiste em uma organização das branchs que permita ter um controle do fluxo de criação, aprimoramento e release das novas features de um sistema. Mas, antes de entrarmos nos conceitos propriamente ditos, cabe entender como o git é comumente utilizado.

<h1>Git</h1>

O git, como já deve estar claro, é uma ferramenta de controle de versão, ou seja, ela permite o acesso aos "momentos" de um fluxo de desenvolvimento, isto é: permite que os desenvolvedores de um time acessem e modifiquem um código de diferentes formas e registrem essas modificações em uma timeline de ramificações (branches), sem necessariamente modificar o código original. Este modelo pode ser representado como uma árvore cujos galhos se originam do tronco, sendo este a branch ```master```:

<div align="center">
  <img src="">
</div>

<h1>Por que o Git Flow ?</h1>

Tendo em mente que o git não necessariamente precisa do git flow para exercer sua função, é natural que o seu uso seja questionado. Porém, esta questão encontra uma resposta quando se compreende que o desenvolvimento de sistemas pode ter proporções bastante diversas.

Um sistema simples pode ser desenvolvido sem gerar preocupações quanto ao seu versionamento. Já sistemas de grande porte, precisam de uma atenção maior neste sentido, já que a quantidade de problemas resultante deles é muito maior, devido a quantidade de informação gerada e o número de contribuintes. Com isso, é possível concluir, que seu uso é recomendado em situações de maior complexidade, afim de evitar problemas no decorrer do desenvolvimento.

<h2>Conceitos</h2>


