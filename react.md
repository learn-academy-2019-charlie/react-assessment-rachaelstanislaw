# React Assessments

Try your best to answer each question on your own before looking up the answer online. Once you're done writing your first answer, you can google the question and write the best answer you find.

#### 1. Here is a list of pros and cons to using the React library to build your application -- but some of them are false. Remove the false statements from the list:

- React was created to be simple, so that even people with minimal code experience could use it and create Single Page Applications (SPAs)
- React is a modern, efficient answer to complex UI applications
- React is a flexible library that plays the role of V in an MVC framework

 
 #### 2. What are "smart"(logic) and "dumb"(display) components? Explain the difference and also add why we bother to make the distinction between them.
 
 
 //Your Answer
Smart components hold the majority of the state of an app. smart components communicate with dumb components via props. Dumb components do not have much (if not any) state to manage and only display information.
 
 //Googled Answer
Using the container design pattern, the smart (or container) components are separated from the dumb (or presentational) components and each handles their own side of things. The smart components do the heavy lifting and pass the data down to the dumb components as props.
 
Dumb components themselves only have a render() method (they don’t need any others) and are often just Javascript functions. They don’t have internal state to manage. They wouldn’t know how to change the data they are presenting if they were asked. Ignorance is bliss.
 
#### 3. When we use "yarn add ..." in the terminal - what is yarn doing? And what file will always be automatically updated after we add a package with yarn?
 
 
 //Your Answer
 Yarn add adds dependencies to your project. The react app file is automatically updated.
 
 //Googled Answer
The package.json file is updated as well as yarn.lock
 
#### 5. There are three mistakes in this code that would cause it to break our application. Find the mistakes and fix them:

    import React, { Component } from 'react';

    class Recipes {
      constructor(props){
        super(props)
        this.state = {
          recipes: 
            {name: 'Meatballs'},
            {name: 'Mac & Cheese'}
      
        }
      }

      render() {
    
        return (
    
          let recipes = this.state.recipes.map(function(recipe){
            return(
              <li key={recipe.name}>{recipe.name}</li>
            )
          })
    
          <ul>
            {recipes}
          </ul>
        );
      }
    }

    export default Recipes;

#### 6. Name three html input types. (NOTE: text is the default type - so it doesn't count in this case)
 
 //Your Answer
 
 radio, button, checkbox
 
 //Googled Answer
 
 email, password, image
 
 #### 7. How would you explain state to a friend who doesn't know code?
 
 //Your Answer
 
 State is data that is integral to an app's functionality. For example, cars. A car could be a number of different makes and models, etc. However, every car has an engine, wheels, and a speed. The engine, wheels, and speed are all state. Different cars, like a Tesla or a Toyota, might have added features but they all at least carry the same state as a default car.
 
 //Googled Answer
 
 
 #### 8. What is the difference between component state and props? Your answer should include a short explanation of both.
 
 
 //Your Answer
 Component state is information that, like described above, contains vital information for a component, that can be passed to a child component. A "tesla" component will inherit all of the same state as "car" through props. This is because "car" is "tesla's" parent component. Props are inherited values. Child components cannotchange state directly. This must be done through a method that passes to the child, returns and outcome to the parent, and alters state indirectly. To elaborate, child components can reassign their own props through methods (for example, "tesla" may only have 2 doors), but it cannot alter the original "car" state of 4 doors.
 
 //Googled Answer
 Props and state are related. The state of one component will often become the props of a child component. Props are passed to the child within the render method of the parent as the second argument to React.createElement() or, if you're using JSX, the more familiar tag attributes.
 The parent's state value of childsName becomes the child's this.props.name. From the child's perspective, the name prop is immutable. If it needs to be changed, the parent should just change its internal state.
 and React will propagate it to the child for you. A natural follow-on question is: what if the child needs to change its name prop? This is usually done through child events and parent callbacks. The child might expose an event called, for example, onNameChanged. The parent would then subscribe to the event by passing a callback handler.
 The child would pass its requested new name as an argument to the event callback by calling, e.g., this.props.onNameChanged('New name'), and the parent would use the name in the event handler to update its state.


   
#### 9. Write a paragraph or so about your experience with building tic-tac-toe. Some topics to start with might be: things you learned about yourself, concepts from React that stood out to you, something about pair programming (if you paired), or the experience of building something in code from scratch.

I learned not to bite off more than you can chew. We went straight to Battleship and ended up wasting a lot of time just trying to figure out where to begin. When we took a step back and started at Treasure Hunt, we realized a lot of fundamentals that had been muddied by the overall scale of battleship. We were able to get back to basics, solving a small problem first, before expanding into a bigger project. 
I also really enjoyed learning about state and props. I felt like the concept was really interesting and luckily wasn't too terribly complicated (yet!). Once the idea of state and props really sunkk in, the framework for react started to make a lot more sense. It wasn't just arbitrary components, they actually all had a purpose. 
Our group communicated really well and I think we were all really proud of what we came up with in the end.