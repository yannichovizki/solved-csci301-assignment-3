Download Link: https://assignmentchef.com/product/solved-csci301-assignment-3
<br>
<strong> </strong>Create a simple blockchain system simulating proof-of-work between two parties, Alice and Bob. Use the blockchain system given in Lab 4 and create blocks by competing with each other using proof-of-work.




<ol>

 <li>Both players have an initial block and series of transactions in a genesis block given in Lab 4 to start their play.</li>

 <li>When the system is initialized, both Alice and Bob compete with each other to add a new block in the system using proof-of-work. Therefore, they compute &lt;Nounce&gt; of the new block which satisfies the following condition:</li>

</ol>




<em> SHA256(&lt;New block&gt;) &lt; 2<sup>236</sup> </em>




<ol start="3">

 <li>To make Alice and Bob’s mining time different. Let Alice and Bob search a valid &lt;Nonce&gt; value in a new block from 0 and 1,000,000,000, respectively and increase it by 1.</li>

 <li>If one finds a valid &lt;Nonce&gt; value for a new block, it broadcasts the block (or necessary information to form the block) using the PubNub system. The other party then verifies the received block in a way discussed in Task 8 of Lab 4 Note. If the received block is valid, it stops the current mining process and starts mining of the next block.</li>

</ol>

<em> </em>

<em>[Alternative] Stopping a process in  the middle computation needs some advanced coding skills to implement and manage threads. If you are not familiar with thread computing, you can implement that the receiver waits until the current mining is finished and send a completion message to the sender. Therefore, both parties start the next block generation if the mining of the current block for both parties finishes. It should be noted that only the block generated first is considered as a valid block. The block created later (from the receiver) will be discarded. </em>

<strong> </strong>

<h2>Marks</h2>

<ul>

 <li>Implementation of the proof-of-work process. (20 marks)</li>

 <li>Block validation process implementation. (10 marks)</li>

 <li>The other basic requirements of the system (e.g., block generation) (30 marks)</li>

 <li>Implementation of the blocks exchange protocol (PubNub) (30 marks)</li>

 <li>Report (10 marks)</li>

</ul>




<strong>                </strong>

1







CSCI301 Contemporary Topics in Security

This material is copyrighted. It must not be distributed without permission from Jongkil Kim

<h2>Submission</h2>

Make a folder named Assignment3 and include  –      Programs for Alice and Bob.

<ul>

 <li>The history of one of the completed games (e.g., block0.txt, block1.txt, …, and txt)</li>

 <li>Report explaining the requirements to execute your program and the expected outcome of your program.</li>

</ul>




Compress the Assignment3 folder using a zip program to create yourSurname_Assignment3.zip.


