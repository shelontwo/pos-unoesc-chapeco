------ INICIO do artigo ------

Atomic Design

Evandro Diego Erlo (O2 Multicomunicação)
{erlo.evandro@gmail.com}

Resumo:

Neste artigo será abordado sobre o tema "Atomic Design", que vem a ser uma metáfora baseada em conceitos de quimica.

1) O que é?

Atomic Design, é uma metodologia desenvolvida para a criação de design. Esta metodologia de criação de design foi desenvolvida pelo Brad Frost, em seu livro ele comenta que página de um site é algo que para o usuário final torna-se um elemento isolado, algo quantifícavel, mas na verdade uma página Web, no caso removendo o conceito da palavra página, seria algo bi-direcional, possuindo inúmeros pontos interdependentes. Uma "página" de web é a junção de vários elementos, que, quando todos unidos pelo interpratador tornam-se um elemento único visualmente.

2) Como funciona

O Atomic Design, funcina de maneira semelhante a átomos, moléculas e organismos, que juntando vários elementos de várias maneiras diferentes se transformam em um outro objeto que pode ser uma página web em si. Frost seguiu esta medotologia pelo princípio dos átomos, na web, site, softwares, app e tudo mais é gerado através da junção de vários elementos HTML, JS, CSS, que destes elementos podem surgir vários grupos de outros elementos, e destes grupos de elementos podem surgir mais outros vários grupos de elementos, nesta lógica em design web, você tem uma base de diversos elementos/átomos, que podem ser utilizados para montar os mais diversos sistemas/organismos possíveis.

###### Funcionamento do Atomic Design com base em princípios de química.

- Partes do Atomic Design
	- Átomos, em conceito químico átomo é aquilo que não pode ser dividido, logo em web, átomo pode ser qualquer tag HTML que não necessita de nenhum contexto para existir, exemplo uma tag `<i>`.
    - Moléculas, em conceito químico, são agrupamentos de atómos, logo em web pode ser usado por exemplo em uma Label de formulário com um campo input de texto, que juntos formam um outro objeto que pode ser utilizado para vários outras pontas do projeto.
	- Organismos, seria uma junção de moléculas para se formar algo novo, seguindo nosso exemplo, com a molécula da label com o input podemos juntar ela várias vezes e ja criar um organismo ligeiramente criando um formulário, mesmo dentro deste organismo podem existir outros organismos como por exemplo o botão deste formulário ser gerado através da junção de várias outras moléculas que podem ser originadas de Átomos de CSS, JS e afins.
    - Templates, esta teoria todo mundo já conhece, é onde já se tem algo mais visualmente estruturado, sendo semelhantes as wireframes de um projeto, é a junção de vários organismos gerados com todos os átomos inicialmente criados.
    - Páginas, por fim chegamos ao contexto de página, que nada mais é da estrutra final de todos os organismos, moléculas, templates, átomos que foram projetados para serem usados na geração de todas as páginas do projeto, esta seria a etapa final, por sua vez, a estrutura concluida.

3) Para que usar

O Atomic design é um conceito muito interesante de se usar principalmente em projetos de grande porte, tambem em seu livro Frost relata o exemplo de se criar um portal institucional ontem existem 30 mil páginas para serem desenvolvidas, isso certamente assutará qualquer desenvolvedor, mas partindo do princípio de Atomic Designer, facilitária a criação deste projeto, onde inicialmente criaria todos os grupos de elementos/átomos possiveis para este projeto ou com as ferramentas que voce pretende utillizar, sendo assim você densenvolve uma base onde todo o restante do projeto se molda nestes átomos inicialmente criados. Em caso de projetos de pequeno porte como citado no artigo da Tableless, projetos de pequeno porte não necessariamente trabalhariam com o conceito de Atomic design, pois a quantia de elementos finais é muito baixa, sendo não necessário possuir um imenso leque de opções com os mais diversos átomos assim como propoe o Atomic Design.

4) Onde usar?

O Atomic design segundo artigo públicado em `nomadev` referênciado pela Filosofia Unix, detalha que Atomic design é mais atrativa sua utilização em sistemas web, onde você utilizará os mais diversos elementos repetidamente, montando novas etapas deste software com base nos mesmo átomos definidos inicialmente. Retrata-se pelo exemplo dado anteriormente do projeto de 30 mil páginas sendo que sua estrutura de átomos / elementos inicias será utilizada e reutilizada diversas vezes por vários locais diferentes do projeto. Por estes motivos destaca-se novamente que não necessariamente você saira utilizando Atomic design para todo lado, até na página em manutenção la do site que você irá desenvolver, mas sim utilizando em casos que a estrutra inicial seja utilizada das maisdiversas maneiras possíveis.

5) Exemplos:

Vamos usar o exemplo que tivemos de base para esclarecimentos:
- Meus átomos:
```html
<label>Nome</label>

<form></form>

<label>Data de nascimento</label>

<input type="text">

<input type="date">

<input type="submit">

<div></div>
```
```css
    display: block;
    
    font-size: 15px;
    
    font-family: 'Arial'; 
    
    color:purple; 
    
    width:100%;
    
    float: left; 

```
- Moléculas:
```html
    
    <div class="linha_form">
        <label>Nome</label>
        <input type="text">
    </div>

    <div class="linha_form">
        <label>Data de nascimento</label>
        <input type="date">
    </div>
    
    <div class="linha_form">
        <input type="submit">
    </div>

```
```css
    .linha_form{
        display: block;
        font-size: 15px;
        font-family: 'Arial'; 
        color:purple; 
    }
    label{
      width:100%;
      float: left; 
    }
``` 
-Organismo

```html
<form>
    <div class="linha_form">
        <label>Nome</label>
        <input type="text">
    </div>
    <div class="linha_form">
        <label>Data de nascimento</label>
        <input type="date">
    </div>
    <div class="linha_form">
        <input type="submit">
    </div>
</form>
```

-Template:
######ja deixando melhor visualmente juntando com outras Moléculas, Átomos diversos.
[Exemplo aqui](http://codepen.io/shelontwo/pen/epVGJV)

-Página:

######Finalizado por exemplo a página de contato.

[Exemplo aqui](http://codepen.io/shelontwo/pen/NGyabd)


6) Referências

#####http://tableless.com.br/o-que-e-design-atomic/
#####http://pt.slideshare.net/bradfrostweb/atomic-design
#####http://nomadev.com.br/atomic-design-por-que-usar/
#####http://atomicdesign.bradfrost.com/chapter-1/
#####http://www.frontendbrasil.com.br/tutoriais/atomic-design-como-funciona/
------ FIM do artigo ------