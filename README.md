1.	The purpose of the app
It is to help the user to have an idea on what to eat each time of a day whether in the morning, lunch or even dinner. The app has pre-planned options in which the user can use for meal suggestions and meal decision making. The app offers a quick and easy meal ideas for a user that is always busy. (Douglas 2018).
2.	Design considerations.
Simplicity
The app does not need long sign-ups, there’s just basic preferences. The user gets meals recommendations based on which time of the day is it. The app has a clean design with a search box for the user time of the day meal. I applied my simplicity by using a simple layout on images and meal names. I avoided unnecessary text on each screen. (Buley and Natoli 2024).
Consistency.
The app has clear colours, fonts and buttons. The app ensures features behave predictably across different screens. The words on the app have good spacing, margins and image sizes are standardized. I applied my consistency by choosing readable fonts and the app buttons texts elements are evenly spaced. (Durgekar, Rahman, Naik, Kanchan and Srinivasan 2024).
Readability.
Legible fonts were used and consistent font size was also used for my app name. The app buttons and layout stand with enough contrast. I applied my readability by avoiding decorations. The app name font is large for easy scanning. (Perez Vidal-Ribas 2023).
Feedback.
The app provides feedback when user enters the time of the day meal on the search box. (Toaha 2024). 
Placement.
The box to search for the time of the day meal will be provided under the image. The response for the time of the day meal should be listed underneath the search box for the time of the day meal. At the bottom of the app there’s a reset button and the show meal button. I applied my placement by inserting two navigation bars in which there’s the reset and show meal button at the bottom for easy thumb access. (Bigham, Jayant, Little, Miller, Miller, Miller, Tatarowicz, White, White, and Yeh 2010, October.)















3.	The design of the app.
 

Explaining how the app works.
We will firstly enter my food app which is FoodEducate. After opening the app, the screen will show the app name, image which refers to the purpose of the app and under the pic there’s a quote that says “See how you eat”. Underneath the quote there’s a search box for the time of the day meal then follows the answer for the text typed on the search box. At the bottom there’s then two buttons which are named reset and show meal. On the search box when searching for a meal on a certain time of the day, the user has to insert the time of the day formally (9 a.m. morning). After entering the time of the day “morning” in the search box underneath it you will then have an answer for what the user has entered in the search box. (Tan 2024.)

 
 
 
 
 
 







4.	GitHub link
https://github.com/VCPTA/hmaw1-imad5112-assignment-1-ST10494404.git


5.	YouTube link 
https://youtu.be/L5UH_3vrmoE

6.	Copy of my code.
7.	package vcmsa.ci.foodeducate
import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import android.widget.Toast
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        // Initialize UI elements
        val timeOfDayEditText: EditText = findViewById(R.id.timeOfDayEditText)
        val showMealButton: Button = findViewById(R.id.showMealButton)
        val resetButton: Button = findViewById(R.id.resetButton)
        val mealSuggestionsTextView: TextView = findViewById(R.id.mealSuggestionsTextView)

        // Show meal suggestions when button is clicked
        showMealButton.setOnClickListener {
            val timeOfDay = timeOfDayEditText.text.toString().trim()

            if (timeOfDay.isEmpty()) {
                // Show a Toast if no time of day is entered
                Toast.makeText(this, "Please enter a time of day", Toast.LENGTH_SHORT).show()
            } else {
                // Display meal suggestions based on the time of day
                val mealSuggestions = when (timeOfDay.lowercase()) {
                    "morning" -> {
                        "Breakfast: Scrambled Eggs and Toast\nOatmeal with Fruits"
                    }
                    "mid-morning" -> {
                        "Snack: Yogurt and Granola\nFruit Smoothie"
                    }
                    "afternoon" -> {
                        "Lunch: Grilled Chicken Salad\nVegetable Stir-fry"
                    }
                    "mid-afternoon" -> {
                        "Snack: Nuts and Berries\nCheese and Crackers"
                    }
                    "dinner" -> {
                        "Dinner: Spaghetti with Marinara Sauce\nGrilled Salmon with Veggies"
                    }
                    "after dinner" -> {
                        "Dessert: Chocolate Cake\nFruit Salad"
                    }
                    else -> {
                        "Invalid time of day. Please enter a valid time."
                    }
                }

                // Show the meal suggestions in the TextView
                mealSuggestionsTextView.text = mealSuggestions
            }
        }

        // Reset the input and suggestions when reset button is clicked
        resetButton.setOnClickListener {
            timeOfDayEditText.text.clear()
            mealSuggestionsTextView.text = ""
        }
    }
}















8.	References.
Douglas 2018. Deciphering a meal. In Food and culture (pp. 29-47). Routledge.
Buley and Natoli 2024. The user experience team of one: A research and design survival guide. Rosenfeld Media.
Durgekar Rahman, Naik, Kanchan and Srinivasan 2024. A Review Paper on Design and Experience of Mobile Applications. EAI Endorsed Transactions on Scalable Information Systems, 11(3).
Perez Vidal-Ribas 2023. Effects of Font Design on Highway Sign Legibility (Doctoral dissertation, Virginia Tech).
Toaha 2024. Log your eating habits (Master's thesis, Oslo Metropolitan University).
Bigham, Jayant, Ji, Little, Miller, Miller, Miller, Tatarowicz, White, White and Yeh 2010, October. Vizwiz: nearly real-time answers to visual questions. In Proceedings of the 23nd annual ACM symposium on User interface software and technology (pp. 333-342).
Tan 2024. Mobile application for real-time food image segmentation and nutritional guidance at grocery store (Doctoral dissertation, UTAR).




