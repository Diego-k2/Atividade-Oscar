# Atividade Oscar

Muito bem, Pessoal... 

Hoje vamos trabalhar com o Oscar.
A ideia de premiar ou ser premiado é para reconhecer:
- Reconhecer uma qualidade
- Reconhecer um atributo
- Reconhecer o esforço... 

Reconhecer sempre.

Nem todos os prêmios são merecidos e nem todos que merecem ganham. 
Então vale mesmo a pena, premiar? 


<h3>USO DOS COMANDOS SQL</h3>

<b>1)-Quantas vezes Natalie Portman foi indicada ao Oscar?</b>
Ela foi indicadas 3 vezes. <br>
<b>QUERY EM SQL</b>
<code>SELECT COUNT(*) FROM oscar WHERE name LIKE '%Natalie Portman%';</code>

<br><br>

<b>2)-Quantos Oscars Natalie Portman ganhou?</b>
Ela venceu uma vez. <br> 
<b>QUERY EM SQL</b>
<code>SELECT COUNT(*) FROM oscar WHERE name LIKE '%Natalie Portman%' AND winner LIKE '%True%';</code>

<br><br>

<b>3)-Amy Adams já ganhou algum Oscar?</b>
Ela nunca venceu. <br>






