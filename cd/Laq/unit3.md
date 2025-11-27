Below are **full-length, clear, easy-to-understand 10-mark answers** for **Unit-3 (Exception Handling in UiPath)**.
No jargon, no unnecessary complexity — perfect for exam writing.

---

# **1. Discuss exception handling in UiPath using Try–Catch and Rethrow activities.**

*(10 Marks – Simple, comprehensive)*

## **Introduction**

Exception handling ensures that a UiPath workflow does not crash when something unexpected happens (like missing files, slow applications, or wrong inputs). UiPath provides **Try–Catch** and **Rethrow** activities to manage such situations smoothly.

---

## **1. Try–Catch Activity**

The Try–Catch activity works like a safety guard.

### **Try Block**

* Contains the main actions that may raise errors.
* Example: Reading Excel, clicking a button, downloading a file.

### **Catch Block**

* Executes only when an error occurs in the Try section.
* You can catch different types of errors such as:

  * FileNotFoundException
  * NullReferenceException
  * TimeoutException
  * ApplicationException

### **Example:**

Try → Read Excel
If Excel file missing → Catch → Show message “File not found”

---

## **2. Using Multiple Catch Blocks**

You can add multiple Catches to handle each error differently.
Example:

* If Excel not found → create a new file
* If selector fails → retry the action
* If timeout → notify the user

This makes workflows more stable.

---

## **3. Rethrow Activity**

The Rethrow activity is used when you want to catch an error, do some local handling, **and still pass the error up** for final handling.

### **Why use Rethrow?**

* When partial handling is done but the workflow should still stop.
* Useful in layered workflows like:

  * Sub-workflows
  * Reusable components
  * Nested Try–Catch blocks

### **Example:**

Catch logs the error → Rethrow sends it to parent workflow for final action.

---

## **Conclusion**

Try–Catch helps in **catching and controlling errors**, while Rethrow helps in **passing the error upward after a partial fix**. Together, they make UiPath automations reliable, stable, and production-ready.

---

# **2. Explain how to implement nested decision logic using Switch and Flowchart.**

*(10 Marks – Easy & structured)*

## **Introduction**

Complex automations often require multi-level decisions. UiPath supports nested logic using **Switch** and **Flowchart**, which allow the bot to choose actions based on different conditions.

---

## **1. Nested Logic Using Switch Activity**

### **What is Switch?**

A Switch allows multiple branches based on a value (like text or numbers).

### **How to use nested Switch:**

1. Create a Switch for the first-level condition
2. Inside one of the cases, add another Switch for second-level condition

### **Example:**

Email Processing System

* Switch 1: Email type

  * Case “Billing” → Switch 2: Payment status

    * Pending → Send reminder
    * Completed → Close ticket
  * Case “Technical” → Send troubleshooting steps
  * Case “General” → Auto reply

This makes multi-layered decisions easy to manage.

---

## **2. Nested Logic Using Flowchart**

### **Why Flowchart?**

Best for visual representation and branching logic.

### **How it works:**

1. Add **Flow Decision** nodes
2. Each decision leads to another decision or action
3. Complex logic becomes easy to visualize

### **Example:**

Loan approval system:

* Flow Decision 1: Is customer eligible?

  * Yes → Flow Decision 2: Is credit score high?

    * Yes → Approve loan
    * No → Manual review
  * No → Reject loan

### **Benefits:**

* Easy debugging
* Clear process paths
* Suitable for real-world workflows with many conditions

---

## **Conclusion**

Switch is best for value-based branching, while Flowchart is best for multi-path, visual decision trees. Both support nesting to handle complicated decision-making smoothly.

---

# **3. Create a workflow that handles file-not-found exception gracefully.**

*(10 Marks – Practical and simple)*

## **Introduction**

File-handling errors are extremely common in automation. A bot should not crash if a file is missing. Instead, it should handle the situation smoothly.

---

## **Step-by-Step Workflow Design**

### **1. Use a Try–Catch Activity**

Place the file-reading action in the Try block.

### **2. Inside Try Block**

* Add an activity such as “Read Text File” or “Read Range”.
* Input: `C:\Data\Report.xlsx`

### **3. Catch Block (FileNotFoundException)**

Inside Catch:

* Display a message: “File not found. Creating a new file…”
* Use “Create File” or “Write Text File” to generate a new file.
* Log the error in a log file.

### **4. Add Finally Block (optional)**

Perform cleanup tasks like closing applications.

---

## **Output Behavior**

* If file exists → bot reads it normally.
* If file missing → bot creates file and continues without crashing.

---

## **Conclusion**

This workflow shows how UiPath manages missing files gracefully using Try–Catch, improving stability and user experience.

---

# **4. Describe a real-world scenario where exception handling is critical in automation.**

*(10 Marks – Realistic, easy-to-write)*

## **Scenario: Invoice Processing Automation**

A company uses RPA to extract invoice data from incoming emails and enter it into an ERP system.

---

## **Why Exception Handling Is Critical**

### **1. Missing Attachment (File Not Found)**

User forgets to attach an invoice.
Bot must:

* Catch the error
* Send alert to user
* Move email to “Error” folder

---

### **2. Wrong File Format**

User attaches JPG instead of PDF/Excel.
Bot must:

* Identify format issue
* Log error
* Notify accounting team

---

### **3. ERP Application Not Responding**

ERP might freeze or have slow response.
Bot must:

* Retry after short delay
* If still failing → escalate to IT

---

### **4. Data Extraction Errors**

If invoice has missing fields, bot should:

* Catch NullReferenceException
* Store incomplete data in “Exception Queue”
* Send for manual review

---

### **5. Network Issues**

If internet disconnects while uploading invoice:

* Bot catches timeout
* Retries
* Logs event

---

## **Conclusion**

In real business processes, unexpected events are common. Exception handling prevents workflow failure, maintains accuracy, ensures smooth continuation, and keeps the organization’s operations stable.

---

# **5. Discuss the significance of logging and debugging during exception handling.**

*(10 Marks – Very easy & exam-friendly)*

## **Introduction**

Logging and debugging are essential tools that help identify, understand, and solve issues in UiPath workflows. They make exception handling more effective and reliable.

---

# **1. Significance of Logging**

### **1. Helps Track Errors**

Logs show what the bot was doing when the error occurred.

### **2. Improves Troubleshooting**

Developers can review logs to find:

* Faulty activity
* Incorrect selector
* Missing file

### **3. Helps in Production Monitoring**

Orchestrator logs allow support teams to monitor bots in real time.

### **4. Creates Audit Trails**

Logs record every important action, useful for compliance and auditing.

---

# **2. Significance of Debugging**

### **1. Identify Root Cause Before Deployment**

Debug mode highlights the activity where the error occurs.

### **2. Step-by-Step Execution**

Features like:

* Step Into
* Step Out
* Breakpoints

help test workflow flow carefully.

### **3. Helps Validate Data**

Locals panel shows the value of every variable during execution.

### **4. Avoids Runtime Failures**

Debugging catches small mistakes early, preventing production crashes.

---

# **3. Logging + Debugging During Exception Handling**

### **Why both are important together:**

* Logging records what happened
* Debugging shows why it happened

Example:
If a "Click" failed, logs show the failure, debugging shows that selector value was wrong.

---

## **Conclusion**

Logging and debugging are essential parts of exception handling. They help diagnose problems, improve workflow quality, and ensure stable automation in production environments.

---

If you want, I can continue with **Unit-4 or Unit-5** 10-mark answers.
