# Software Development Life Cycle 

## What is the typical software development life cycle?

1. Analysis and Planning
- How does this project connect to my company’s larger mission and goals?
- Do I have the people, tools, resources I need to take this on?
- Set timeline for the project
- Estimate the cost if possible (AWS cost)

2. Requirements
- Who’s going to use it and why?
- What sort of data input/output is needed?
- Will I need to integrate with other tools or APIs?
- How will I handle security/privacy?
- How will I scale?

3. Design and Prototyping
- It's not about how it looks and feel but it's about how it works
- Use lucid chart - whiteboarding

4. Software Development
- Actually do the work - write the code 

5. Testing
- This is built into the pipeline
- Unit test - functional test

6. Deployment!
- Deploy your feature/software
- Deploy through a pipeline
- automate everything

7.  
- the keyword is lifecycle, maintain a feedback loop
- maintain the deployable pipeline - encourage frequent deployment
- Set up observability pipeline
- set up alerts - for on-call

# How I write code
- I want to become an expert at Managing Complexity
- As a software developer, I see the world through the lens of software development. 
- We need to manage the complexity of the systems that we create as we create them, 
- and if we want to do this at any kind of scale beyond the scope of a single, small team, 
- we need to manage the complexity of the organizational information systems as well as the more technical software information systems

# WHen I write code I focus on these 5 aspects

- Modularity
- Cohesion
- Separation of concerns
- Documentation/abstraction
- Coupling

#### Modularity/Separation of Concerns
- is the degree to which a system’s components may be separated and recombined, 
- gives us the benefit of flexibility
- gives us the ability to test things seperately - test each function
- a design principle for separating a computer program into distinct sections 
- such that each section addresses a separate concern.
- gives us clarity and focus in our code and system
- useful for  dependency injection

#### Cohesion
- the degree to which the elements inside a module belong together
- you write function that help each other in the same class


#### Abstraction/Documentation
- Users of your service or API does not need to know how it works
- Users provide input and my API or function should provide the output
- Documentation plays a big part in this
- Talk about your documentation

#### Coupling
- Coupling is the the degree of interdependence between software modules
- much like creating microservices that talk to each other 
-we can scale it indepently 