# 🧠 Unit 3 Vocabulary Study Sheet

**Core Concepts for Understanding the Counter Pattern** *(with Code.org CSD Unit 3 lesson links and related videos)*

---

### 💡 Counter Pattern

A common algorithm in programming where:

* A variable is declared **outside** a loop  
* The variable is **changed (incremented or decremented)** **inside** the loop  
* 🔁 Example 1: Moving a sprite across the screen.  
* 🔁 Example 2: Updating a score under a certain condition


The counter pattern is the most important pattern you'll learn in this class—it powers animations, scores, timers, and more. It shows how code can track and change over time. Mastering it unlocks endless creative possibilities in Game Lab and beyond. Stick with it—you’re building real programming skills every time you use it\!

📘 Code.org Lessons:

* [Lesson 12: The Draw Loop](https://studio.code.org/courses/csd-2024/units/3/lessons/12/levels/1)  
* [Lesson 13: Sprite Movement](https://studio.code.org/courses/csd-2024/units/3/lessons/13/levels/1)

🎥 Video:

* [Animating with Sprites](https://youtu.be/G666sFzAg5g)

---

### 🔤 Variable

A **label** that stores information in a program (like a box with a name on it). Used to hold numbers, text, or even sprites.

📘 Code.org Lesson:

* [Lesson 5: Variables](https://studio.code.org/courses/csd-2024/units/3/lessons/5/levels/1)

🎥 Videos:

* [Variables Part 1](https://www.youtube.com/watch?v=UG7Q1Sr0_F0)  
* [Variables Part 2](https://www.youtube.com/watch?v=luR8Al5CjEw)

#### ▶ Variable Label

The **name** of the variable, like `score` or `eyeSize`.

#### ▶ Declare a Variable

Use the `var` keyword to create a variable.

#### ▶ Initialize a Variable

Set the starting value of a variable.

#### ▶ Assign a Value

Use `=` to give a variable its value.

#### ▶ Value

The actual data stored in a variable.

---

### 🔁 Loop

A block of code that **repeats**. In Game Lab, the `draw()` function loops constantly.

📘 Code.org Lesson:

* [Lesson 12: The Draw Loop](https://studio.code.org/courses/csd-2024/units/3/lessons/12/levels/1)

🎥 Video:

* [The Draw Loop](https://youtu.be/G6QJeuHhqCM)

---

### 📐 Property

A **characteristic** of a sprite like its `x` position, size, or tint.

📘 Code.org Lesson:

* [Lesson 9: Sprite Properties](https://studio.code.org/courses/csd-2024/units/3/lessons/9/levels/1)

🎥 Video:

* [Sprite Properties \- Dot Notation](https://www.youtube.com/watch?v=5Op72oHFUnc)

---

### ⚙ Algorithm

A set of steps used to complete a task or solve a problem. The counter pattern is an example.

📘 Code.org Lesson:

* [Lesson 1: Programming for a Purpose](https://studio.code.org/courses/csd-2024/units/3/lessons/1/levels/1)

---

### 🔘 Dot Notation

A way to access or update object or sprite properties using a period (`.`).   
Example: `sprite.x = 100;`

📘 Code.org Lesson:

* [Lesson 9: Sprite Properties](https://studio.code.org/courses/csd-2024/units/3/lessons/9/levels/1)

🎥 Video:

* [Sprite Properties \- Dot Notation](https://www.youtube.com/watch?v=5Op72oHFUnc)

---

### 🟢 Initial Condition

The **starting setup** of a program, which includes both:

* **Variables** (such as counters, scores, or sizes set to a known starting value)  
* **Objects** like sprites (with initial position, appearance, or animation)

Setting clear initial conditions ensures the program behaves consistently every time it runs.

---

### 🧊 Sprites

Sprites are characters or images you can control in Game Lab.

📘 Code.org Lesson:

* [Lesson 8: Sprites](https://studio.code.org/courses/csd-2024/units/3/lessons/8/levels/1)

🎥 Videos:

* [Sprites Part 1](https://www.youtube.com/watch?v=96iGNtAp9J4)  
* [Sprites Part 2](https://www.youtube.com/watch?v=BrkREtPb0J4)

---

### 🖍 Drawing

The use of commands like `rect()`, `fill()`, and `ellipse()` to create shapes.

📘 Code.org Lesson:

* [Lesson 3: Drawing in Game Lab](https://studio.code.org/courses/csd-2024/units/3/lessons/3/levels/1)

🎥 Videos:

* [Drawing in Game Lab Part 1](https://youtu.be/PXn9gKiKKFo)  
* [Drawing in Game Lab Part 2](https://youtu.be/QLabeWhw_O0)

---

### ❌ Undeclared Variable

An error that happens when you try to use a variable that hasn’t been declared with `var`.

📘 Commonly seen in:

* [Lesson 5: Variables](https://studio.code.org/courses/csd-2024/units/3/lessons/5/levels/1)  
* [Lesson 6: Random Numbers](https://studio.code.org/courses/csd-2024/units/3/lessons/6/levels/1)

---

## 🚫 Common Errors in Game Lab

### 1\. Undeclared Variable Error

```
ERROR: Line: 9: Oops, we can’t figure out what orangeFish is — perhaps you meant the string "orangeFish" with quotes? If this is meant to be a variable, make sure you declared a variable: var orangeFish
```

**What it means:**  
You’re trying to use a variable (`orangeFish`) before telling the computer that it exists. In JavaScript, you must use `var` to declare the variable before using it.

**Why it’s wrong:**

**❌ Incorrect Code:**

```javascript
orangeFish.x = 200;
```

Here, you’re trying to use the variable without declaring it first.

**How to fix it:**  
You need to declare the variable first and create the sprite before using it.

**✅ Correct Code:**

```javascript
var orangeFish = createSprite(200, 200);
orangeFish.x = 200;
```

---

### 2\. TypeError from Using an Uninitialized Variable (undefined variable)

```
ERROR: Line: 5: TypeError: Cannot read property 'x' of undefined
```

**❌ Incorrect Code:**

**What it means:**  
Even though you declared the variable, you used it *before* it was assigned. JavaScript runs your code in order, so i `orangeFish` is “empty” or “undefined” when you try to use it.

**Why it’s wrong:**

```javascript
orangeFish.x = 250;
var orangeFish = createSprite(200, 200);
```

You’re trying to move the sprite before it exists.

**How to fix it:**  
Make sure to declare and create the sprite *before* you use it:

**✅ Correct Code:**

```javascript
var orangeFish = createSprite(200, 200);
orangeFish.x = 250;
```

---

### 🧩 Abstraction

**Abstraction** means simplifying your code by hiding details and grouping steps together. You do this by using **functions**—your own custom blocks of code.

Benefits of abstraction:

* 🧠 Focus on **what** the code does, not all the details  
* ♻️ Reuse code instead of repeating it  
* 🧹 Keep your program clean and organized

📘 Code.org Lessons:

* [Lesson 20: Collision Detection with `sprite.isTouching()`](https://studio.code.org/courses/csd-2024/units/3/lessons/20/levels/2) – Use abstraction to check collisions and respond  
* [Lesson 25: Functions](https://studio.code.org/courses/csd-2024/units/3/lessons/25/levels/1) – Learn to define and call your own functions

🎥 Video:

* [Calling and Defining Functions](https://youtu.be/3ZfqwCuDZaQ)  
* [Functions with Parameters](https://www.youtube.com/watch?v=5UMKeMPCa7E)

---
