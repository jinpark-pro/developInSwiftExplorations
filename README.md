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
