# Develop in Swift Explorations

## Values

### Constants and Variables

- ```swift
    // Declaring a constant
    let placeOfBirth = "New Jersey"

    // Declaring a variable
    var currentLocation = "New Jersey"

    // Assigning a new value to a variable
    currentLocation = "California"
  ```

- In most ways, constants and variables are the same:
  - Both use the same rules for names
  - Both associate a name with an assigned value
  - Both have a specific type
- The difference is:
  - The value of a constant cannot be changed after it's first assigned.
  - The value of a variable can be changed after it's first assigned.
- Values declared with let are constants, and can’t be changed once a value is assigned. These values are called immutable.
- Values declared with var are variables, and can be assigned new values over time. These values are called mutable.
- A mutable value can be used as part of an assignment statement to itself: score = score + 10.
- Compound assignment operators allow mutable values to be updated: score += 10.
- Using constants and variables in the correct places helps make your code safer and easier to understand.
- Error Indicator
  - The normal error indicator is a red circle with a white x in it.
  - But an error indicator having an idea how to fix the error on Xcode is a red circle with a white dot in it.
    - a Fix-it will fix errors in your code, but the fix might not be what you meant to do.
    - The Fix-it is trying to be helpful, but it could be suggesting that you make something mutable that you wanted to stay immutable.
- special string syntax for long text

  - ```swift
      let manyLineString =
      """
      This is a long string.
      It can be interpolated \(1) or any number of times. You don't have to escape "quote marks."

      And it can contain empty lines, like the one above.
      Just use three quotes on their own lines to open and close it.
      """
    ```

### Build a PhotoFrame App

1. Create a new Xcode project.
   1. iOS section > App > Next
   2. Product Name: PhotoFrame, Interface: Storyboard, Language: Swift > Next
   3. Select a location to save > Create
2. The simulator may appear large on your screen. You can make it smaller by choosing Window > Physical Size.
3. Xcode Workspace
   - <img src="./resources/images/xcode_workspace.png" alt="Xcode Workspace" width="400" />
   - Toolbar
     - To check the project's status
     - To hide and show the other window areas
     - To build and run your app from the big "Play" button
   - Navigator
     - To move around your project; select file to open in the editor by clicking it
   - Editor
     - To edit your project files; source code, user interface items, or app configuration
   - Inspector
     - To find out more details about the item currently selected or displayed in the editor
     - Especially to edit user interface files in Interface Builder
4. Add a Photo
   1. Select Asset on teh navigator area.
   2. Drag in image files
5. Edit the Storyboard
   1. Open the storyboard by selecting `Main` from the list of files in the project navigator.
   2. Change the Device.
      1. Click the Devices icon at the bottom of the window and select iPhone 13 Pro.
   3. Select the main view.
      1. Click anywhere in the scene to select its main view.
      2. In the Document Outline to the left, you'll notice that the View Controller Scene expands to show the items it contains, and the View item is highlighted.
   4. Show the Attributes inspector.
   5. Adjust the background color.
   6. Run you app
6. Adding a Frame
   1. Open the Object library, type `UIView`
   2. Drag `View` in the center of the view controller.
   3. Resize to make the view large enough to display your photo.
   4. In the Attributes Inspector, select the menu next to Background, select Custom, and choose a color from the color picker.
7. Adding and Configuring an Image View
   1. Open the Object library, type `image`
   2. Drag `Image View` into the frame view.
   3. Resize the image view until the frame behind it is the right width.
   4. In the Attributes Inspector
      1. Choose the image you added earlier at the top of the inspector.
      2. Select Content Mode to Aspect Fill.
         - <img src="./resources/images/photo_frame.png" alt="Photo Frame" width="200" />

### Design For People

## Algorithms

### Get Started With Algorithms

- An algorithm is a set of instructions for accomplishing a task.
- There are three essential building blocks in all algorithms: `sequencing`, `selection`, and `iteration`.
- Sequencing
  - Arranging instructions in order is called sequencing, and it's one of basic techniques for creating an algorithm.
  - Swift uses sequencing as it executes your code line by line and from top to bottom.
- Selection
  - Selection lets you describe multiple paths through your algorithm.
  - By using selection, you can examine the conditions at the time your code runs and your program will proceed along one of many possible paths.
