# Exno.7-Develop a prompt-based application tailored to their personal needs, fostering creativity and practical problem-solving skills while leveraging the capabilities of large language models.

# Date:14/10/25
# Register no:212223040034
# NAME :DHANUSHA K
# Aim: To develop a prompt-based application using ChatGPT - To demonstrate how to create a prompt-based application to organize daily tasks, showing the progression from simple to more advanced prompt designs and their corresponding outputs.

# AI Tools Required: 
ChatGPT (OpenAI LLM, simulated via prompt engineering)

# Explanation: 
Prompt:
"Design a personal productivity assistant that can help manage daily tasks, schedule reminders, suggest wellness tips, and answer general queries. The assistant should interact using natural language and be adaptable to the user’s changing preferences over time."
Procedure:
1. Define the core requirements of a personal productivity assistant.
2. Identify and construct appropriate prompts for each task using an LLM (e.g., ChatGPT).
3. Simulate natural user interaction through a simple interface or command-line system.
4. Collect feedback or inputs from users and adapt responses accordingly.
5. (Optional) Integrate basic memory to simulate preference adaptation.
EXPECTED OUTPUT: - (attached the drive link)
Output (Example Response by LLM):
Personal Productivity Assistant Features:
1. Daily Task Manager:
o Accept tasks via natural language (e.g., "Remind me to call mom at 6 PM").
o Organize tasks by priority and deadline.
o Provide daily summaries and pending items.
2. Smart Scheduler:
o Schedule events and set reminders using contextual understanding.
o Notify user of overlapping appointments or free time slots.
3. Wellness Tips Generator:
o Suggest daily wellness advice (hydration, exercise, screen-time breaks).
o Adapt suggestions based on past user preferences and responses.
# Personal Productivity Assistant Features
# 1. Core Requirements & Simple Prompts
# a. Daily Task Manager
# Prompt Example:

"Extract task, time, and priority from: '[User Input]'. Respond in JSON with keys: task, time, priority (high/medium/low)."
# User Input:
"Remind me to call Mom at 6 PM."
Output:
```
{
  "task": "Call Mom",
  "time": "18:00",
  "priority": "medium"
}
```
<img width="595" height="180" alt="image" src="https://github.com/user-attachments/assets/1ad543b6-9e3e-430e-81ce-5c12438363e7" />

# b. Smart Scheduler
# Prompt Example:
"Check if '[new event time]' conflicts with existing events: [existing events]. Respond with 'Conflict: Yes/No' and a summary."
# User Input:
"Schedule a meeting at 3 PM tomorrow."
# Output:
```
"No conflict. Added 'Meeting' at 15:00 tomorrow."
```
# c. Wellness Tips Generator
# Prompt Example:
"Suggest a wellness tip from: hydration, stretching, screen breaks. Avoid: [user disliked tips]."
# Output:
```
"Tip: Take a 5-minute screen break every hour to reduce eye strain!"
```
## 2. Intermediate: Contextual Understanding
# a. Conflict Detection
# Prompt Example:
"User input: '[event request]'. Existing events: [list]. Identify overlaps and respond with a warning if conflicts exist."
# User Input:
"Add yoga class at 5 PM today."
# Output:
" Warning: Conflicts with 'Team Meeting' (17:00–18:00). Reschedule?"
# b. Priority-Based Task Sorting
# Prompt Example:
"Sort tasks by priority (high > medium > low): [task list]. Format as a numbered list."
# Output (Markdown Style):
```
1. [High] Submit report by 17:00  
2. [Medium] Call Mom at 18:00  
3. [Low] Buy groceries  
```
# 3. Advanced: Adaptive Memory & Natural Interaction
# a. Wellness Tips with Memory
# Prompt Example:
"User previously disliked 'hydration' tips. Suggest a new tip. Options: meditation, walking, ergonomics."
# Output:
```
"How about a 10-minute walk? It boosts energy and focus!"
```
# b. User Preference Adaptation
```
Simulated Memory (JSON):

{
  "disliked_tips": ["hydration"],
  "preferred_time": "morning"
}
```
# Prompt Example:
"Generate a morning wellness tip based on user preferences: [memory]."
# Output:
```
"Start your day with 5 minutes of meditation!"
```
# c. Natural Language Interaction
# Prompt Example:
"Respond conversationally to the user's task list request: [tasks]."
# User Input:
"What’s on my schedule today?"
# Output:
```
"Here’s your day:
10:00 AM: Project meeting (high priority)
3:00 PM: Email clients (medium)
7:00 PM: Gym (low)
Need adjustments?"*
```
# 4. Optional: Feedback Loop & Interface Simulation
Feedback Collection Logic:
After each response, assistant asks:
```
“Was this helpful? (Yes/No)”
```
If “No”:
```
“Noted! I’ll adjust future suggestions.”
```
🖥️ Command-Line Simulation (Python Pseudocode):
```
while True:
    user_input = input("You: ")
    if "add task" in user_input:
        # Trigger task manager prompt
    elif "wellness tip" in user_input:
        # Fetch tip from memory-adapted prompt
    # ... other actions
```
# Expected Output Example
<img width="444" height="224" alt="image" src="https://github.com/user-attachments/assets/dc3d3322-973e-40f0-be97-c23d7ec15623" />

# User Input:
"Plan a blog draft and a dentist appointment at 2 PM tomorrow."
# Assistant Response:
```
{
  "tasks": [
    { "task": "Write blog draft", "time": "Flexible", "priority": "high" },
    { "task": "Dentist appointment", "time": "14:00", "priority": "medium" }
  ],
  "summary": "Added 2 tasks. No schedule conflicts detected!"
}
```
# User Input:
"What wellness tip do you recommend?"
# Assistant (Adaptive):
"Since you enjoy fresh air: Take a walk outside for 10 minutes!"

# Result: 
The lab exercise resulted in the creation of a prototype concept for a personal assistant powered by large language models. Students were able to:
 Understand how to tailor LLM prompts to real-life applications.
 Foster creativity by designing features suited to their personal or academic lives.
 Learn prompt engineering techniques for optimal interaction with AI tools.
 Experience the versatility and utility of generative AI in solving everyday problems.
