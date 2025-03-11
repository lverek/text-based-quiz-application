# text-based-quiz-application
The application will ask the user a series of questions and then provide a score at the end.
class Quiz:
    def __init__(self):
        self.questions = []
        self.score = 0

    def add_question(self, question, answer):
        self.questions.append({'question': question, 'answer': answer})

    def start(self):
        for question in self.questions:
            print(question['question'])
            user_answer = input("Your answer: ")
            if user_answer.lower() == question['answer'].lower():
                self.score += 1
                print("Correct!\n")
            else:
                print(f"Wrong! The correct answer is {question['answer']}.\n")

        print(f"Quiz finished! Your score is {self.score}/{len(self.questions)}")

if __name__ == "__main__":
    quiz = Quiz()
    quiz.add_question("What is the capital of France?", "Paris")
    quiz.add_question("What is 2 + 2?", "4")
    quiz.add_question("Who wrote 'To Kill a Mockingbird'?", "Harper Lee")
    quiz.add_question("What is the largest planet in our solar system?", "Jupiter")

    quiz.start()
How it works:
Class Initialization: The Quiz class initializes with an empty list of questions and a score of 0.
Adding Questions: The add_question method allows adding questions and their corresponding answers to the quiz.
Starting the Quiz: The start method runs through all the questions, prompts the user for an answer, checks if it's correct, updates the score, and provides feedback.
Main Program: The if __name__ == "__main__": block creates an instance of the Quiz class, adds some questions, and starts the quiz.
13579