- Functions
  - In Swift, you use functions to group instructions together and give them a name.
  - By breaking a problem into pieces, you can write functions to solve each piece independently.
  - You can combine them to solve the bigger problem.
  - The approach of grouping instructions into a unit and giving that unit a name is call `procedural abstraction`.
  - Remember, the key feature of any kind of abstraction is to hide, or encapsulate, the details of how something works.
  - After you've written and tested a function, you no longer have to think about how it works, just about what it does.
- Types
  - Swift uses the term type to describe each different kind of value.
- Parameters
  - You use parameters to define the input that goes into a function.
  - Each parameter for a function has a type.
  - By adding parameters to functions, you can make them more flexible so they can be used in a variety of situations.
- Making Decisions with Booleans
  - The yes-and-no answers are represented in Swift as "true" and "false."
  - They are known as Boolean values, named after George Boole, a 19th century mathematician.
  - The Bool type is used in Swift to represent Boolean values.

### Play with Programs

- Functions

  - Reusability is a large part of what makes functions so powerful.
  - Any identifier followed by parentheses, `()`, is a function.
  - The code between the two braces, `{...}`, is called the body of the function.
  - Nothing is displayed in the results because declaring a function only describes what the function would do if it ever run.
  - To actually run the code, you have to call the function. Typing the name of the function will call the function.
  - Decomposition: break a single long list down into multiple smaller lists.

- Types

  - String
  - Number is Int, an abbreviation of integer.
  - Swift keeps track of the type of the variable and makes sure you don't accidentally try to assign a value of a different type.
    - The value of a variable can change, but the type of the variable can't change.
  - Type Safety: Swift won't let you write code that uses types incorrectly or unexpectedly.
    - Another instance of type safety would occur if you tried to add values of different types.
  - A literal is the simplest form of expression.
  - Swift makes assumptions about what types the literals are meant to be.
    - Any value inside double quotes will be treated as a String, and a whole number will be treated as an Int.
    - Type Inference: Swift uses context clues from code to infer what type something is.
  - Check the type by holding down the `Option` key while clicking a variable.
  - You can add an extra piece of information, called a `type annotation`, to tell Swift exactly what type you want to use.
    - `let annotationDouble: Double = 20`
    - `annotationDouble` is a Double, even though there is no decimal point, because of the type annotation.
  - All type names begin with a capital letter. If there are multiple words the first letter of each word is also capitalized.
    - This is slightly different from the rules for naming constants, variables, and functions, which all begin with lower-case letters.
  - Types and capabilities can be grouped together into collections called `frameworks` or `libraries`.
    - To use a framework in your program, you have to import it like `import Foundation`.

- Parameters and Results

  - Declare: `func functionName(parameter: Type) {...}`
  - Call: `functionName(parameter: argument)`
  - Passing a value back when a function is finished is called returning a value. To declare a function that returns a value, you have to add two things to your code.
    - After your list of parameters, add a text arrow `->` and the type of value to be returned.
    - Then you have to end the body of the function with a return statement that gives that type fo value back.
    - `func functionName(parameter: Type) -> Type { ... return ...}`
    - Your function can have multiple parameters, but it can only return one value.
  - When a function does some kind of work that's unrelated to a return value, like printing to the console, the work is call a `side effect`.
    - When you name a function, it's good to somehow include the side effect in the name.
    - If a function has no return value, all of its work is considered a side effect.
    - A function that has a side effect should have a verb in the name.
  - The order that code executes in a program is called `control flow`.
  - When your code calls a function, the following line doesn't execute until after the function returns.
  - `func functionName(argumentLabel parameterName: Type) {...}`

    - ```swift
        func printHello(to name: String) {
          print("Hello " + name)
        }
        printHello(to: "Chris")
      ```

  - To declare a parameter without an argument label, you use the underscore `_` where the argument label would go.
  - In Swift, the underscore means "I don't care about this item because I'm not going to use it."

    - ```swift
        func printHelloTo(_ name: String) {
          print("Hello " + name)
        }
        printHelloTo("John")
      ```

