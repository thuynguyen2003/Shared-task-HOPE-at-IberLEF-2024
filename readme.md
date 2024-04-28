# An Empirical Study of Prompt Engineering with Large Language Models for Hope Detection in English and Spanish

Because we join all subtasks in this shared task, each subject there are a different goal, concept, or label so to convenient for us to present full prompting for each subtask we will pre-define some variables to store some part of the text. And combine those variables in the table to present details of our promptings.

- **Request:**
  - **request_1: request for the Zero-shot and Few-shot technique for task 1** \
    Please classify whether a given text conveys hope or not. Only return the label from [Hope Speech, Non Hope Speech] without any other text.
  - **request_2a: request for the Zero-shot and Few-shot technique for subtask 2a**\
    Please classify whether a given tweet conveys hope or not. Only return the label from [Hope, Not Hope] without any other text.
  - **request_2b: request for the Zero-shot and Few-shot technique for subtask 2b**\
    Please classify whether a given tweet conveys hope or not. If it conveys hope, indicate what specific type of hope it is. Only return the label from [Generalized Hope, Realistic Hope, Unrealistic Hope, Not Hope] without any other text.
  - **request_CoT_1: request for the Chain of thought technique for task 1**\
    Please classify whether a given tweet conveys hope or not. Only return one label from [Hope Speech, Non Hope Speech] and explain your classification results.
  - **request_CoT_2a: request for the Chain of thought technique for subtask 2a**\
    Please classify whether a given tweet conveys hope or not. Only return one label from [Hope, Not Hope] and explain your classification results.
  - **request_CoT_2b: request for the Chain of thought technique for subtask 2a**\
    Please classify whether a given tweet conveys hope or not. Only return one label from [Generalized Hope, Realistic Hope, Unrealistic Hope, Not Hope] and explain your classification results.
- **Concept:**
  - **concept_1: the concept of Hope in task 1**\
    Hope speech is the type of speech that is able to relax a hostile environment and that helps, gives suggestions and inspires for good to a number of people when they are in times of illness, stress, loneliness or depression.
  - **concept_2: the concept of Hope in task 2**\
    Hope is characterized as "openness of spirit toward the future, a desire, expectation, and wish for something to happen or to be true" that remarkably affects a human’s state of mind, emotions, behaviors, and decisions.
- **Class:**
  - **class_1: Meaningful of classes in task 1**\
    Describe the sentiment of the given text using one of these two attributes: “Hope Speech”, “Non Hope Speech”. Knowing that a text is considered as “Hope Speech“ if the text: (1) explicitly supports the social integration of minorities or otherwise distinct groups in society; (2) promotes tolerance, equality, positivity, and healing for all. And knowing that a text is considered “Non Hope Speech” if it: expresses the negative sentiment, discrimination, violence; or uses insults toward people.
  - **class_2a: Meaningful of classes in subtask 2a**\
    Describe the sentiment of the given tweet using one of these two attributes: “Hope”, “Not Hope”. Knowing that a tweet is considered as “Hope” if the tweet conveys a mention of hope. And knowing that a tweet is considered as “Not Hope” if it do not convey hope, expectation, or desire.
  - **class_2b: Meaningful of classes in subtask 2b**\
      <P>
      Describe the sentiment of the given tweet using one of these four attributes: "Generalized Hope",  "Realistic Hope",  "Unrealistic Hope", and “Not Hope”. Knowing the meaning of each attribute is described as follows:<br>
      + Generalized Hope: is expressed as a general hopefulness and optimism that is not directed toward any specific event or outcome<br>
      + Realistic Hope: is about expecting something reasonable, meaningful, and possible thing to happen<br>
      + Unrealistic Hope: is usually in the form of wishing for something to become true, even though the possibility of happening is remote or significantly less or even zero<br>
      + Not Hope: tweets that do not convey hope.
      </P>
- **Role: role defined for all subtasks**\
   You are an NLP engineer expert as a language specialist. You are labeling to create a dataset for the Hope Speech Detection task.
