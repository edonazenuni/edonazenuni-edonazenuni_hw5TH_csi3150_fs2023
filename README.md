# edonazenuni-edonazenuni_hw5TH_csi3150_fs2023

Problem Statement: The quiz app is a simple app that is comprised of five questions that users must answer within a certain time frame. The correct answers are highlighted in green, and the wrong answers are highlighted in red. The app will evaluate the user’s responses and provide a score based on the correct number of answers.


Functional Features:

-	Quiz with 5 simple programming language name questions.
-	Time constraint for each question.
-	Instant feedback on user response (green = correct, red = wrong).
-	Score calculation of the final score based on correct answers.
-	Restriction on undoing a selected answer.
-	Users may exit and restart the quiz.
-	

Directory Structure:

Index.html: The main HTML file. Entry point for application. Holds the quiz box, information box, and result box. It’s connected to the CSS and JavaScript files to provide interactivity.
CSS/Style.css: This file is responsible for all the styling, visual appearance, and layout of the application. 
Js/Questions.js: This file holds the array of questions consisting of the question number, question, answer, and options. Populates the quiz box in index.html with the question-and-answer options.
Js/quizApp.js: This file holds the main functionality of the quiz application. This file interacts with elements in the HTML file and includes the timer, user inputs, and final score calculations.

Codebase Explanation: 
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Index.html: 

<div class="info-title"><span>Some Rules of this Quiz</span></div>
<div class="info-list">
    <div class="info">1. You will have only <span>15 seconds</span> per each question.</div>
    <div class="info">2. Once you select your answer, it can't be undone.</div>
    <div class="info">3. You can't select any option once time goes off.</div>
    <div class="info">4. You can't exit from the Quiz while you're playing.</div>
    <div class="info">5. You'll get points on the basis of your correct answers.</div>
</div>

This section informs the user about the specific rules that apply to the quiz.

<div class="start_btn"><button>Start Quiz</button></div>

The <div class="start_btn"> element represents the button container for starting the quiz.

<div class="quiz_box">
    <!-- ... -->
</div>

The <div class="quiz_box"> element serves as the container for the main quiz interface and functionality.
Inside this div are elements that facilitate the quiz experience, including question display, options for each question and a timer.

</div>

<!-- Result Box -->
<div class="result_box">
    <!-- ... -->
</div>

The result_box section is responsible for displaying the user's final score.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Style.css:


.start_btn,
.info_box,
.quiz_box,
.result_box {
}

These sections style the start button, information box, quiz box, and result box.

.info_box {
}

.info_box .info-title {
}

.info_box .info-list {
}

Styling for the information box including title and list

.info_box .buttons {
}

.info_box .buttons button {
}

.quiz_box {
}

.quiz_box header {
}

These sections style the buttons inside the information box, the quiz box, and header in the quiz box.

section .que_text {
}

section .option_list {
}

section .option_list .option {
}

Styling for the question test and option list within the quiz box

section .option_list .option:last-child {
}

section .option_list .option:hover {
}

section .option_list .option.correct {
}

section .option_list .option.incorrect {
}

section .option_list .option.disabled {
}

Styling for the options that are correct, incorrect, and disabled options within the option list.


section .option_list .option .icon {
}

.option_list .option .icon.tick {
}

.option_list .option .icon.cross {
}

footer {
}

footer .total_que span {
}

More styling for the options including the tick icon, cross icon, footer section, and span elements.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

quizApp.js
1.	Variable Initialization:
•	The variables timeValue, que_count, que_numb, userScore, counter, counterLine, and widthValue are initialized. These variables are crucial for managing the quiz's functionality and state.
2.	Restart Quiz Event Listener:
•	Identified in the restart_quiz event listener, the function resets several key parameters to their initial values. This ensures that the quiz can be restarted from the beginning, clearing any previous progress and resetting the timers.
3.	Quit Quiz Event Listener:
•	The quit_quiz event listener, this function reloads the current page. This allows the user to exit the quiz entirely and start over if needed.
4.	Next Question Event Listener:
•	The next_btn event listener, this section checks if the quiz has reached the maximum number of questions. If not, it progresses to the next question, updating the question count and number. If the quiz has reached the maximum number of questions, it stops the timers and displays the final result.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

questions.js
1.	Question Data:
•	The file contains an array named questions, which stores a list of objects, each representing a quiz question. Each question object contains properties such as the question number (numb), the question itself (question), answer options (options), and the correct answer (answer).
2.	Question Structure:
•	Each question object has a unique identification number (numb), a question (question), an array of answer options (options), and the correct answer (answer). This structured representation enables the quiz app to access and present the questions and answer options to the user. 