- Making Decisions

  - Clean code
  - Conditionals are perfect opportunities to write helpful functions. If you have some decision-making code that doesn't read easily or makes things look to complicated, you can wrap it in a function and make it look like you're asking a question.

    - ```swift
        if gearWeight < totalCarryingCapacity {
            if bulkiestItemWeight < 80 {
                "Rock on."
            } else if chanceOfRain >= 0.1 {
                "Everyone quits! Looks like you've got a solo show."
            }
        } else {
            "Everyone quits! Looks like you've got a solo show."
        }
      ```

    - ```swift
        if gearWeight < totalCarryingCapacity && (chanceOfRain < 0.1 || bulkiestItemWeight < 80) {
            "Rock on."
        } else {
            "Everyone quits! Looks like you've got a solo show."
        }
      ```

    - ```swift
        func bandCanCarryGear(bandMemberCount: Int, gearWeight: Int, bulkiestItemWeight: Int, chanceOfRain: Double) -> Bool {
            let maximumTripCount = 2
            let weightPerPerson = 50
            let totalCarryingCapacity = bandMemberCount * weightPerPerson * maximumTripCount

            return gearWeight < totalCarryingCapacity && (chanceOfRain < 0.1 || bulkiestItemWeight < 80)
        }
        if bandCanCarryGear(bandMemberCount: 5, gearWeight: 650, bulkiestItemWeight: 60, chanceOfRain: 0.05) {
            "Rock on."
        } else {
            "Everyone quits! Looks like you've got a solo show."
        }
      ```

- BoogieBot

  - Functions are the way programmers group blocks of work together.
    - A function is reusable, which saves on reading and typing.
    - A function can be understood on its own, so you don't have to think of every single step.
    - If a function is changed, the changes apply everywhere the function is used.

- Data Visualization

### Build a QuestionBot App

- Rather than running the app several times as you develop your code, you can use a playground to get your question answerer up and running more quickly.
- You can see multiple results instantly, and there's no need to return.
- Once you're happy with your code, you'll use it to replace the existing code segment in QuestionBot.

#### Building Your Function

- QuestionAnswerer.playground

  - ```swift
      import Foundation
      func responseTo(question: String) -> String {
          let lowerQuestion = question.lowercased()

          if lowerQuestion.hasPrefix("hello") {
              return "Why, hello there"
          } else if lowerQuestion.hasPrefix("where are the cookies?") {
              return "In the cookie jar!"
          } else if lowerQuestion.hasPrefix("where") {
              return "To the North"
          } else if lowerQuestion.hasPrefix("can i") {
              return "Yes, you can"
          } else if lowerQuestion.contains("your name") {
              return "My name is QuestionBot."
          } else if lowerQuestion.contains("what time") {
              return "\(Calendar.current.component(.hour, from: Date())):\(Calendar.current.component(.minute, from: Date()))"
          } else {
              if lowerQuestion.count % 2 == 0 {
                  return "Thank you for asking, but I have no idea."
              } else {
                  return "Please ask it tomorrow."
              }
          }
      }

      responseTo(question: "Hello there")
      responseTo(question: "Where are the cookies?")
      responseTo(question: "Where should I go on holiday?")
      responseTo(question: "Can I have a cookie?")
      responseTo(question: "Should I go?")
      responseTo(question: "What time is it?")
    ```

#### Updating the App

- common problems:
  - **The app runs but you don't see the answers** you were expecting. This is probably because you pasted the function in the wrong place. Perhaps it was in the wrong file, or in the wrong place in the correct file.
  - The app doesn't build with an error that reads **Unexpected non-nil return value in void function**. You probably pasted the function body code from the playground into the wrong function in the project.
  - The app doesn't build with an error that reads **Invalid redeclaration of responseTo(question:)**. This means you have two functions with the same name in the same area of the code - not allowed because it isn't clear which function should run when called.
  - The app doesn't build with an error that reads **Expected declaration**. You may have inadvertently replaced the entire function, declaration and all, with only the body of the function from your playground, or you pasted the function body into the wrong place.
  - The app doesn't build with an error that reads **Missing return in a function expected to return 'String'**. You probably pasted an entire function inside another one.
  - The app doesn't build with an error that reads **Closure expression is unused** or **Expressions are not allowed at the top level**. You probably pasted the body of your function into a file without any context - with no `func` keyword.
  - The app doesn't build with an error that reads **Use of unresolved identifier 'MyQuestionAnswerer'**. You probably replaced the entire `struct MyQuestionAnswerer` with the `responseToQuestion` function or its body.

#### Customizing the Interface

- Open the Main.storyboard, and make sure the Attributes inspector is visible.
- Background Color
  - Select View under View Controller, and use the Background attribute to choose a different color.
