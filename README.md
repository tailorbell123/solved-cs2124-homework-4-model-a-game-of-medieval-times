Download Link: https://assignmentchef.com/product/solved-cs2124-homework-4-model-a-game-of-medieval-times
<br>
We will [continue to] model a game of medieval times. Our world is filled with not only warriors but also nobles. Nobles don’t have much to do except do battle with each other. (We’ll leave the feasting and other entertainments for add-ons.) Warriors don’t have much to do except hire out to a noble and fight in his behalf. Of course the nobles are pretty wimpy themselves and will lose if they don’t have warriors to defend them. How does all this work?

<ul>

 <li>Warriors start out with a specified strength.</li>

 <li>A battle between nobles is won by the noble who commands the stronger army.</li>

 <li>The army’s strength is simply the combined strengths of all its warriors.</li>

 <li>A battle is to the death. The losing noble dies as does his warriors.</li>

 <li>The winner does not usually walk away unscarred. All his men lose a portion of their strength equal to the ratio of the enemy army’s combined strenth to their army’s. If the losing army had a combined strength that was 1/4 the size of the winning army’s, then each soldier in the winning army will have their own strength reduced by 1/4.</li>

</ul>

<strong>Hiring and Firing</strong>




<ul>

 <li>Warriors are hired and fired by Nobles. Lack of adequate labor laws, have left the Warriors without the ability to quit, nor even to have a say on whether or not a Noble can hire them.</li>

 <li>However it is possible that an attempt to hire or fire may fail. Naturally the methods should not “fail silently”. Instead, they will return true or false depending on whether they succeed or not.</li>

 <li>A Warrior can only be employed by one Noble at a time and <em>cannot</em>be hired away if he is already employed.</li>

 <li>As noted below, Nobles who are dead can neither hire nor fire anyone. (Note this will <em>implicitly</em>prevent dead Warriors from being hired.)</li>

 <li>When a warrior is fired, he is no longer part of the army of the Noble that hired him. He is then free to be hired by another Noble.

  <ul>

   <li>How do you remove something from a vector.</li>

   <li>While there are techniques that make use of iterators, we have not yet discussed iterators so you will not use them here. (As a heads up, if you see a technique that requires you to call a vector’s begin() method, that is using iterators. Don’t use it.)</li>

   <li>While it may seem a slight burden, certainly it does not require more than a simple loop to remove an item from a vector. No <u>do not</u>do something silly like create a whole new vector.</li>

   <li>Soon we will cover iterators and then you will be freed from these constraints. Patience, please.</li>

  </ul></li>

</ul>

<strong>Death</strong>

It’s a sad topic, but one we do have to address.

<ul>

 <li>People die when they lose a battle, whether they are a Nobles or Warriors.</li>

 <li>Nobles who are dead are in no position to hire or fire anyone. Any attempt by a dead Lord to hire someone will simply fail and the Warrior will remain unhired.</li>

 <li>However curiously, as has been seen before, Nobles can declare battle even though they are dead.</li>

 <li>Note that when a Noble is created he does not have any strength. At the same time he is obviously alive. So lack of strength and being dead are clearly <em>not</em></li>

</ul>

A test program and output are attached. Note that the output shown is what you are <u>expected</u> to generate. Pardon us, we don’t like limiting your creativity, but having your output consistent with ours makes the first step of grading a bit easier. And also helps you to be more confident that your code works.

<strong>Programming Constraints</strong>

What would a homework assignment be without unnecessary and unreasonable constraints?

Your classes must satisfy the following:

<ul>

 <li>The battle method will announce who is battling whom, and the result (as shown in the example output).

  <ul>

   <li>If one or both of the nobles is already dead, just report that. The “winner” doesn’t win anything for kicking around a dead guy. And his warriors don’t use up any strength.</li>

   <li>Look at the output for the sample test program to see what you should be displaying.</li>

  </ul></li>

 <li>A noble’s army is a <strong><u>vector of pointers</u></strong>to warriors. Warriors will be ordered in the army by the order in which they were <em>hired</em>. That affects how you remove a Warrior thatgets fired.</li>

</ul>