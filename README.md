Download Link: https://assignmentchef.com/product/solved-eecs484-homework-1-conceptual-physical-or-external-schema
<br>
<h1>PART 1</h1>

Question 1

Determine if the following statements regarding the data of an online store describe a <strong>conceptual/logical</strong>​, ​<strong>physical</strong>​ or ​<strong>external </strong>​representation/schema of data.

<ol>

 <li>All data are stored as sorted files on cassette.</li>

 <li>Students can see name, credit and rating for each course.</li>

 <li>ID, name and price of all items is stored in a single table.</li>

 <li>Question 2</li>

</ol>

Consider the given ​<em>instances </em>​(i.e., snapshot/subset) of a relation.

In this snapshot, there are 3 attributes: A, B and C (ID, Anonymized Age Group, Name).




<table width="624">

 <tbody>

  <tr>

   <td width="208"><strong>A (ID) </strong></td>

   <td width="208"><strong>B (Anonymized Age Group) </strong></td>

   <td width="208"><strong>C (Name) </strong></td>

  </tr>

  <tr>

   <td width="208">100</td>

   <td width="208">a</td>

   <td width="208">George</td>

  </tr>

  <tr>

   <td width="208">200</td>

   <td width="208">f</td>

   <td width="208">Nick</td>

  </tr>

  <tr>

   <td width="208">350</td>

   <td width="208">c</td>

   <td width="208">Jackie</td>

  </tr>

  <tr>

   <td width="208">400</td>

   <td width="208">d</td>

   <td width="208">Laura</td>

  </tr>

  <tr>

   <td width="208">100</td>

   <td width="208">e</td>

   <td width="208">Ellie</td>

  </tr>

  <tr>

   <td width="208">500</td>

   <td width="208">b</td>

   <td width="208">Paul</td>

  </tr>

  <tr>

   <td width="208">350</td>

   <td width="208">x</td>

   <td width="208">Jackie</td>

  </tr>

 </tbody>

</table>




By analyzing this snapshot, for each of the following attribute sets specify whether it is <strong>definitely a key</strong>​, ​<strong>definitely NOT a key</strong>​, or​<strong> might be a key</strong>​.

<table width="106">

 <tbody>

  <tr>

   <td width="72"> </td>

   <td width="34"> </td>

  </tr>

  <tr>

   <td width="72">(i)</td>

   <td width="34">A</td>

  </tr>

  <tr>

   <td width="72">(ii)</td>

   <td width="34">B</td>

  </tr>

  <tr>

   <td width="72">(iii)</td>

   <td width="34">C</td>

  </tr>

  <tr>

   <td width="72">(iv)</td>

   <td width="34">AB</td>

  </tr>

  <tr>

   <td width="72">(v)</td>

   <td width="34">AC</td>

  </tr>

  <tr>

   <td width="72">(vi)</td>

   <td width="34">BC</td>

  </tr>

  <tr>

   <td width="72">(vii)</td>

   <td width="34">ABC</td>

  </tr>

 </tbody>

</table>

<h2>Question 3</h2>

The following ER diagram shows the relationships between hospital employees and patients:

Determine whether or not each of the following statements is ​<strong>True</strong>​ or ​<strong>False</strong>​, given the constraints reflected by the above ER diagram. (2 points each)

<ol>

 <li>A nurse, Alice (eid=30), is allowed to sit idle (care for no patients).</li>

 <li>A patient, Dave (pid=23) cannot be “cared for” during multiple shifts by nurse Alice (eid=30).</li>

 <li>A patient, Dave (pid=23), can be taken care of by nurses Alice (eid=30) and Alex (eid=32) in two different shifts.</li>

 <li>The above diagram is wrong because the Nurse entity does not have a primary key.</li>

 <li>This design enforces that in each shift, every patient is taken care of.</li>

</ol>

<strong>           </strong>Question 4

Consider the following ER diagram that represents one way a music database could be designed:

<strong> </strong>Answer all of the following true/false questions referring to the previous ER diagram (2 points each):

<ol>

 <li>Does this design allow multiple musicians to give concert in the same date and place?</li>

 <li>Does this design allow a musician to give multiple concerts in the same place in different dates?</li>

 <li>Does this design allow for a song which is not in any album?</li>

 <li>Does this design allow a musician to perform songs produced by another musician, in a concert?</li>

 <li>Does this design allow multiple musicians to collaborate on an album?</li>

 <li>Does this design allow musicians to collaborate with other musicians to perform a song?</li>

 <li>Does the above ER diagram allow for a musician who only sings (i.e. does not play an instrument)?</li>

 <li>Does this design allow a musician to produce an album that contains no songs?</li>

 <li>Does this design allow a musician to give a concert without performing any songs?</li>

 <li>Each album in this database can be linked back to the instruments that could have been used in the album. Does this diagram enforce that each album is linked with at least one instrument?</li>

 <li>Does this diagram enforce that each song is linked with at least one​ ​instrument?</li>

</ol>

<h2>Question 5</h2>

Answer the following true/false questions about keys:

