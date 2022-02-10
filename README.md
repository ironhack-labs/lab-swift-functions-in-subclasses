
![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Lab | Functions in subclasses

<br>

## Introduction

In this lab, we will define classes representing programmers and teachers, which are both employees. We will properly encapsulate the data we need and override functions in such a way that we get the desired results. 

After completing this lab, you will be able to:

- Create subclasses
- Implement new initializers and override functions
- Mark properties and functions as private and final
- Call subclass overridden functions from a superclass' defined function

## Requirements

- Fork this repository.
<!-- - Add your instructor and the class graders to your repository and ensure that your repository is private. Public repositories will receive a zero on the assignment.
  - If you are unsure who your class graders are, ask your instructor or refer to the day 1 slide deck. -->
- Upload the code for all of the following prompts to your repository.

## Submission

- Upon completion, run the following commands:

  ```shell
  git add .
  git commit -m "done"
  git push origin main
  ```

- Create a Pull Request

When you make pull request in pair-programming: `student1,student2-nameOfTheExercise` <br>
When you make a pull request in individual-programming: `student-nameOfTheExercise`

<br>

## Starter code

No starter code needed/provided.

<br>

## Iterations

### Iteration 1

- Create a class `Employee` with properties `firstName`, `lastName` and `hasAJob`. Give the Bool property `hasAJob` private access modifier. 
- Create an init for all properties.
- Create a function `nameString()` that returns a String of introduction, containing `firstName` and `lastName` properties. For example: "My name is John Wick".

### Iteration 2

- Create a function `jobString()` that returns a String indicating the employee's employment status, depending on the value of the `hasAJob` property. For example, if `hasAJob` is false, return: "I am currently unemployed." 
- Create a func `introduceString()` that returns a String which is containing both return values of `nameString()` and `jobString()` functions, added one after the other (concatenated).
- Create an object of this class and print its `introduceString()` return value.

### Iteration 3

- Create a class `Teacher` and make it a subclass of `Employee`. Create a property `subject` representing a subject the teacher is teaching.
- Create an initializer that initializes all properties. Call the superclass init within the `Teacher` class init using the keyword 'super'.
- Override `jobString()` function and re-implement its logic in such a way that it now returns a String stating that this individual is a teacher in a particular subject, while also adding the return value of its superclass' `jobString()` function to it (concatenating it), using the 'super' keyword. For example, the return value could be: "I am a biology teacher and I am currently unemployed."
- Create an object of this class and print its `introduceString()` return value

### Iteration 4

- Create a class `Programmer` and make it a subclass of `Employee`. Create an optional property `yearsOfExperience` representing how long a programmer has been working.
- Create an initializer that initializes all properties. Call the superclass init within the `Programmer` class init using the keyword 'super'. Give the `yearsOfExperience` input parameter a default value of `nil`.
- Create a private function `experienceString()` that returns a String whose value depends on the `yearsOfExperience` property value. If `yearsOfExperience` is `nil`, return "Student". If it is not `nil` but it's lower than 2, return "Junior". If it is between 2 and 4, return "Intermediate". If it is larger or equal to 4, return "Senior".
- Override `jobString()` function and re-implement its logic so it returns a String stating that this individual is a programmer and how experienced they are, using `experienceString()` function, while also adding the return value of its superclass' `jobString()` function to it (concatenating it), using the 'super' keyword. For example, the return value could be: "I am a Junior programmer and I am currently unemployed."
- Create an object of this class and print its `introduceString()` return value.

### Iteration 5 (Bonus)

- Give the `introduceString()` and `nameString()` functions of class `Teacher` the correct access modifier that will prevent them from being overridden in their subclasses. 
  - Hint: we have mentioned this access modifier in today's activity.
- Give the `Teacher` and `Programmer` classes the correct access modifier that will prevent them from being subclassed.
  - Hint: we have mentioned this access modifier in today's activity.
- Give the `jobString()` function of class `Teacher` the `internal` access modifier. Search online and explain what this access modifier does.

<br>

Happy coding! :heart: