# Objection Handler

This is a quiz app built with React Native that reads questions from a CSV, and provides a quiz to the user.

It will allow you to select which 'product' you want to quiz on at the home screen, and then proceed to the quiz itself.

The quiz is composed of 3 types of questions, and each question will typically have 9 variations (also in the CSV).

Upon getting a question wrong, your sent to the beginning of the quiz again. When you've got all questions complete, your accuracy on each question is given to you.

## Experimental Ideas

This is being built as a way to test and experiment with a couple different ideas.

- Applying Elm Architecture ideas to React
- Documentation driven development
- Test Driven Development

## Elm Ideas + Documentation Driven Development

Documentation driven development means that before developing any component, I first write the documentation for what it will do. The documentation itself will heavily rely on ideas around Data Models, what Messages can be triggered, and how those Messages transform the corresponding data model.

One specific thing being explored is what happens if I model things as Algebraic data types in the documentation, but drop down to using JS-compatible data types in the application itself. Will the gap between the Algebraic data types from functional languages and the actual implementation details cause issues, or will it lead to better clarity despite the differences?