<ol>

 <li>A candidate key for the relation ‘Teaches’ in the above ER Diagram is {pid, cid}</li>

 <li>A candidate key for the relation ‘Teaches’ in the above ER Diagram is {cid}</li>

</ol>

<em>The following questions are about table representation of the above diagram. </em>​<em>Assume the minimal number of tables are used to represent the ER diagram. </em>

<ol>

 <li>‘pid’ is NOT a foreign key in the Course table</li>

 <li>‘cid’ is a foreign key in the Professor table</li>

 <li>The Course table created by the below SQL statement is complete with regards to ​<em>all</em> integrity constraints shown by the above ER Diagram</li>

</ol>

CREATE TABLE Course (

cid               INTEGER,

cname VARCHAR(200), pid INTEGER,

PRIMARY KEY (cid),

FOREIGN KEY (pid) REFERENCES Professor

);

PART 2 – ER Diagrams

<strong> </strong>Question 6

As the CDBO (Chief Database Officer) of KnowItAll — a new, up-and-coming online bookstore — your job is to design a new database system that can keep track of all the books, authors, publishers, warehouses and customers under your company. Unfortunately, due to budget cuts, you are now the only DBO in your company, so you have to do this by yourself (and maybe along with your partner, if you have one).

In the design of your database, you must keep track of the following:

<ul>

 <li>Each book must have an ISBN, title, edition, and price. (Assume different books will have different ISBNs)</li>

 <li>Each author must have a unique author ID, name, personal website URL, and address.</li>

 <li>Each publisher must have a unique name, phone number, address, and website URL.</li>

 <li>Each book has at least one author, and exactly one publisher.</li>

 <li>Each customer must have an email address (unique), a name, a credit card number, and an address.</li>

 <li>Your company loves to send ads to customers based on their purchase history, so you will also have to store the following:</li>

</ul>

o    Each customer will have exactly one “shopping cart”, and shopping carts must belong to exactly one customer. Each shopping cart needs a unique id. o            This shopping cart will contain a customer’s purchase history, which includes: purchased book, number of copies, and date of purchase.

&#x25aa;     Note: Customers should be able to purchase the same book multiple times, on different ​<em>dates</em>​. Purchases on the same day should be grouped together.

<ul>

 <li>You need to track your warehouses (that store your books) as well. Each warehouse must have a unique code, an address, and a phone number.</li>

 <li>Each warehouse can store any number of copies of any book.</li>

</ul>

Design an ER diagram that reflects the constraints described above. State any assumptions you make that are not specifically addressed in the question. Always follow the constraints described in the questions, even if you don’t think they make sense in the real world.

Ensure that all your entities, attributes and constraints are drawn (again, state assumptions clearly if they are not stated in the question).

<strong>         </strong>Question 7

As a football lover, and a database enthusiast, you want to design a database to model university football teams. This includes the teams themselves, the games, the players and the referees.

In the design, you want to capture the following:

<ul>

 <li>For each football team, you want to store their unique team ID, name, main stadium and the university to which the team belongs.</li>

 <li>Each player on each team will have a unique ID, name, date of birth (DoB), and shirt number. o Each team has many players and each player can belong to only one team. ​<em>It is possible that a player does not belong to any team.</em></li>

 <li>You want to store data on all the football matches:

  <ul>

   <li>Each match has one host team and one guest team o Each match has a Match ID, match date, and a final result</li>

   <li>Each match must store which players participated in the match (each match must have at least one player), as well as:</li>

  </ul></li>

</ul>

&#x25aa;     The number of points the player scored, and their total time playing in that match

<ul>

 <li>Players can substitute for other players during each match, which should be recorded as well:</li>

</ul>

&#x25aa;     One player may substitute for any player; however, a player can substitute for the same player only once in a match (e.g., A can substitute for B only once in a match, but A can substitute for other players in the same match and be substituted for too.)

<ul>

 <li>You believe who referees a match makes a big difference, so you’d also like to capture the following:

  <ul>

   <li>Each match has multiple referees. Each referee should have a unique ID, name, DoB, and years of experience. o There is one main referee per match. Note that a referee can be a main referee for one match, but not the main referee for another match. (It does not mean “if a referee is a main referee in one match, he can never main referee again”, but means “if a referee was a main referee once, he is not necessarily the main referee for another match”. See point 3 for details.)</li>

   <li>A referee can either have never been a main referee, been a main referee for only one match, or been a main referee for more than one match. It does not mean that the referee can only be a main referee once.</li>

  </ul></li>

</ul>

Complete the ER diagram below so that it reflects the constraints described above. Once again, state any assumptions you make that are not specifically addressed in the question. Always follow the constraints described in the questions, even if you don’t think they make sense in the real world.

Ensure that all your entities, attributes and constraints are drawn (again, state assumptions clearly if they are not stated in the question). Please do not modify any given entities and attributes. However, you can modify the given constraints.

<em>HINT: To complete this question, you may want to add more entities, relations and attributes. You may want to modify some of the given constraints as well. </em>