- **Few-shot: **

  - **one-shot_1: one demonstration for task 1**
      <P>Tweet: “Hay que tratar de aislar democrÃ¡ticamente los argumentos polÃ­ticos que justifican a machistas, xenÃ³fobos, racistas y las expresiones de odio a los colectivos LGTBI. El odio genera violencia y la violencia no tiene medida en sus consecuencias”  <br>
      Label: Hope Speech <br>
      Tweet: “Los fundadores del socialismo,-Karl Marx: "Los homosexuales son peores que pederastas".- Friedrich Engels: â€œLa homosexualidad es una aberraciÃ³n de la burguesÃ­a degeneradaâ€.- IÃ³sif Stalin: "La homosexualidad es un vicio burguÃs"”  <br>
      Label: Non Hope Speech <br>
      </P>
  - **three-shot_1: three demonstrations for task 1.** It is similar to one-shot_1, however, the number of demonstrations in each class is three

  - **one-shot_2a_English: one demonstration for English data in subtask 2a**
      <P> 
      Tweet: “When Eric Gill wrote An Essay on Typography in 1931, he probably didn’t anticipate it would live on to become not only the most influential manifesto on typography’s cultural place ever written” <br>
      Label: Not Hope <br>
      Tweet: “i really hate how much namjoon's little art gallery photos make me yearn i want what he has”
      Label: Hope <br>
      </P>

  - **one-shot_2a_Spanish: one demonstration for Spanish data in subtask 2a.** It is similar to one-shot_2a_English, however, the tweet is in Spanish.
  - **three-shot_2a_English: three demonstrations for English data in subtask 2a.** It is similar to one-shot_2a_English, however, the number of demonstrations in each class is three.

  - **three-shot_2a_Spanish: three demonstrations for Spanish data in subtask 2a.** It is similar to one-shot_2a_Spanish, however, the number of demonstrations in each class is three.
  - **one-shot_2b_English: one demonstration for English data in subtask 2b**
      <P>Tweet: “When Eric Gill wrote An Essay on Typography in 1931, he probably didn’t anticipate it would live on to become not only the most influential manifesto on typography’s cultural place ever written”  <br>
      Label: Not Hope <br>
      Tweet: “and I assure you that all of them along with myself wish you nothing but the best for the rest of your career. Thank you so much, and again...congrats!!” <br>
      Label: Generalized Hope<br>
      Tweet: “Inshallah if I do become a doc and if I leave this country ...I will come back to serve my motherland which made me a doctor  by the free education given from grade 1 to uni, the amazing teaching in the university and a valuable degree which I can proudly hold on to Inshallah”<br>
      Label: Realistic Hope<br>
      Tweet: “I wish my bf were less attractive to me like how am I supposed to stay mad”<br>
      Label: Unrealistic Hope<br>
      </P>
  - **one-shot_2b_Spanish: one demonstration for Spanish data in subtask 2b.** It is similar to one-shot_2b_English, however, the tweet is in Spanish.
  - **three-shot_2b_English: three demonstrations for English data in subtask 2b.** It is similar to one-shot_2b_English, however, the number of demonstrations in each class is three.
  - **three-shot_2b_Spanish: three demonstrations for Spanish data in subtask 2b.** It is similar to one-shot_2b_Spanish, however, the number of demonstrations in each class is three.

