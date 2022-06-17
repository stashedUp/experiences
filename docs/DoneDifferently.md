# What would you have done differently in a past project?

### Situation:
- The example that I am going to provide is technical one. 
- Each time we start working on a new project, we build the infrastructure with terraform. 
- Once the terraform build is successful, we build other higher environments
- The files and modules in terraform helps us build environment faster and 
- it allows us to use the same template for all environments including production 
- Over time, we add more complexity to the infrastructure and the managing the infrastructure code can become harder

### Problem:
- When we add more resources, we sometimes simple copy and paste the existing code while changing the name. 
- Overtime, we have many duplicates of the similar code
- This is bad practice
- As the complexity increases, maintaining these code becomes harder

### Solution
- One thing I would have done differently is to plan for complexity
- For example, when I create a shared module, I would ask myself how the file structure would look like if I added 100 more lambdas

### Lesson:
- Overtime, I have learned that we have to plan for complexity within our code as well - not just the infrastructure.
- On a later project, we modularied our terraform code so that resource files so that it can be shared 
- As a lead, I enforce keeping the code dry as much as possible
- MANAGING Complexiy

### Impact:
- When you keep your code in a way that it can scale, it will prevent messy code and unnecessary band aids
