UNIT – IV (RPA / UiPath)
Full, simple, exam-ready answers — no formulas, easy terms, fully understandable


---

1) Describe how Assistant Bots are triggered by user events in UiPath with examples.

OR

Explain how Assistant Bots can be triggered by keyboard or mouse events with examples.

Assistant Bots in UiPath can start running whenever a user performs a specific action such as pressing a key, clicking a button, or selecting an option. These triggers help create attended automations, where the bot helps the user instantly when needed.

1. Keyboard Triggers

UiPath provides Keyboard Trigger activity that listens for a specific key or combination.

Example:

Press Ctrl + Shift + S → Bot starts saving all open invoices automatically.

Press F9 → Bot starts filling a form.


This is useful for tasks you do repeatedly and need to launch instantly.


---

2. Mouse Triggers

Bots can respond when the user clicks a UI element.

Example:

When the user clicks a “Search” button, the bot automatically reads data from the page and fills the result.

When the user right-clicks on a customer name, a bot pops up showing their full details.



---

3. UI Trigger Events

Bots watch for changes in applications.

Examples:

When a new email arrives, the bot starts processing attachments.

When a new row appears in an Excel file, the bot validates the data.



---

4. Taskbar / Assistant Triggers

Users can click buttons inside UiPath Assistant to run bots.

Example:

Clicking “Generate Report” in the Assistant starts a bot that collects data and prepares a daily report.



---

Conclusion:

Assistant Bots start working automatically based on keyboard actions, mouse clicks, UI changes, or buttons inside UiPath Assistant. This makes attended automation fast and user-friendly.


---

2) Explain the role of Exception Handling and Debugging techniques in maintaining reliable automation.

OR

Discuss the importance of Exception Handling and Logging in debugging UiPath processes.

Automation becomes reliable only when it can handle errors and diagnose issues properly.


---

A) Exception Handling in UiPath

Exception handling deals with unexpected errors, ensuring that the bot does not crash.

Why it is important:

1. Prevents bot failure when unexpected data or system issues occur.


2. Allows safe recovery, like retrying the action or using backup steps.


3. Improves stability, especially in real-time applications.


4. Helps track root causes of issues.



Techniques:

1. Try-Catch

Code inside Try is executed normally.

If an error occurs, Catch handles it gracefully.

Can show a message, log error, or retry the action.


2. Throw

Used when you want to raise a custom error.


3. Finally Block

Runs always (cleanup operations).


Example:
During file reading, if the file is missing → Catch block logs the issue and asks the user to re-provide file path.


---

B) Debugging Techniques

Debugging helps find where and why a workflow is failing.

1. Step Into / Step Over

Runs the workflow step by step to locate the problem.

2. Breakpoints

Pauses execution at specific points to inspect variable values.

3. Slow Step Mode

Runs the workflow slowly, making it easy to observe logic flow.

4. Immediate Panel & Locals Panel

Shows live values of variables during execution.


---

C) Logging

Logging records bot actions and errors for later review.

Importance of Logging:

1. Helps trace what happened before failure.


2. Useful for long-running processes.


3. Assists in debugging production-level robots.


4. Provides references for future improvements.



Types of Logs:

Info: General workflow information

Warning: Something unusual but not fatal

Error: When something fails

Trace: Detailed execution steps (for deeper debugging)



---

Conclusion:

Exception handling prevents crashes, logging records problems, and debugging helps identify the root cause. Together, they make UiPath automation stable, dependable, and easy to maintain.


---

3) Discuss debugging and logging techniques in automation.

Debugging and logging are essential for ensuring a bot works accurately.


---

A) Debugging Techniques in UiPath

1. Breakpoints

Pauses execution at a specific activity to inspect variables.

2. Step Into / Step Over

Allows you to run each line step-by-step to locate logical errors.

3. Slow Step Execution

Runs the workflow slowly so you can watch the execution path clearly.

4. Immediate Panel

Allows typing expressions during debugging to check values instantly.

5. Highlight Elements

Shows what element the bot is interacting with (helps in UI issues).

6. Analyze Errors

Gives details about missing arguments, wrong variable types, etc.


---

B) Logging Techniques in UiPath

Logging helps record and understand bot behavior.

1. Log Message Activity

Used to print messages like:

“Started reading Excel file”

“Customer ID not found”

“Process completed successfully”


2. Log Levels

Info – routine updates

Warning – unusual but not dangerous cases

Error – failures

Trace – deep technical logs


3. Orchestrator Logs

Centralized logs that help understand errors in production bots.

4. Screenshots

Bot can take screenshots when something goes wrong.

5. Execution Reports

Generated after a process is completed to summarize actions.


---

Conclusion:

Debugging identifies issues during development, while logging records run-time behavior. Both ensure smooth bot operation and easy troubleshooting.


---

4) Explain how to collect crash dumps and report errors in a bot project.

When a bot crashes, we need proper information to diagnose the cause.


---

1. Collecting Crash Dumps (Windows / UiPath)

A) Using Windows Error Reporting

When UiPath crashes, Windows automatically generates a crash dump.

Steps:

1. Go to C:\ProgramData\Microsoft\Windows\WER\ReportQueue


2. Look for .dmp or .wer files.


3. These contain detailed crash information.




---

B) Using UiPath Diagnostic Tool

UiPath provides a built-in tool:

1. Open UiPath Diagnostic Tool.


2. Select “Collect Logs”.


3. It gathers:

Crash dumps

Logs

System info



4. Export the generated zip file.




---

2. Reporting Errors in a Bot Project

A) Using Orchestrator

Errors automatically appear in Orchestrator Logs.
You can open a job → view Exception Details.

B) Using Log Message Activity

Log custom messages like:

“Excel file missing”

“Selector not found”


C) Using Global Exception Handler

Collects and reports errors before stopping the bot.

D) Email Alerts

Bot sends an email when an error occurs.

Example:
If a bot cannot find a UI element, it sends “Process failed – Element missing”.


---

Conclusion:

Crash dumps and error logs provide detailed technical information that helps developers understand failures and fix them quickly.


---

5) Demonstrate the use of Assistant Bots in UiPath.

Assistant Bots are attended robots that help users perform daily tasks quickly.


---

Examples of Using Assistant Bots

1. Data Entry Bot

User clicks “Fill Form” in UiPath Assistant →
Bot reads data from Excel → fills website form automatically.


---

2. Invoice Download Bot

User presses F7 →
Bot opens email → downloads invoice attachments → stores them in folders.


---

3. Report Generator Bot

User clicks “Generate Daily Report” in Assistant →
Bot collects information from Excel, ERP, website → creates PDF report.


---

4. Screenshot and Mail Bot

User presses Ctrl + F10 →
Bot takes screenshot of current screen → sends it via email.


---

5. File Organizer Bot

User selects “Organize Files” in Assistant →
Bot reads the Downloads folder → places files in date-wise folders.


---

Benefits of Assistant Bots

1. Saves time for repetitive tasks


2. Simple to use (only need to click a button)


3. Reduces human errors


4. Works side-by-side with the user


5. No coding knowledge required to use it




---

Conclusion:

Assistant Bots make automation accessible to all users by providing instant, on-demand automation for daily activities through simple triggers like keyboard shortcuts, mouse clicks, or buttons in UiPath Assistant.


---

If you want, I can prepare short 5-mark or 10-mark versions for quick revision too.