In bellow tabel we show our detail syntax for final prompting in three techniques Zero-shot, One-shot and Chain of thought with 6 strategy for task 1, and subtask 2a in English. Three-shot prompting, subtask 2b in English, and Task 2 in Spanish are not presented in this table. But it's easy to deduce based on the pre-defined variables and syntax we've provided.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax">Technique</th>
    <th class="tg-0lax">Instruction</th>
    <th class="tg-0lax">task 1</th>
    <th class="tg-0lax">Subtask 2a English</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax" rowspan="6">Zero-shot</td>
    <td class="tg-0lax">strategy 1</td>
    <td class="tg-0lax">&lt;request_1&gt;<br>&lt;normal answer format&gt;</td>
    <td class="tg-0lax">&lt;request_2a&gt;<br>&lt;normal answer format&gt;</td>
  </tr>
  <tr>
    <td class="tg-0lax">strategy 2</td>
    <td class="tg-0lax">&lt;concept_1&gt;&lt;request_1&gt;<br>&lt;normal answer format&gt;</td>
    <td class="tg-0lax">&lt;concept_2&gt;&lt;request_2a&gt;<br>&lt;normal answer format&gt;</td>
  </tr>
  <tr>
    <td class="tg-0lax">strategy 3</td>
    <td class="tg-0lax">&lt;class_1&gt;<br>&lt;request_1&gt;<br>&lt;normal answer format&gt;</td>
    <td class="tg-0lax">&lt;class_2a&gt;<br>&lt;request_2a&gt;<br>&lt;normal answer format&gt;</td>
  </tr>
  <tr>
    <td class="tg-0lax">strategy 4</td>
    <td class="tg-0lax">&lt;role&gt;&lt;request_1&gt;<br>&lt;normal answer format&gt;</td>
    <td class="tg-0lax">&lt;role&gt;&lt;request_2a&gt;<br>&lt;normal answer format&gt;</td>
  </tr>
  <tr>
    <td class="tg-0lax">strategy 5</td>
    <td class="tg-0lax">&lt;concept_1&gt;<br>&lt;class_1&gt;<br>&lt;request_1&gt;<br>&lt;normal answer format&gt;</td>
    <td class="tg-0lax">&lt;concept_2&gt;<br>&lt;class_2a&gt;<br>&lt;request_2a&gt;<br>&lt;normal answer format&gt;</td>
  </tr>
  <tr>
    <td class="tg-0lax">strategy 6</td>
    <td class="tg-0lax">&lt;role&gt;&lt;concept_1&gt;<br>&lt;class_1&gt;<br>&lt;request_1&gt;<br>&lt;normal answer format&gt;</td>
    <td class="tg-0lax">&lt;role&gt;&lt;concept_2&gt;<br>&lt;class_2a&gt;<br>&lt;request_2a&gt;<br>&lt;normal answer format&gt;</td>
  </tr>
  <tr>
    <td class="tg-0lax" rowspan="6">One-shot</td>
    <td class="tg-0lax">strategy 1</td>
    <td class="tg-0lax">&lt;request_1&gt;<br>&lt;one-shot_1&gt;<br>&lt;normal answer format&gt;</td>
    <td class="tg-0lax">&lt;request_2a&gt;<br>&lt;one-shot_2a_English&gt;<br>&lt;normal answer format&gt;</td>
  </tr>
  <tr>
    <td class="tg-0lax">strategy 2</td>
    <td class="tg-0lax">&lt;concept_1&gt;&lt;request_1&gt;<br>&lt;one-shot_1&gt;<br>&lt;normal answer format&gt;</td>
    <td class="tg-0lax">&lt;concept_2&gt;&lt;request_2a&gt;<br>&lt;one-shot_2a_English&gt;<br>&lt;normal answer format&gt;</td>
  </tr>
  <tr>
    <td class="tg-0lax">strategy 3</td>
    <td class="tg-0lax">&lt;class_1&gt;<br>&lt;request_1&gt;<br>&lt;one-shot_1&gt;<br>&lt;normal answer format&gt;</td>
    <td class="tg-0lax">&lt;class_2a&gt;<br>&lt;request_2a&gt;<br>&lt;one-shot_2a_English&gt;<br>&lt;normal answer format&gt;</td>
  </tr>
  <tr>
    <td class="tg-0lax">strategy 4</td>
    <td class="tg-0lax">&lt;role&gt;&lt;request_1&gt;<br>&lt;one-shot_1&gt;<br>&lt;normal answer format&gt;</td>
    <td class="tg-0lax">&lt;role&gt;&lt;request_2a&gt;<br>&lt;one-shot_2a_English&gt;<br>&lt;normal answer format&gt;</td>
  </tr>
  <tr>
    <td class="tg-0lax">strategy 5</td>
    <td class="tg-0lax">&lt;concept_1&gt;<br>&lt;class_1&gt;<br>&lt;request_1&gt;<br>&lt;one-shot_1&gt;<br>&lt;normal answer format&gt;</td>
    <td class="tg-0lax">&lt;concept_2&gt;<br>&lt;class_2a&gt;<br>&lt;request_2a&gt;<br>&lt;one-shot_2a_English&gt;<br>&lt;normal answer format&gt;</td>
  </tr>
  <tr>
    <td class="tg-0lax">strategy 6</td>
    <td class="tg-0lax">&lt;role&gt;&lt;concept_1&gt;<br>&lt;class_1&gt;<br>&lt;request_1&gt;<br>&lt;one-shot_1&gt;<br>&lt;normal answer format&gt;</td>
    <td class="tg-0lax">&lt;role&gt;&lt;concept_2&gt;<br>&lt;class_2a&gt;<br>&lt;request_2a&gt;<br>&lt;one-shot_2a_English&gt;<br>&lt;normal answer format&gt;</td>
  </tr>
  <tr>
    <td class="tg-0lax" rowspan="6">CoT</td>
    <td class="tg-0lax">strategy 1</td>
    <td class="tg-0lax">&lt;request_CoT_1&gt;<br>&lt;CoT answer format&gt;</td>
    <td class="tg-0lax">&lt;request_CoT_2a&gt;<br>&lt;CoT answer format&gt;</td>
  </tr>
  <tr>
    <td class="tg-0lax">strategy 2</td>
    <td class="tg-0lax">&lt;concept_1&gt;&lt;request_CoT_1&gt;<br>&lt;CoT answer format&gt;</td>
    <td class="tg-0lax">&lt;concept_2&gt;&lt;request_CoT_2a&gt;<br>&lt;CoT answer format&gt;</td>
  </tr>
  <tr>
    <td class="tg-0lax">strategy 3</td>
    <td class="tg-0lax">&lt;class_1&gt;<br>&lt;request_CoT_1&gt;<br>&lt;CoT answer format&gt;</td>
    <td class="tg-0lax">&lt;class_2a&gt;<br>&lt;request_CoT_2a&gt;<br>&lt;CoT answer format&gt;</td>
  </tr>
  <tr>
    <td class="tg-0lax">strategy 4</td>
    <td class="tg-0lax">&lt;role&gt;&lt;request_CoT_1&gt;<br>&lt;CoT answer format&gt;</td>
    <td class="tg-0lax">&lt;role&gt;&lt;request_2a&gt;<br>&lt;CoT answer format&gt;</td>
  </tr>
  <tr>
    <td class="tg-0lax">strategy 5</td>
    <td class="tg-0lax">&lt;concept_1&gt;<br>&lt;class_1&gt;<br>&lt;request_CoT_1&gt;<br>&lt;CoT answer format&gt;</td>
    <td class="tg-0lax">&lt;concept_2&gt;<br>&lt;class_2a&gt;<br>&lt;request_CoT_2a&gt;<br>&lt;CoT answer format&gt;</td>
  </tr>
  <tr>
    <td class="tg-0lax">strategy 6</td>
    <td class="tg-0lax">&lt;role&gt;&lt;concept_1&gt;<br>&lt;class_1&gt;<br>&lt;request_CoT_1&gt;<br>&lt;CoT answer format&gt;</td>
    <td class="tg-0lax">&lt;role&gt;&lt;concept_2&gt;<br>&lt;class_2a&gt;<br>&lt;request_CoT_2a&gt;<br>&lt;CoT answer format&gt;</td>
  </tr>
</tbody>
</table>
