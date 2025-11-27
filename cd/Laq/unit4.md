Below are **full, long, simple, exam-ready 10-mark answers** for **Unit-4 (UiPath – Web Automation, Scraping, Recording, Selectors)**.
All answers are **easy to understand**, **no jargon**, and written in scoring format.

---

# **1. Explain the process of automating a web-based application using UiPath.**

*(10 Marks – Clear, comprehensive, beginner-friendly)*

## **Introduction**

Web automation is one of the most common uses of UiPath. It allows bots to open browsers, fill forms, click buttons, extract data, download files, and complete long web tasks automatically. UiPath provides dedicated browser activities and selector-based automation to interact with web elements accurately.

---

## **1. Launching the Web Application**

Automation starts by opening a browser like Chrome, Edge, or Firefox.

### **Activities Used**

* **Open Browser**
* **Use Application/Browser**

### **What bot does:**

* Opens the URL
* Loads the webpage
* Prepares the environment for the next steps

---

## **2. Identifying UI Elements**

UiPath identifies webpage elements using **selectors**.
Each element (textbox, button, dropdown) has an internal HTML structure.

### **Example elements bot can detect:**

* Username field
* Search box
* Submit button
* Product link

Selectors allow accurate interaction even in complex websites.

---

## **3. Performing Actions on Web Elements**

### **Common Activities:**

* **Type Into** → enter username/password
* **Click** → click login button
* **Select Item** → choose from dropdown
* **Get Text** → read values

### **Example task:**

Filling a login form:

1. Type Into → username
2. Type Into → password
3. Click → Login button

---

## **4. Handling Delays and Page Loads**

Webpages may load slowly. UiPath handles this using:

* Delay
* Timeout settings
* Wait for Element
* Retry Scope

These ensure the bot does not click too early and fail.

---

## **5. Extracting Data from Web Pages**

Bots can scrape product information, tables, prices, or user details using:

* Data Scraping Wizard
* Screen Scraping
* Get Text activities

---

## **6. Closing the Browser**

After completing tasks, bot uses:

* **Close Tab**
* **Close Application**

This prevents memory usage and keeps the system clean.

---

## **Conclusion**

Web automation in UiPath involves opening a browser, interacting with web elements using selectors, performing actions, extracting required information, and closing the browser. With these steps, UiPath delivers fast and reliable web-based task automation.

---

# **2. Describe how to perform data scraping in UiPath with a suitable use case.**

*(10 Marks – Simple, exam-friendly)*

## **Introduction**

Data scraping allows UiPath to extract **structured data** from web pages, PDFs, and applications. Structured data means tables, lists, grids, product catalogs, etc. UiPath provides a built-in **Data Scraping Wizard** for this purpose.

---

# **Steps to Perform Data Scraping**

## **1. Launch the Target Application**

Open the website or software where data is present.

Example site:
Flipkart/Amazon product list.

---

## **2. Open Data Scraping Wizard**

In UiPath Studio:
**Home → Data Scraping**

The wizard guides the user step-by-step.

---

## **3. Select First and Last Element**

Bot needs to know the pattern in the data.

Example:
If scraping product names:

1. Click on first product name
2. Click on second product name

UiPath understands the repeating pattern.

---

## **4. Extract Additional Fields**

You can also extract:

* Price
* Rating
* Description

Wizard allows multiple fields.

---

## **5. Configure Pagination**

If data spans multiple pages:

* Bot clicks “Next Page”
* Wizard repeats extraction

This allows large data scraping.

---

## **6. Output to DataTable**

The extracted data is automatically stored in a **DataTable**.

Bot can then:

* Write to Excel
* Filter data
* Process records

---

# **Use Case Example: Product Price Scraping**

### **Goal:**

Extract product name, price, and rating from Amazon.

### **Steps:**

1. Open browser → Navigate to Amazon
2. Use Data Scraping Wizard
3. Select first product name → second name
4. Extract price and rating
5. Enable pagination
6. Write DataTable to Excel

**Outcome:**
You get a neatly organized Excel sheet with hundreds of products in seconds.

---

## **Conclusion**

Data scraping is a powerful UiPath feature that extracts structured data quickly and accurately. It is widely used for e-commerce, finance, reporting, and analytics tasks.

---

# **3. Explain recording features and differences between types.**

*(10 Marks – Clear classification)*

## **Introduction**

Recording helps UiPath capture user actions automatically. Instead of dragging activities manually, the recorder tracks clicks, typing, and selections to generate a workflow.

UiPath provides four major recording types.

---

# **1. Basic Recording**

### **Features:**

* Simple and fast
* Captures clicks and typing
* Good for small, linear tasks

### **Use Case:**

Filling a login form.

### **Limitation:**

Less accurate selectors, not ideal for complex apps.

---

# **2. Desktop Recording**

