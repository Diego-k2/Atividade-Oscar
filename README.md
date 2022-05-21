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
<b>R: </b>Ela foi indicadas 3 vezes. <br>
<b>QUERY EM SQL</b>
<code>SELECT COUNT(*) FROM oscar WHERE name LIKE '%Natalie Portman%';</code>

<br><br>

<b>2)-Quantos Oscars Natalie Portman ganhou?</b>
<b>R: </b>Ela venceu uma vez. <br> 
<b>QUERY EM SQL</b>
<code>SELECT COUNT(*) FROM oscar WHERE name LIKE '%Natalie Portman%' AND winner LIKE '%True%';</code>

<br><br>

<b>3)-Amy Adams já ganhou algum Oscar?</b><br>
<b>R: </b>Ela nunca venceu. <br>
<b>QUERY EM SQL</b>
<code>SELECT COUNT(*) FROM oscar WHERE name LIKE '%Amy Adams%' AND winner LIKE '%True%';</code>

<br><br>

<b>4)-Alguém já ganhou um Oscar e tem o seu primeiro nome??</b><br>
<b>R: </b>Não <br>

<b>QUERY EM SQL</b><br>
<code>SELECT COUNT(*) FROM oscar WHERE name LIKE '%Diego%' AND winner LIKE '%True%';</code>

<br><br>


<b>5)-Toy Story 3 ganhou um Oscar em quais anos?/b><br>
<b>R: </b>2010 <br>
<b>QUERY EM SQL</b><br>
<code>SELECT name, year_film FROM oscar WHERE film LIKE '%Toy Story 3%' AND winner LIKE '%True%';</code>

<br><br>
  
<b>6)-Quem tem mais Oscars: a categoria "Melhor Ator" ou "Melhor Filme"?</b <br>
<b>R: </b>Melhor Ator <br>  
<b>QUERY EM SQL</b><br>
<code>SELECT category, COUNT(category) FROM oscar WHERE category LIKE '%ACTOR' OR category LIKE '%CINEMATOGRAPHY' AND winner LIKE '%True%' GROUP BY category;</code>

<br><br>
 
<b>7)-O primeiro Oscar para melhor Atriz foi para quem? Em que ano?/b><br>
<b>R: </b>Janet Gaynor em 1928<br>
<b>QUERY EM SQL</b><br>
<code>SELECT name, MIN(year_ceremony) FROM oscar WHERE category LIKE '%ACTRESS%' AND winner LIKE '%True%';</code>

<br><br>

<b>8)-Na categoria Winner, altere todos os valores com "True" para 1 e todos os valores "False" para 0./b><br>
<b>R: </b> <code>UPDATE  oscar SET winner = '1' WHERE winner LIKE '%True%'</code><br>
<b>R: </b> <code>UPDATE  oscar SET winner = '0' WHERE winner LIKE '%False%'</code>
  
<br><br>

 
<b>9)-Em qual edição do Oscar "Crash" ganhou o prêmio?</b><br>
<b>R: </b>Em 2006<br>
<b>QUERY EM SQL</b><br>
<code>SELECT year_ceremony FROM oscar WHERE film LIKE '%Crash' AND winner LIKE '%1%';</code>

<br><br>

<b>10)-Que filme merecia ganhar um Oscar e não ganhou?</b><br>
<b>R: </b>Joker<br>

<br><br>

<b>11)-Bom... dê um Oscar para esse filme, então.</b><br>
<b>R: </b> <code>UPDATE oscar SET winner = '1' WHERE id = 10294</code>

<br><br>
  
<b>12)-O filme Central do Brasil aparece no Oscar?</b><br>
<b>R: </b>Não<br>
<b>QUERY EM SQL</b><br>
<code>SELECT * FROM oscar WHERE film LIKE '%Central do Brasil';</code>
  
<br><br>

<b>13)-Aliás... Qual sua opinião sobre central do Brasil</b><br>
<b>R: </b>Nunca assisti ,as vou colocar na minha base de dados<br>

<br><br>
  
<b>14)-Inclua no banco 7 filmes que nunca nem foram nomeados ao Oscar, mas que na sua opinião, merecem.</b><br>
 <b>R: </b><code>INSERT INTO oscar (`year_film`, `category`, `name`, `film`, `winner`) VALUES ('1980', 'CINEMATOGRAPHY', 'Charles Chaplin', 'Tempos Modernos', '0'), ('1980', 'CINEMATOGRAPHY', 'Stanley Kubrick', 'O Iluminado', '0'), ('1988', 'CINEMATOGRAPHY', 'Hayao Miyazaki', 'Meu Amigo Totoro', '0'), ('1993', 'CINEMATOGRAPHY', 'Harold Ramis', 'Feitiço do Tempo', '0'), ('1997', 'CINEMATOGRAPHY', 'Hayao Miyazaki', 'Princesa Mononoke', '0'), ('2016', 'CINEMATOGRAPHY', 'Makoto Shinkai', 'Your Name', '0'), ('2017', 'CINEMATOGRAPHY', 'Patty Jenkins', 'Mulher-Maravilha', '0');</code>  

<br><br>
  
<b>15)-Crie uma nova categoria de premiação. Qualquer prêmio que você queira dar. Agora vamos dar esses prêmios aos filmes que você cadastrou na questão acima.</b><br>
<b>R: </b><code>ALTER TABLE oscas ADD curto BINARY;</code>  <br>
<b>R: </b><code>UPDATE oscar SET curto = 1 WHERE id BETWEEN 10396 AND 10403;</code>  
  
<br><br>  
  
 
 <b>16)-Pensando no ano em que você nasceu: Qual foi o Oscar de melhor filme, Melhor Atriz e Melhor Diretor?</b><br>
<b>R: </b><br>
<b>QUERY EM SQL</b><br>
<code></code>
  
<br><br>
  
  
  
  
  
  
  