- Robot Head
  - Select the Robot Head label under Stack View
  - Using the Text attribute in the inspector, change the emoji to a different character.
  - Press `Ctrl + CMD + Space` to bring up the emoji picker.
- Welcome Message
  - Select Response Label in the Document Outline and change the opening text.
  - Pressing `Ctrl + Return` to add a new line if you need one.

### Design an Experience

- Design isn't just about how a product looks and feels; it's also about how it works.
- A crucial step in designing successful computing innovations is understanding the people who will use the innovation.
- When your design incorporates diverse perspectives, it will improve the experience for all users.
- Apple has four key principles around designing for user privacy:
  - Request consent when your app needs personal data.
  - Be transparent about how personal data will be used.
  - Give the user control over their personal data and protect the personal data you collect.
  - Use the minimum amount of personal data required.

#### Plan

- You need to consider how your main screens will look. Refer back to your design mood board for inspiration, and sketch a few screens.
- <img src="./resources/images/initial_idea.png" alt="Initial Idea" width="500" />
- Show how a user will move through the screens - a storyboard.
  - You can create a storyboard by organizing the screens in a flowchart and indicating the graphic elements that enable users to make choices within the app.
  - <img src="./resources/images/storyboard.png" alt="Storyboard" width="500" />

#### Create a User Experience Flowchart