### **Features:**

* Best for automating desktop applications
* Strong, reliable selectors
* Supports multiple windows
* Efficient for large workflows

### **Use Case:**

Automating tasks in Excel, ERP, legacy applications.

---

# **3. Web Recording**

### **Features:**

* Specially designed for browsers
* Handles links, text fields, drop-downs
* Captures browser-specific operations

### **Use Case:**

Form filling, submitting data, flipping through pages.

---

# **4. Image Recording**

### **Features:**

* Used when application has no reliable selectors
* Works with images and OCR
* Suitable for virtual machines (Citrix)

### **Use Case:**

Automation on remote desktops and Citrix environments.

---

# **Key Differences Table**

| Recording Type | Best For               | Selector Quality   | Speed  | Example             |
| -------------- | ---------------------- | ------------------ | ------ | ------------------- |
| Basic          | Simple tasks           | Low                | Fast   | Login form          |
| Desktop        | Complex desktop apps   | High               | Medium | Excel automation    |
| Web            | Browser actions        | High               | Medium | Online registration |
| Image          | No selectors available | None (image-based) | Slow   | Citrix window       |

---

## **Conclusion**

Recording allows fast workflow creation. Choosing the right recording type improves accuracy, efficiency, and reliability of automation.

---

# **4. Develop a workflow using screen scraping and partial selector.**

*(10 Marks – Practical, simple explanation)*

## **Introduction**

Screen scraping is used when data cannot be selected normally. Partial selectors are used inside containers like **Attach Browser**, helping UiPath identify elements accurately.

---

# **Workflow Steps**

## **1. Use “Open Browser” Activity**

* Open website
* Example: [https://weather.com](https://weather.com)

---

## **2. Use “Attach Browser”**

This container ensures all activities inside share a **common selector** (partial selector).

### **Why partial selector?**

* It removes repetitive browser information
* Makes automation stable
* Faster execution

---

## **3. Add Screen Scraping Wizard**

Choose type:

* **Full Text** (fastest)
* **Native** (accurate)
* **OCR** (for images)

---

## **4. Select the Text Element to Scrape**

Example: Extracting temperature from weather website.

UiPath shows preview and extracts text.

---

## **5. Store Extracted Text in Variable**

Example variable: `temperature`

---

## **6. Display Output in Message Box**

Message Box → “Current temperature: ” + temperature

---

## **Final Workflow Structure**

```
Open Browser
   Attach Browser (partial selector)
       Screen Scrape
       Assign scrapedText
       Message Box
```

---

## **Conclusion**

This workflow demonstrates how screen scraping and partial selectors ensure stable automation even when normal selectors fail or data is in non-standard format.

---

# **5. Analyze limitations and solutions when dealing with dynamic selectors.**

*(10 Marks – High scoring, easy to understand)*

## **Introduction**

Dynamic selectors are selectors whose attributes keep changing (like IDs, classes, or indexes). Bots may fail if selectors are not handled correctly.

---

# **Limitations of Dynamic Selectors**

## **1. Changing Element IDs**

Websites often generate new IDs every time.

### **Impact:**

Bot cannot click the element → selector not found.

---

## **2. Page Layout Changes**

If UI layout shifts, the bot may click the wrong area.

---

## **3. Dynamic Text or Values**

Buttons like “Next 1”, “Next 2” change dynamically.

---

## **4. Slow or Asynchronous Loading**

If page loads slowly, the element may not exist when bot tries to click.

---

## **5. Multiple Elements with Similar Selectors**

Bot becomes confused which element to choose.

---

# **Solutions to Dynamic Selector Problems**

## **1. Use Wildcards (*, ?)**

Wildcards replace the changing part of the selector.

Example:
`id='text123'` → `id='text*'`

---

## **2. Anchor Base**

Use a nearby stable element as a reference point.

Example:
Anchor on “Username” label → Type Into field next to it.

---

## **3. Fuzzy Selectors**

UiPath’s modern feature that matches approximate elements.

---

## **4. Use “Wait for Element”**

Ensures the element appears before the bot clicks.

---

## **5. Use Regular Expressions in Selectors**

To capture patterns instead of exact values.

---

## **6. Use UI Frameworks**

Change UI framework (Default → Active Accessibility → UI Automation) when selectors are unstable.

---

## **7. Use Stable Attributes**

Instead of ID, rely on:

* Name
* Class
* Title
* Inner text

---

## **8. Use Computer Vision (CV Activities)**

When selectors are completely unreliable.

---

## **Conclusion**

Dynamic selectors can break automations, but using advanced UiPath techniques—wildcards, anchor base, fuzzy matching, delays, and UI frameworks—ensures stable and robust web and desktop automation.

---

If you want, I can now prepare **Unit-5 (Bots, Orchestrator, Deployment)** long answers.
