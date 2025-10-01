# cse535_project1
Android App - Context Monitoring
Raja Aravind Reddy Manimala
1233152507
Generative AI Acknowledgment: Portions of the code in this project were generated with assistance from ChatGPT, an AI tool developed by OpenAI. 
Reference: OpenAI. (2024). ChatGPT [Large language model]. openai.com/chatgpt
* Estimated percentage of code influenced by Generative AI: ~10% (Also including the XML files for activity_symptoms.xml)

# Generative AI Used: ChatGPT (OpenAI, September 24, 2025)
# Purpose: Needed help writing a spinner for drop down
# Prompt: "How to create a dropdown for the symptoms for the user to choose from [list of symptoms]"

val adapter = ArrayAdapter(this, android.R.layout.simple_spinner_item, symptoms)
        adapter.setDropDownViewResource(android.R.layout.simple_spinner_dropdown_item)
        symptomSpinner.adapter = adapter
addSymptomBtn.setOnClickListener {
            val selectedSymptom = symptomSpinner.selectedItem.toString()
            val rating = ratingSeekBar.progress
            symptomRatings[selectedSymptom] = rating
            updateSymptomsDisplay(symptomsListText)
            Toast.makeText(this, "Added $selectedSymptom with rating $rating", Toast.LENGTH_SHORT).show()
        }


1) Writing thousands of lines of code for sensors and smartphones, especially when your knowledge of programming is limited feels almost impossible. That’s where Health-Dev comes into play, a framework that helps people automatically generate code for health monitoring systems. Instead of writing the code from scratch, we just need to give Health-Dev the right specifications, and it will build the system.
To use Health-Dev, the first thing to do is to provide the sensor specifications. This means telling the framework what kind of sensors the app will use. For example, if one wants to measure heart rate, one would pick an ECG sensor. If one wants temperature or humidity, they would pick those corresponding sensors. We also need to specify how often the sensor collects data, what platform it runs on (like Shimmer or Arduino), and which algorithms should be used to process the signals. Health-Dev already has a library of algorithms, like peak detection for ECG or correlation for temperature and humidity.
Next, we would have to describe the network specifications. This part is about how the sensors talk to each other and to the smartphone. We could choose if they connect directly or if the data hops through other sensors, and whether they use Bluetooth or ZigBee to communicate. We also need to say how the sensors save energy, for example, keeping the radio on all the time or only turning it on when needed.
Finally, we must specify the smartphone application. This includes how the app looks and what features it has. For example, we could design buttons like “Start” and “Stop,” text fields to show values such as heart rate or temperature, and graphs to display ECG signals. we could also set commands for the phone to send back to the sensors, like telling them to change their sampling frequency. Since Health-Dev currently works with Android, all of these settings would be translated into real Android code without having to write it by hand.
By giving Health-Dev these three kinds of information: sensor specifications, network specifications, and smartphone specifications, we can get a working application even without being a great programmer. This makes it possible for beginners to bring ideas to life. Instead of struggling with complicated code, one can focus on the design and purpose of an app, while Health-Dev takes care of the technical part.
In conclusion, Health-Dev is like a bridge between our imagination and actual software. All we need to do is describe what sensors are required, how they should connect, and what the app should look like. With that, the framework can create the code automatically. For someone who dreams of building useful technology but doesn’t yet have strong coding skills, this is a perfect way to get started.


2) In Project 1, we stored different symptoms that the user was experiencing, like nausea, diarrhea, and weakness, into a local server. This was an important step because it allowed us to collect health data in one place. But just storing the data is not enough. If we actually want to help the user feel better, we need to take that information and turn it into feedback that makes sense to them. That’s where the bHealthy application suite can be really useful.
bHealthy is a mobile wellness system that uses special sensors and apps to monitor the body and the mind. For example, it can use heart sensors, brain sensors, and even motion sensors to understand the user’s current state, like if they are stressed, tired, or active. Once it knows this, bHealthy doesn’t just stop at collecting data. It also gives suggestions about what remedies the user should try, such as exercising with the PETPeeves app or improving focus and relaxation with the BrainHealth app. These apps also track how the user performs over time and generate a wellness report that the user can see and understand.
To connect Project 1 with bHealthy, we can combine the symptoms we already saved with the physiological data that bHealthy provides. For example, if a user reports nausea and weakness, bHealthy could check their heart rate or brain activity to see if stress is making things worse. Then, it could suggest specific activities, like relaxation training through BrainHealth, or light walking through PETPeeves. This way, the system is not only reacting to the symptoms the user is feeling but also sensing what is happening in real time.
A new application we could design using this system would be a Symptom-to-Remedy Mapper. This app would take the stored symptoms (from Project 1) and combine them with the user’s live sensor data from bHealthy. Using both pieces of information, the app would suggest the best activity for the user and track how their symptoms change over time. For example, if the user had diarrhea and stress, the app might suggest calming exercises. If the user felt weak but showed no stress, it might suggest light movement or rest. Over time, the app would build a model of the user’s health patterns, showing what symptoms happen most often and what activities actually help them.
By putting Project 1 and bHealthy together, we move from just recording health problems to providing personalized feedback. This not only makes the system more helpful but also makes the user feel supported in improving their wellness every day.


3) At first, I used to think that mobile computing was mostly about app development. Whenever I heard the words “mobile computing,” I pictured people building apps for smartphones, like games, social media, or health trackers. That seemed to be the whole story. But after working on Project 1 and reading the papers about Health-Dev and bHealthy, my views have definitely changed.
Now I understand that mobile computing is much bigger than just making apps. It’s actually about connecting many pieces together, like sensors, data collection, analysis, and feedback, all through mobile devices. For example, in Project 1 we stored users’ symptoms, such as nausea, diarrhea, and weakness, on a local server. At first that felt like app development because we were building something simple that collected data. But when I read about bHealthy, I realized that mobile computing also includes using physiological sensors like heart and brain monitors to figure out the user’s real-time condition. Then, the system suggests activities and even gives wellness reports. That’s way more than just making an app, it’s creating an entire system that learns about the user and helps improve their life.
I think mobile computing is about designing smart, context-aware systems that make use of all the technology built into or connected to our phones. For example, a fitness app that counts steps is not just “an app.” It uses accelerometer sensors, GPS, and health models to understand your activity. Similarly, the PETPeeves app in bHealthy isn’t only about software, it combines data from heart sensors and movement to motivate people to exercise by keeping a virtual pet happy.
So, my views have changed. Mobile computing is not just about coding apps, it’s about using phones as powerful tools that combine sensors, networks, and data to give people real-time help in their daily lives. That’s what makes it so exciting and important.
