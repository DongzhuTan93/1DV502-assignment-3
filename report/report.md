# Reflection on my Intended Design

### There are lot of things I can think about the classes in my diagram if I compare it with the teacher´s solution. He has good structure and an advanced solution, and he divides the code more finely into different files/classes, each class is subtly related to other classes.  

#
### Comparing my own designs, I think I've properly shown the important classes that the game needs on the diagram, but I didn't consider that maybe they could be further split into several subclasses at that time. Such as I have a tile class which is intend to contain different tiles, property, free tile and start tile, while teacher divide them into three subclasses that inherit from the tile class, and with the help of board class to creates the tiles. I didn't think carefully about these subclasses at the time but now I know it´s good to divide the behavior into different classes, In doing this, you can reuse the fields and methods of the existing class without having to write (and debug!) them yourself. Although sometimes there is not much content in some subclasses, it is still convenient for us to add more functions in the subclasses later, which is also a good practice for larger projects in the future.

#
### I have a computer player class as a subclass which is inheriting from the player class in my class diagram, it inherits all the members (fields, methods, and nested classes) from its superclass, I haven't seriously thought about what extra functionality it has but I created it to play against human player in a further design. It was placed next to the human player class with the name “Computer Player” and it is clearly to see that they both inherit to the player class in the class diagram. Just considering the importance of class names, I could just use “C” instead of “Computer Player” and “H” instead of “Human Player” if I wanted to omit some letters, but would it make it easier for other readers to understand my design and implementation? A suitable classname is not just easy to read and understand. As Anastasiia Zhuravleva pointed out in her article “Naming Classes- Matters, and How to do it well” about the benefits of proper class naming, “It´s easy to search and navigate a codebase, you know what to expect from a certain class, it makes onboarding newcomers easier, quicker, and less confusing” etc. 

#
### Different classes have different responsibilities and that's why we separate them with different names and different files. But that doesn't mean they are completely independent, every class have more or less relationships with other classes, together they form the complete application. For example in my diagram, the Board class have associations with all of the other classes, it is responsible for creating the dice, ui, players, tiles, and run the main game loop. The Player class has dependency with the Tile class and the Dice class, Ui class has dependencies with the Human player and Tile class. The Player object can use dice as a dependency, since it receives the dices from another class and doesn’t create the dices itself. As nirajrules saying in his article “Association vs. Dependency vs. Aggregation vs. Composition” about “Dependency indicates that you may invoke one of the APIs of the received class reference.” with the dependency injection you can easily change the inject objected at the runtime, as Bhavya Karia mentioned in her article “A quick intro to Dependency Injection: what it is, and when to use it” with “a class should depend on abstraction and not upon concretions (in simple terms, hard-coded).” 

#
### The class diagram contain, methods, attributes, interfaces and the relationships between the classes etc. You may have a general understanding of the interactions among the classes by looking it, while at the object diagram will show how objects in your system are interacting with each other at some point in time and what value those objects contain. It may be a little be hard to understand the whole process without the help of the class diagram. The sequence diagram show how the objects are used to perform in a sequential order (steps by steps), sequence diagram are time focused and show the interaction between the objects.

#
### There are lots of thing I can improve in my diagram, The most different between my diagram and teacher is he used a circular double linked list to implement the Tile class, I didn't use this method and I thought I could solve it by just using a loop just like the ant task in the assignment 1. Well, it is always good to learn new methods after all! Except this, I think I have tried my best with my task and it doesn't look as bad as I thought, what´s the most important thing for me is how to make good structure before I draw the diagram. For example how many classes do I have to qualify for the application and what kind of relationships that the classes has, and how classes should better interact with each other etc. It´s always good to have a design diagram, with the help of it, I won't get lost during the coding time by following the diagram and it would help me to explain my thoughts to other people.

#
### 
Sources：
https://pspdfkit.com/blog/2018/naming-classes-why-it-matters-how-to-do-it-well/

https://nirajrules.wordpress.com/2011/07/15/association-vs-dependency-vs-aggregation-vs-composition/

https://www.freecodecamp.org/news/a-quick-intro-to-dependency-injection-what-it-is-and-when-to-use-it-7578c84fa88f/

https://www.ibm.com/support/pages/difference-between-object-model-diagram-and-class-diagram-rational-rhapsody
