# Kitchen_Master

### Implemented in this project:
- Intent
- BroadcastReceiver
- Animation
- Database

### Abstract:
Kitchen Master is a Quiz App with fun easy Kitchen questions for cooking lovers which also stores the score. The application works on any android device.

### STEPS OF THIS PROJECT:

Step1: Create a new project.

Step2: Take another theme called MyApp with parent no action bar and in AndroidManifest.xml file put the theme inside activity MyApp and keep orientation to portrait.
            Add plugins kotlin-android-extensions

Step3: In activity_main.xml design UI:
	In Linear Layout,
	After adding a gradient image in drawable for background
	Firstly, take a textview with Heading of Quiz App
	Secondly, 2 textviews that display Welcome and Enter your name respectively in a cardview.
	Then a Textinput Layout which contains edit Text to enter your name.
	Then a button that displays Next to go on next activity in the same cardview.
	Import material UI in dependencies of build.gradle module for better designing options.
	Lastly put Windowsoftinputmode to adjustResize means when keyboard appears it will adjust itself  and will not hide the cardview. Its one type of animation.

Step4: Create a QuestionActivity.kt file
	Now in activity_question.xml file,
		In a linear Layout,
		take 4 textviews which contains a question and 4 options of the quiz.
		Create a drawable question_option for options background and take a submit button.
		Then after the first textview take a  progressbar and a textview in a linear layout.
	
Step4 : Now create a kotlin class file QuestionData.kt to set questions
	In which take 4 properties for question, id, four options and correct answer.
             Create another Kotlin file setData.kt to set the data (object)
	Create a fun which returns question data in a Array list, now create objects for different questions and set data in it.
	Then call and fetch setData in QuestionActivity.kt file

Step5: In MainActivity.kt file,
	Creater fun to ensure that before clicking the next button user had written a name and then intent it to QuestionActivity.

Step6 : In QuestionActivity.kt file 
	Firstly, create 3 new drawables for button background for selected right and wrong answers.
	Here using functions progress bar will increase with next question and also questions values are set from setData.kt file.
	When user selects an option and submits it, it will show the right and wrong answers with green and red colour resp. And show the Go to next button.

Step 7 : Create Result.kt file
	In activity_result.xml file,
	In linear layout create a cardview, and then 3 textviews and a button for name score and finish.

Step 8 :  In Result.kt file
	Fetch name from the firts page in MainActivity. Created 2 variables name and score in setdata.kt file to show name and score on last activity.
	On clicking finish button data is stored using shared prefrences.

Step 9 : Create CallReceiver.kt file for incoming call while using the App using broadcast receiver.
	And add permissions and CallReceiver code to manifest file.
	
