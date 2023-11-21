# Stack


### Overview

<aside>
<img src="https://www.notion.so/icons/snippet_gray.svg" alt="https://www.notion.so/icons/snippet_gray.svg" width="40px" /> A stack is a linear data structure that follows a particular order in which the operations are perfomed. The order may be LIFO (Last in First OUT) or FILO (First In Last Out). This structured is used in many algorithms and has a simple yet powerful concept.

</aside>

### Simple Terms:

---

Imagine a stack of plates. You can only take the top plate off or put a new plate on top. This is how a stack words in data structures. You can only add (push) or remove (pop) elements from the top of a stack. 

### Key Terms:

---

- ************Push:************ Add an element to the top of the stack.
- **********Pop:********** Remove the top element from the stack.
- ********************Top/Peek:******************** Look at the top element without removing it.
- ************Empty:************ Check if the stack is empty.
- ************Size:************ Get the number of elements in the stack.

### Syntax:

---

This syntax is conceptual and may vary based on programming language: 

```jsx
class Stack {
    push(element)
    pop()
    peek()
    isEmpty()
    size()
}
```

### Example:

---

```jsx
class Stack {
    constructor() {
        this.items = []
    }

    push(element) {
        this.items.push(element)
    }

    pop() {
        if(this.items.length > 0) {
            return this.items.pop()
        }
    }

    peek() {
        return this.items[this.items.length - 1]
    }

    isEmpty() {
        return this.items.length == 0
    }

    size() {
        return this.items.length
    }
}
```

### Breakdown:

---

1. **Constructor:** Initializes the stack with an empty array `items`. 
2. **push(element):** Adds a new `element` to the top of the stack.
3. **pop():** Removes and returns the top element of the stack. If the stack is empty, it doesn’t perform any operation. 
4. **peek():** Returns the top element without removing it from the stack. 
5. **isEmpty():** Returns `true` if the stack is empty, otherwise `false`. 
6. **size():** Returns the number of elements in the stack. 

### Real World Example

---

One of the most relatable real-world examples of a stack is the functionality of the back button in web browsers. When you navigate various web pages, the URLs of these pages are stored in a stack. Each new page visited is “Pushed” onto that stack. When you click the back button, the browser “Pops” the URL from the top of the stack, taking you to the previous page. 

```jsx
class BrowserHistory {
    constructor() {
        this.historyStack = new Stack();
    }

    visitPage(url) {
        this.historyStack.push(url);
        console.log("Visited:", url);
    }

    goBack() {
        if (!this.historyStack.isEmpty()) {
            // Popping the current page
            this.historyStack.pop();
            if (!this.historyStack.isEmpty()) {
                // Peeking to get the previous page
                console.log("Going back to:", this.historyStack.peek());
            } else {
                console.log("No more pages to go back to.");
            }
        } else {
            console.log("No history available.");
        }
    }

    currentUrl() {
        if (!this.historyStack.isEmpty()) {
            return this.historyStack.peek();
        } else {
            return "No current page.";
        }
    }
}

// Example Usage
let browser = new BrowserHistory();
browser.visitPage("https://www.example.com");
browser.visitPage("https://www.example.com/about");
browser.visitPage("https://www.example.com/contact");

console.log("Current URL:", browser.currentUrl()); // Shows the last visited URL

// Going back
browser.goBack(); // Goes back to 'about' page
browser.goBack(); // Goes back to 'home' page
browser.goBack(); // No more pages to go back to
```

### Breakdown

---

- **BrowserHistory Class:** Simulates a web browser’s history functionality.
- **visitPage(url):** Mimics visiting a new page by pushing the URL onto the stack.
- **goBack():** Simulates the back button. It pops the current URL (the top element of the stack), then peeks at the next URL, which becomes the current page.
- ***currentURL():** Returns the URL at the top of the stack, representing the current page.
- **Example Usage:** Demonstrates visiting pages and then using the back button functionality.

