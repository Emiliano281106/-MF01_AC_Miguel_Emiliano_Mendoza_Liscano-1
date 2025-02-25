# Evaluación Continuada/Emiliano Mendoza

# REACT

## Hooks

- **What does it do?**
  
  * useState: manage `SIMPLE` variables and literal objects. Tracks the variables state.
  * useRef: `STORES` data betwween renders, ensuring it `PERSISTS` across renders. It can be used to store a mutable value that does not cause a re-render when updated.
  * useMemo: same as useRef but is better for handling complex operations.
  * useContext: `SHARES` data between `COMPONENTS`. We use it when different componenets need access to the same value.
  * useReducer: manage `large` volumes of objects, is like the "enhanced" version of the useState.
  * useEffect: `SYNCS` with actions(dependencies).

- **Syntax**
  
  - useState:
    
    ```jsx
    const [state, setState] = useState(initialState);
    ```

- useRef:
  
  ```jsx
  const ref = useRef(initialValue);
  ```

- useMemo:
  
  ```jsx
  const cachedValue = useMemo(calculateValue, dependencies)
  ```

- useContext:
  
  ```jsx
  const value = useContext(SomeContext)
  ```

- useReducer:
  
  ```jsx
  const [state, dispatch] = useReducer(reducer, initialArg, init?)
  ```

- **Dispatcher**: function that sends an action to the reducer.

- **Reducer**: function that determines how the state should change in response to a given action and return a new state.

- **Action** : literal object with a field type thst describes the action, and other fields that contain the payloads.

- useEffect:
  
  ```jsx
  useEffect(() => {
  // code to execute
  return () => {
  };
  }, [dependencias]);
  ```
- If [] is empty, runs only once after first render.
- If [dependencies], runs after any of them changes.
- If don't specify, runs after every render.

## KEY CONCEPTS/TOOLS

### Render Cycle

The **Render Cycle** in React consists of three phases to efficiently update the UI using the **Virtual DOM**.  

- **Trigger Phase** → A re-render occurs due to changes in **state, props or events**. No user code runs at this stage.  
- **Render Phase** → The component function executes, generating a **new Virtual DOM** to compare with the previous version (**Reconciliation**).  
- **Commit Phase** → The **Real DOM updates**, side effects run, and references are updated.  

### Render virtual DOM

#### Definition:

The Virtual DOM is a copy of the Real DOM that helps update web pages more efficiently.

#### What it does:

Makes web apps faster by reducing direct updates to the Real DOM.

#### How:

- **Component Renders** → React creates a new Virtual DOM when data (state) changes.  
- **Reconciliation** → React compares the new Virtual DOM with the old one to find changes.  
- **Updates** → Only the changed parts are updated in the Real DOM, making it faster.  
- **Re-Rendering** → The process repeats when data changes again.

### React Router DOM

 **library for managing navigation** in React applications. It allows developers to create **single-page applications (SPAs)** with multiple views, enabling smooth transitions between pages without re-rendering the entire app.  

### Handlers (event managers)

- Runs when an event occurs(onClick, onChange...).

### Axios

**Axios** is a library for making HTTP requests, commonly used for API communication.  

* Automatically handles JSON responses 

### .JSX

 Is a syntax extension for JavaScript that lets you write HTML-like markup inside a JavaScript file.

**STRENGTHS:**

* **JavaScript Integration** – You can embed JavaScript expressions directly within JSX using `{}` for dynamic content.

* **Improved Readability & Maintainability** – JSX makes UI code more intuitive by closely resembling HTML, making it easier to read and manage.

# JAVA

## BASIC CONCEPTS

* **Model**: represents the data and the business logic of the application.Communicates with database.

* **Controller**: responsible for handling incoming requests and mapping them to the appropriate logic in the model and view.

* **JPA**: allows to interact with databases using **Java objects** instead of writing raw SQL queries(translates java into database language).

* **Service**: acts as an intermediary that manages, organizes, and facilitates communication between clients and a backend system. It receives requests, queues them if necessary, and ensures they are processed efficiently.

## JPA

### Dependency inyection

 Allows objects to receive their dependencies from external sources rather than creating them internally.

### Annotations:

* `@RestController`: This annotation is used to define a class as a RESTful web service controller.

* `@Service` : This annotation is used to define a class as a service class that defines the business logic.

* `@Autowired`:  manages the whole life cycle of the object.

