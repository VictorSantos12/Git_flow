<div align="center">
  <img src="https://user-images.githubusercontent.com/61476935/207375452-8b965f99-b054-4aef-9885-b8bce6c0e9c2.png" >
</div>
<br>
<img src="https://img.shields.io/static/v1?label=Git&message=flow&color=red&style=for-the-badge&logo="/>

O Git Flow é um modelo de workflow comumente utilizado por squads de desenvolvimento com o intuito de maximizar e aprimorar o versionamento de código, visando uma maior organização e segurança. Antes de mais nada, para uma melhor compreensão do assunto, é importante entender que o Git Flow não se trata da ferramenta git, mas sim de uma estratégia que se aplica a esta. 

De forma sucinta, a estratégia consiste em uma organização das branchs que permita ter um controle do fluxo de criação, aprimoramento e release das novas features de um sistema. Mas, antes de entrarmos nos conceitos propriamente ditos, cabe entender como o git é comumente utilizado.

<h1>Git</h1>

O git é uma ferramenta de gerenciamento de versão, ou seja, ela registra e da acesso aos "momentos" de um fluxo de desenvolvimento, isto é: permite que os desenvolvedores de um time acessem e modifiquem um código de diferentes formas, através de uma versão deste código; esta que se manifestam em uma timeline de ramificações (branches), sem necessariamente modificar o código original. Este modelo pode ser representado como uma árvore cujos galhos se originam do tronco, sendo este a branch ```master```.

<h1>Por que o Git Flow ?</h1>

Tendo em mente que o git não necessariamente precisa do Git Flow para exercer sua função, é natural que o seu uso seja questionado. Porém, esta questão encontra uma resposta quando se compreende que o desenvolvimento de sistemas pode ter proporções bastante diversas.

Um sistema simples pode ser desenvolvido sem gerar preocupações quanto ao seu versionamento. Já sistemas de grande porte, precisam de uma atenção maior neste sentido, já que a quantidade de problemas resultante deles é muito maior, devido a quantidade de informação gerada e o número de contribuintes. Com isso, é possível concluir que seu uso é recomendado em situações de maior complexidade, afim de evitar problemas no decorrer do desenvolvimento.

Por outro lado, não é recomendado que se aplique o Git Flow em projetos com uma alta continuidade de entragas, já que as branches geradas no Git Flow tem uma duração maior que em projetos de pequeno porte.

<h2>Conceitos</h2>

Tendo entendido quando utilizar o Git Flow, agora podemos abordar como utilizá-lo. A princípio, dividimos as ramificações (branches) em dois tipos distintos:. 

<h2>Principais</h2>

As branchs principais, ou seja, aquelas que de fato irão registrar as sequentes atualizações na versão e que serão eternas no Git Flow, são duas: 

<h3>master/main</h3>

A branch master, como é de se esperar, é a branch que origina todas as demais, mantendo registradas todas as releases geradas a partir do que foi desenvolvido, corrigido ou deletado nas branches que dela se originam, gerando o código que irá operar em produção. Quando uma nova release for atribuída a branch master, esta deve recebar uma tag contendo a versão resultante da release. A branch master interage diretamente com três branches: <i>develop</i>, <i>Hotfix</i> e <i>release</i>.

<h3>develop</h3>

A branch develop é a primeira a ser originada da branch master, sendo a ramificação responsável por registrar todas a features estáveis do código que soferá deploy. Isso significa que ela possui funcionalidades que, quando testadas e aprovadas, farão parte de uma release, posteriormente sendo integradas a master. A branch develop interage diretamente com todas as demais branches.

<h2>Suporte</h2>

As branches de suporte, ou seja, as que servem as branhces pricipais, e que não são permanentes dentro do fluxo de desenvolvimento, são três:

<h3>feature</h3>

A branch feature irá originar uma nova funcionalidade a partir da develop, retornando para ela após esta ter sido concluída. Dentro do Git Flow, uma feature conta com uma convenção de nomenclatura que auxilia o seu reconhecimento e mantém um padrão:

> feature/functionality-name

Após a feature em questão sofrer o merge que finda seu desenvolvimento, esta é removida. A branch feature só interage diretamente com sua branch de origem, ou seja, a <i>develop</i>.

<h3>hotfix</h3>

A hotfix se origina da master quando existe uma correção em produção que demande atenção imediata. O que as diferencia de uma feature é que estas se originam da branch principal e, quando são finalizadas, tando a master quanto a develop sofrem um merge, recebendo as correções. Quando retornada a branch master, esta recebe uma tag indicando uma mudança na versão, assim como também é removida. Ela interage diretamente com duas branches: <i>master</i> e <i>develop</i>.

<h3>Release</h3>

A branch release é a soma de todas as features que sofreram merge e compõem a develop, ou seja, ela é a responsável por integrar todas as funcinalidades resultantes do desenvolvimento com a principal branch do projeto, funcionando como um ambiente de homologação e permitindo o deploy para produção. 

Ela também é removida após os testes e o merge com a master terem sido concluídos. Caso esta contenha algum bug ou problema, este deve retornar corrigido a sua origem através de um merge com a develop. No momento de conclusão de uma release uma tag contendo a versão desta deve ser incluída, sendo registado no merge com a master.

A imagem a seguir descreve o fluxo de desenvolvimento e controle de versão com base nos conceitos do Git Flow:

<div align="center">
  <img src="https://user-images.githubusercontent.com/61476935/207422885-5f12d199-5f13-4ce8-9129-fd8ceb746356.png">
</div>

