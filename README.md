Download Link: https://assignmentchef.com/product/solved-icsi410-homework-3
<br>
<u>Problem 1. </u>(20 points) Consider a situation where <em>hash join </em>is applied to relations <em>R </em>and <em>S</em>. Assume that (1) relation <em>R </em>contains 10<sup>9 </sup>disk blocks, (2) relation <em>S </em>contains 10<sup>8 </sup>disk blocks, (3) the size of each disk block is 1<em>KB</em>, (4) the hash join partitions <em>S </em>into 15 buckets in a manner where each bucket fits into the main memory, and (5) 16<em>GB </em>of main memory is used for buffering (one buffer is used for each file being read or written and all of the buffers have the same size). Answer each of the following questions:

<ul>

 <li>( Calculate the <em>number of block transfers </em>and the <em>number of disk seeks </em>during the <em>partitioning phase </em>of the hash join. Justify your answer. To simplify cost analysis, assume that (i) the last block of each bucket from <em>R </em>and <em>S </em>is completely filled and (ii) when the end of each bucket is saved, the buffer for the bucket is completely filled.</li>

 <li>(10 points) Calculate the <em>number of block transfers </em>and the <em>number of disk seeks </em>during the <em>build and probe phases </em>of the hash join. Justify your answer.</li>

</ul>

<u>Problem 2. </u> Consider a situation where <em>external sort-merge </em>is applied to relation <em>R </em>in

Problem 1. Note that the size of the main memory is 16<em>GB </em>and thus the main memory can keep up to 16 × 10<sup>6 </sup>disk blocks. Answer each of the following questions:

<ul>

 <li>(10 points) Explain <em>how many initial runs </em>will be created. Also, describe how <em>many block transfers </em>and <em>disk seeks </em>will be needed to create all of these initial runs.</li>

 <li>(10 points) After the initial runs are created as explained above, <em>external sort-merge </em>repeatedly merges a number of runs into a bigger run until only one final run remains. Assume that each merge pass uses 8 input buffers and 1 output buffer. Explain <em>how many merge passes </em>are needed to obtain one final run. Also, calculate <em>the total number of block transfers </em>during these merge passes (assume that the final run is not actually written to disk and consumed in memory, for example, by a selection or a join operator). Justify your answer.</li>

</ul>

<u>Problem 3. </u>(20 points) Consider a situation where <em>merge join </em>is applied to relations <em>R </em>and <em>S</em>

described in Problem 1. Answer each of the following questions:

<ul>

 <li>(10 points) Assume relations <em>R </em>and <em>S </em>are already sorted by the join column(s). Explain how many <em>block transfers </em>and <em>disk seeks </em>this join requires when it uses, for <em>R </em>and <em>S</em>, two buffers of the same size in the 16<em>GB </em>of the main memory.</li>

 <li>(10 points) Explain whether it is more advantageous to use <em>hash join </em>or <em>merge join </em>when only <em>S </em>is already sorted by the join column(s) and thus <em>R </em>needs to be sorted (only for merge join, not hash join) as in Problem 2. Justify your answer by considering <em>the number of block transfers </em>(and ignoring the number of disk seeks) for each of these join scenarios.</li>

</ul>

1

<u>Problem 4. </u>(10 points) Consider relations <em>R</em>(<em>A,B,C</em>), <em>S</em>(<em>C,D,E</em>) and <em>T</em>(<em>E,F,G</em>). Find a rela-

tional expression which (1) is equivalent to Π<em><sub>A,G</sub></em>(<em>R </em><em>1 </em><em>S 1 </em><em>T</em>) and (2) applies projection to each of <em>R</em>, <em>S </em>and <em>T </em>on the smallest number of attributes.

<u>Problem 5. </u>(20 points) Determine whether or not each of the following statements is true for any

arbitrary relations <em>R</em>(<em>A,B</em>) and <em>S</em>(<em>A,B</em>). If a statement is true, prove it. Otherwise, give a relevant example.

<ul>

 <li>(10 points) Π<em><sub>A</sub></em>(<em>R </em>∩ <em>S</em>) = Π<em><sub>A</sub></em>(<em>R</em>) ∩ Π<em><sub>A</sub></em>(<em>S</em>)</li>

 <li>(10 points) <em>σ<sub>θ</sub></em>(<em>R </em>∪ <em>S</em>) = <em>σ<sub>θ</sub></em>(<em>R</em>) ∪ <em>σ<sub>θ</sub></em>(<em>S</em>)</li>

</ul>

<u>Problem 6. </u>(10 points) Consider four relations <em>R</em>(<em><u>A</u>,Z</em>), <em>S</em>(<em><u>B</u>,A</em>), <em>T</em>(<em><u>C</u>,B</em>) and <em>U</em>(<em><u>D</u>,C</em>) (the

primary keys are underlined). Assume that (1) <em>A </em>in <em>S </em>is a foreign key to <em>R</em>, (2) <em>B </em>in <em>T </em>is a foreign key to <em>S</em>, (3) <em>C </em>in <em>U </em>is a foreign key to <em>T</em>, (4) these relations do not contain any null value, and (5) the size (i.e., the number of rows) of each relation is as follows:

<em>r<sub>R </sub></em>= 4000<em>, r<sub>S </sub></em>= 3000<em>, r<sub>T </sub></em>= 2000<em>, r<sub>U </sub></em>= 1000<em>.</em>

Also, assume that all attributes of the relations are of the same length and we use hash join, so the cost of joining <em>X </em>∈ {<em>R,S,T,U</em>} and <em>Y </em>∈ {<em>R,S,T,U</em>} can be expressed as:

<em>k</em>(<em>r<sub>X </sub></em>· <em>c<sub>X </sub></em>+ <em>r<sub>Y </sub></em>· <em>c<sub>Y </sub></em>)

where <em>k </em>is a constant, <em>r<sub>X </sub></em>and <em>c<sub>X </sub></em>denote the number of rows and the number of columns of <em>X</em>, respectively, and <em>r<sub>Y </sub></em>and <em>c<sub>Y </sub></em>denote the number of rows and the number of columns of <em>Y </em>(we ignore the cost of producing the output relation).

Under the above assumptions, find the lowest cost plan for computing <em>R 1 </em><em>S 1 </em><em>T 1 </em><em>U </em>using <em>dynamic programming </em>and <em>left-deep </em>join trees. You need to complete the following table while finding the best plans (e.g., in the form of ((<em>212</em>) <em>12</em>) <em>12 </em>in the last line) and associated costs.

<table width="463">

 <tbody>

  <tr>

   <td width="115">Subquery</td>

   <td width="45">Size</td>

   <td colspan="2" width="231">Cost</td>

   <td width="73">BestPlan</td>

  </tr>

  <tr>

   <td width="115"><em>R 1 </em><em>S</em></td>

   <td width="45">3000</td>

   <td width="68">14000<em>k</em></td>

   <td width="162">[= (4000 · 2 + 3000 · 2)<em>k</em>]</td>

   <td width="73"><em>R 1 </em><em>S</em></td>

  </tr>

  <tr>

   <td width="115"><em>R 1 </em><em>T</em></td>

   <td width="45"> </td>

   <td width="68"> </td>

   <td width="162"> </td>

   <td width="73"> </td>

  </tr>

  <tr>

   <td width="115"><em>R 1 </em><em>U</em></td>

   <td width="45"> </td>

   <td width="68"> </td>

   <td width="162"> </td>

   <td width="73"> </td>

  </tr>

  <tr>

   <td width="115"><em>S 1 </em><em>T</em></td>

   <td width="45"> </td>

   <td width="68"> </td>

   <td width="162"> </td>

   <td width="73"> </td>

  </tr>

  <tr>

   <td width="115"><em>S 1 </em><em>U</em></td>

   <td width="45"> </td>

   <td width="68"> </td>

   <td width="162"> </td>

   <td width="73"> </td>

  </tr>

  <tr>

   <td width="115"><em>T 1 </em><em>U</em></td>

   <td width="45"> </td>

   <td width="68"> </td>

   <td width="162"> </td>

   <td width="73"> </td>

  </tr>

  <tr>

   <td width="115"><em>R 1 </em><em>S 1 </em><em>T</em></td>

   <td width="45"> </td>

   <td width="68"> </td>

   <td width="162"> </td>

   <td width="73"> </td>

  </tr>

  <tr>

   <td width="115"><em>R 1 </em><em>S 1 </em><em>U</em></td>

   <td width="45"> </td>

   <td width="68"> </td>

   <td width="162"> </td>

   <td width="73"> </td>

  </tr>

  <tr>

   <td width="115"><em>R 1 </em><em>T 1 </em><em>U</em></td>

   <td width="45"> </td>

   <td width="68"> </td>

   <td width="162"> </td>

   <td width="73"> </td>

  </tr>

  <tr>

   <td width="115"><em>S 1 </em><em>T 1 </em><em>U</em></td>

   <td width="45"> </td>

   <td width="68"> </td>

   <td width="162"> </td>

   <td width="73"> </td>

  </tr>

  <tr>

   <td width="115"><em>R 1 </em><em>S 1 </em><em>T 1 </em><em>U</em></td>

   <td width="45"> </td>

   <td width="68"> </td>

   <td width="162"> </td>

   <td width="73"> </td>

  </tr>

 </tbody>

</table>

After solving the above problems, please state the amount of time spent for this assignment. Feel free to add comments or suggestions if any.

2