* `@Entity`:  used to define a class as a **JPA entity**, which can be used to interact with a database.

* `@RequestMapping`: This annotation is used to map HTTP requests to specific methods in a controller class.

* `@Id`: Specifies the primary key field of the entity.

* `@JoinColumn`:    Specifies the join column when using a relationship.

* `@OneToMany`:    Defines a one-to-many relationship between two entities.

* `@ManyToOne` :  Defines a many-to-one relationship between two entities.

* `@ManyToMany ` :  Defines a many-to-many relationship between two entities.

* `@JoinTable` :   Specifies the join table for a many-to-many relationship.



### Relationships:

**Steps to create one:**

1. Define the relationship, the direction of it and the owner.

2. Choose annotations

3. Use `@JoinColumn` or `@JoinTable`

4. Set up annotation, using `mappedBy`,`cascade`...



**Types:**

1. **`@OneToOne`**: Represents a single-valued association where an instance of one entity is related to a single instance of another entity.

2. **`@OneToMany`**: Represents a multi-valued association where an instance of one entity can be related to multiple instances of another entity.

3. **`@ManyToOne`**: The inverse of `OneToMany`, where multiple instances of an entity can be related to a single instance of another entity.

4. **`@ManyToMany`**: Represents a multi-valued association where multiple instances of one entity can be related to multiple instances of another entity.
- They can be either `unidirectional` or `bidirectional`:

- **Unidirectional**: Only one entity has a reference to the other.

- **Bidirectional**: Both entities have references to each other.



**Attributes:**

* **cascade**: Specifies which operations should cascade to child entities. Options include `ALL`, `PERSIST`, `MERGE`, `REMOVE`, etc.

* **mappedBy**: Specifies the field that **owns** the relationship in the child entity.



## MOOC

* Java programming 1 completed

## MY PROJECTS:

- **WeatherApp API info** [WeatherApp](https://github.com/Emiliano281106/weather-app-API).
- **Practice ManyToMany(JoinTable)** [Library](https://github.com/Emiliano281106/Library2.0).
- **Airport-Spring** [Airport](https://github.com/Emiliano281106/Airport-Spring).

# DevOps

I learned basic git and linux commands, I made hand-written notes about them.

![](/home/emiliano/Pictures/IMG_6397.jpeg)

![](/home/emiliano/Pictures/IMG_6397.jpeg)

<img title="" src="file:///home/emiliano/Pictures/IMG_6399.jpeg" alt="" width="651">

# SCRUM

## WHAT IS IT?

**Scrum** is a framework for managing projects, focusing on **teamwork**, **accountability**, **transparency**, and iterative progress towards a clear goal. It enables teams to address **complex adaptive problems** while delivering high-value products creatively and productively.  

At its core, Scrum is a simple yet powerful framework for effective **team collaboration** in developing complex products.

## PILARS

- **TRANSPARECY**: this means showing the facts exactly as they are.
- **INSPECTION**: check your work as you do it.
- **ADAPTABILITY**: continous improvement based on previous inspection.

## KEY CONCEPTS (so far)

- ### IMPEDIMENTS
  * It is those habits/behaviours that stop me from being productive. **THEY ARE OPPORTUNITIES NOT OBSTACLES**
- ### METRICS
  * Tool used to measure my progress, helps to identify wether I'm achieving my goals or not, and also areas where's room for improvement
- ### NEGATIVE LOGIC
  * Getting rid of toxic/non-benefitial habits rather than focusing on implementing `new` ones. "First, don't subtract, and then start adding."
- ### COMMUNICATION
  * Effective
  * Concise
  * Deliver value
  * Charisma = high warmth + high competence.
  * On the same page = where a group sees and generally agree or understand the same situation.
- ### COLLABORATION
  * Open and effective communication
  * Working towards the same goal
  * Sharing responsabilities
- ### PLANNING
  * Time-blocking
  * High-mid-low energy
  * Prioritize
  * Getting things DONE (execute!!!!!!)
- ### USER STORIES
  * Simple description of a software feature from the user's perspective. Highlights what the user wants to achieve.
- ### SMART WORK > HARD WORK
- ### MINDSET

## MY ROADMAP(5 WEEKS)

- [**ROADMAP**](https://github.com/Emiliano281106/ROADMAP)

# TOOLS I LEARNED:

* **git**
* **github**
* **Linux console**
* **markdown**
* **intellijidea**
* **visualStudio**
