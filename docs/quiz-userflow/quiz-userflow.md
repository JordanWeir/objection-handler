## Product Training Quiz

First a quick instructions screen is shown. The click Continue to continue.

Next the first quiz question is shown. The quiz itself has 3 stages.

In the first part, it is 'recognition' style quiz questions. Recognition concepts are Multiple Choice, and meant to be relatively easy. Do you recognize the concept in front of you?

In the second part, it is 'hybrid' style quiz questions. Given a list of ideas on the left, and a list of names on the right, can you link the correct ideas to the correct names?

In the third part, it is a 'recall' exercise. Given a scenario, can you get the correct answer without a direct prompt? This would be typing in the answer, or similar.

Product Training Quiz Flow

- Quiz Intro Screen
- Quiz Recognition Intro Screen
- Quiz Recognition Questions
- Quiz Hybrid Intro
- Quiz Hybrid Questions
- Quiz Hybrid Questions Results
- Quiz Recall Intro
- Quiz Recall Question
- Quiz Results

## Product Training Business Rules

Each concept has a set of 9 questions, with 3 types, and 3 versions/type.

Recognition 1/2/3 - These are slightly different Multiple Choice questions that capture the same concept.
Hybrid 1/2/3 - These are slightly different pairings that can be shown that capture the same concept.
Recall 1/2/3 - These are slightly different questions they can answer with the response to capture the concept.

If they get a question wrong at any point, we want to show a different version of that next time. If they get it wrong at the Hybrid or Recall stage, we'll show the next version of that concept at a level of difficulty one less. eg: They get Recognition 1 right, but hybrid 1 wrong, we can now show Recognition 2. If they've seen Recognition 1 and 2, and Hybrid 1 and 2, then a mistake on recall can show them Recognition 3 before testing recall again.

## Recognition Question Handling

- If an answer is correct, progress to next question
- If an answer is incorrect, handle based on the question stage (recognition, hybrid, recall)

Recognition incorrect handling: Visually indicate it as incorrect for a couple moments, then send them to beginning of Recognition section to repeat all questions again. When they arrive at the question they previously got incorrect, show next version of that question (3 versions of each question \* 3 types = 9 questions per concept).

If they get a question wrong 3 times, continue cycling through the different versions of that question starting from the first again.

## Hybrid Question Handling

Hybrid means they are linking a list of questions on the left to answers on the right.
For now, assume 5 at a time.

Go through all hybrid questions, not resetting on right or wrong answers, but saving the 'correct' or 'incorrect' status.

After all questions have been answered, correctly or incorrectly, let them know there score for the 'hybrid' section, and have 2 options. They can practice those as recognition, before returning to hybrid, or they can try hybrid again.

Practice as Recognition: Do a recognition round with the next recognition version of each of the concepts they got wrong. Then proceed to do Hybrid with the list of concepts, using the next variation of the hybrid question they got wrong.

Try Hybrid Again: Jump immediately to another Hybrid round with the next variation of the hybrid questions they got incorrect.

When they get all the Hybrid questions correct, proceed to Recall.

## Recall Question Handling

A question is asked, and they have to type in the answer. We have an array of 'acceptable' answers for each question. It's not clear yet if the 'acceptable' answers array should be the same for each of the 3 Recall questions in a set, or if they would be meaningfully different. It's tempting to say they should be the same, but that may not give us the flexibility we need to meet real world use cases.

## Screens

- Product Training Quiz
- Product Recognition Question
- Product Hybrid Question
- Product Hybrid Summary
- Product Recall Question
- Product Training Results Summary