- Take photos or screenshots of your screens and add them to Keynote.
- The flowchart should show how a user can move through your app based on the choices they make.
- Annotate your storyboard to explain key features of the app, and highlight the accessibility features you've incorporated.
- Apple provides [resources](https://developer.apple.com/accessibility/) to support developers to build accessible apps.

#### Review and Iterate

- Simplification is a key idea in the app design process.
- If you're very clear about purpose, you can simplify your design so your app fits seamlessly into the flow of the user's activity.
- Share your storyboard with your peers or mentors.
  - As they explore your app design, encourage them to ask you How? Why? and What if? questions. You can record their responses or annotate your storyboard with their queries and ideas.
  - With a partner, take turns examining each other’s designs through the lens of someone who has a disability. (You can consider four broad categories: vision; hearing; physical and motor; and learning and literacy.)
  - Each of you should adopt a specific persona and explain your requirements when using an app. Then work through the app and give feedback from that person’s point of view. Together, identify ways you could improve the app to make it more inclusive.
- App design is an iterative process, and identifying problems and issues can be seen as an opportunity rather than a setback. If you need to, return to the brainstorming phase and use your new insights to revise your app idea. Great apps are the product of extensive ideation, exploration, testing, and revision.

## Organizing Data

### Get Started With Organizing Data

#### Instances, Methods, and Properties

- Types enable you to understand what each value in your code represents.
- Type safety in Swift ensures that you use values of the right type in the right place.
- Types can also define or describe the attributes and behaviors of a particular kind of thing - in other words, what a type is, or knows (its attributes), and what it does (its behaviors).
- In Swift, the attributes of a type are called `properties`, and its behaviors are called `methods`.
- Even though the type describes the properties and methods of a particular kind of thing, each concrete example of the type is a separate, independent instance of the type.

#### Lists and Arrays

- In Swift, such a collection is called an array.
- An array is a collection of individual instances of just one ypte.
- Each instance in the array is called an element.
- Each element in an array has a unique index, which identifies its location in the array respective to the first element, which is always located at index 0.

#### Algorithms: Iteration

- In algorithms, repeating the same swquence of steps multiple times is known as iteration.
- In Swift, as well as all other programming languages, iteration is critical building block of algorithms.
- Remeber - algorithms have three basic building blocks: sequencing, selection, and iteration.

#### Loops

- The term for iteration in most programming languages, including Swift, is a loop.
- A loop defines a code segment that will be repeated - its body - and a determination for when to exit the loop.

#### Working With Arrays - Searches

- It can be very useful to apply a function to every item in an array, but what if you just wanted to perform that function on one particular item?
- You would need to find that item's location in the array - its index - and specify that you were performing the function on the item at that location.
- Finding an item in an array (or determining that it's not there) is called searching, and there are multiple algorithms for performing a search on an array.
- Linear search
  - It isn't as efficient as binary search because it works by evaluating the items in the list one after the other - which means it might have to evaluate the entire list before it finishes.
- Binary search
  - The approach works by successively splitting finding the middle element and comparing the sought value to the middle element.
  - If the value is greater, the first half of the list can be eliminated.
  - If the value is less, the second half can be eleminated.
  - If the value is equal to the middle element, the algorithm has found the value in the list.
- Binary searches are more efficient that linear searches, especially with large amounts of data, but require that the data be in sorted order.

#### Defining Your Own Types With Structs

- In Swift, you can create types of your own that group lots of attributes together.
- A very common way to create a new type in Swift is to define a `struct`.
- When you make your own struct, you define properties that represent all the attributes of the thing they represent.
- In the definition of your struct, you'll also probably include methods to perform useful tasks.

### Play with Complex Data

#### Experiment with Organizing Your Code

##### Code - Instances, Methods, and Properties

###### Instances

- You can create and use different instances of a given type.
- Each instance has its own set of property values, and each instance can perform behavior independent of other instances.
- Creating an Instance
  - You've created almost every instance by typing a literal value directly into code.
  - The exception was in the Types playground, where you used `Date()` to create a value holding the current time.
  - `Date()` looks a lot like a function, but with an important difference: It uses a type name instead of a name beginning with a lowercase letter.
  - You use an initializer to create a new instance of a particular type.
  - Only a few types, like String, Bool, and Int, can be created using literals, but every type has at least one initializer.
  - Even types you've been creating using literals have initializers.
  - You'll often want to provide more information when you create an instance.
  - Many types have initializers with parameters to let you do this:
    - `let oneHourLater = Date(timeIntervalSinceNow: 3600)`
    - This initializer gives you a Date that is a number of seconds from the current time.
  - Initializers and functions are similar in some ways:
    - They can have parameters or no parameters at all.
    - You call them the same way, by passing in required argument values.
  - They also have differences:
    - You use the name of the type when calling an initializer.
    - An initializer returns a new instance of its type.

###### Methods

- Functions can be defined as part of a type.
- These functions are called instance methods, or just methods.
- String has many instance methods, which are used for common operations.
- It's often useful to know if a string begins with another string. The method `hasPrefix()` can answer this question.
  - The method is declared like this: `func hasPrefix(_ prefix: String) -> Bool`
  - The method `hasPrefix()` has a String parameter, which is the prefix you want to test, and returns a Bool.
  - Instance methods are called by using a period (.) after the instance, followed by the method call:
    - `introduction.hasPrefix("It was")`
    - This is known as calling a method on the instance. You've called hasPrefix() on introduction.

###### Methods and Type Safety

- Type safety still applies when you're using instance methods. hasPrefix is a String instance method, so you can't use it without an instance.
- You also can't use an instance method on an instance of the wrong type. You can only use methods that are part of, or members of, a particular type.

###### Properties

- Each instance has one or more pieces of associated information. These values are known as properties.
- It's often useful to know if a string contains any characters at all. The property `isEmpty` answers this question.
- The property is declared like this: `var isEmpty: Bool { get }`.
  - It is marked `var` because the property value could change if the string contents change.
  - The `{ get }` indicates you can only get the value of this property, but you can't set it.
  - This is also called a `read-only` property.
- Properties are called by using a period (.) after the instance, followed by the property name:
  - `something.isEmpty`
- The same type safety rules apply for properties as with methods.

###### Properties Versus Methods

- Variable Versus Function
  - The different between a method and a property is similar to the difference between a function and a variable or constant.
  - A variable is useful for **referring to a value** that you can access when required. Similarly, a property provides a way to get or set a value that's part of an instance. Each instance can have a different value for that property.
  - A function is useful for **providing behavior** that can be repeated as needed. A method works in the same way, providing behavior specific to that instance.
- Arguments
  - If the work you want to perform needs extra information, then it must be a method, since you can't pass arguments to a property.
  - That means `hasPrefix()` must be a method, because you need to pass in the prefix you're testing for.
- Side Effects
  - If the work has side effects, things that happen that aren't related to the return value, then it's a method.
  - For example, String has a method, `removeAll()`, which empties the string.
- Values
  - Properties are for getting values from an instance and for setting values on an instance. Properties don't do any additional work.

##### Arrays and Loops

##### Structures

##### Enums and Switch

##### Testing Code

##### Processing Data

#### Creatively Apply Your Thinking

##### Pixel Art

##### Password Security

##### Visualization
