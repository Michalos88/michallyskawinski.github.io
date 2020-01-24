---
layout: default
title: Talking Software Design
---
<h1 class="page-title">Talking Software Design</h1>

## Why does this matter?
* I had come to realize that I wasn't taking enough time to compose myself and gather my thoughts, but instead **kept talking even if it wasn't of substance**
* The biggest mistake that candidates make is that they are often **unable to provide clear and digestible explanations of their previous work.**

## General:
* Tell them what you're going to tell them, tell them, and then tell them what you told them - is a great method to communicating during your interviews (structure)
* If your interview has structure, the interviewer will know where in the process you are and how to help you when you get stuck
* Don't jump all around all over the place - keep it logical
* Don't jump to the best solution straight away without explaining how you got there
* If you are worried that you will forget something make a note on the whiteboard
* Interviewer wants to get an idea of how it is to be working with you
* The coding interview is **not only a test to your technical skillset** but also on your critical thinking, communication, and teamwork.
* Don't pick the first solution:
  * First, it shows that you will not consider other solutions while at work
  * Makes it difficult for the interviewer to understand how and why you came to this conclusion
  * There are always many solutions and each has pros and cons
  * If you can't come up with an alternative solution, discuss why your solution is great, and where it can be improved and revisit if you are strapped for time
* Use "we" instead of "I" - to show that you are a team player
* Take your time

## Discussion 7-8 minutes
0. Be clear and detailed with the proposed approach to provide crystal clear understanding on how you are solving the problem, and what they can expect from you.
1. Start with example 2. Ask clarifying questions (input, output, function): 1. Reverse the question and test your understanding on the example, asking if you got it right 2. How is the input provided? In memory? Array?  3. Are the numbers sorted?
  4. Any repeating elements? Can I reuse elements?
  5. Are the numbers integers, floating points? What's the range of numbers? - positive, negative?
  6. What do I return? What happens if nothing is found? Does it require a special data structure?
  7. You can write down notes
3. Start with the simplest solution and analyze
  1. Like I would have two for loop, one starting from this, second starting with this, etc.
  2. What would be the time complexity of it?
4. How do we improve it?
  1. Go back to the example and think about how can be improved?
  2. Are you using all of the information?
  3. Can we exploit memory?
5. Test your new solution and go through the example
  1. When does the loop end? On what condition?
  2. If it works in a true example, test in the other examples
  3. Just step through the example conceptually till the end of the theoretical program
6. If you forget something, make sure to tell an interviewer about it
7. If you both agree on the solution move to coding

## Implementation
0. As you write the body of your code, you should stop to explain what the code does
1. Start by writing the main loop, ask what should be the input
2. Say what you are going to write, before writing anything
3. Talk about caveats when input is empty and how it would affect the code
4. Rather than testing something with if statements a couple of times perhaps store in a variable
5. Change the code as needed and go back if you see improvement
6. Talk about what would happen if the input changes - like no longer sorted
7. Talk about what you should be careful about
8. Use comments
9. If you don't remember syntax - say it
10. Test code with example in real-life
  1. Once you do it, you can write down what you store
11. Talk about underflows and overflows
12. Talk, why is the time complexity of the code what you said it is?

## Talk about large scale solution:
1. Discuss how the problem changes? Is it still the same range of numbers?

## Write clean code
* Break out long and confusing functions into smaller helper functions
* Do you try to solve the bigger picture and link up all the parts or do you get distracted?
* Do you get caught up in very specific and unimportant pieces of information?
* Is the code reusable? Make the code generic
* Do you think through use cases and environment of the code and how you want to structure it?

## Roadblocks:
* Eventually, you will come across a situation where you hit a roadblock and get stuck in your solution, or you'll need to adapt it to a more complicated problem.
* How you approach it, will show how you'll behave and perform on the job
* Don't give or get stressed out
* Take some time to revisit your steps on how you got to your current solution
* Check if you missed any vital information
* **Be sure to talk through the steps and how they are related to each other.**
* If you are stuck, phrase it as a question to the interviewer, they are there to help you, and they want to help you.
* If you can't solve it or it's too late for switching the algorithm, be sure to mention this to the interviewer. This shows that you at least know that there is a problem and give the ability for the interviewer to help you

References:
* [How to improve communication during coding interview?](https://blog.pramp.com/how-to-improve-communication-during-a-coding-interview-41f7d8daa8f2)
* [How to: Work at Google — Example Coding/Engineering Interview](https://www.youtube.com/watch?v=XKu_SEDAykw&t=35s)
