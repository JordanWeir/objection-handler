```
type QuestionStatus =
    | Incorrect
    | Correct
    | NotAttempted

type Question =
    | Recognition QuestionText QuestionStatus
    | Hybrid QuestionText QuestionStatus
    | Recall QuestionText QuestionStatus

type QuestionSet<T> = {
    answered: List Question<T>,
    active: Question<T>,
    upcoming: List Question<T>
}

type Concept = {
    recognition: QuestionSet<Recognition>,
    hybrid: QuestionSet<Hybrid>,
    recall: QuestionSet<Recall>
}

type Stage =
    | Recognition
    | Hybrid
    | HybridResults
    | Recall

type Model = {
    stage: Stage,
    answeredQuestions: List Concept
    activeQuestion: Concept
    upcomingQuestions: List Concept
}

type Msg =
    | AnsweredRecognitionCorrect
    | AnsweredRecognitionWrong
    | AnsweredHybridCorrect
    | AnsweredHybridWrong
    | ReturnToRecognitionFromHybrid
    | RetryHybrid
    | AnsweredRecallCorrect
    | AnsweredRecallWrong

```
