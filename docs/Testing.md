# Testing

# Test Driven Deployment

- For the vast majority of us, unit tests were short bits of throw-away code that we wrote to make sure our programs “worked.”
- The problem is that tests must change as the production code evolves. 
- The dirtier the tests, the harder they are to change. 
- The more tangled the test code, the more likely it is that you will spend more time 
cramming new tests into the suite than it takes to write the new production code. 
- As you modify the production code, old tests start to fail, and the mess in the test code makes 
it hard to get those tests to pass again. So the tests become viewed as an ever-increasing liability.



- If you don’t keep your tests clean, you will lose them. 
- And without them, you lose the very thing that keeps your production code flexible. 
- It is unit tests that keep our code flexible, maintainable, and reusable. 
- The reason is simple. If you have tests, you do not fear making changes to the code!

### Unit tests
- A unit test is the smallest and simplest form of software testing. 
- These tests are employed to assess a separable unit of software, such as a class or function, for correctness independent of the larger software system that contains the unit. 
- Unit tests are also employed as a form of specification to ensure that a function or module exactly performs the behavior required by the system. 

### Integration tests
- Software components that pass individual unit tests are assembled into larger components. 
- Engineers then run an integration test on an assembled component to verify that it functions correctly. 
- A common example of a dependency injection is to replace a stateful database with a lightweight mock that has precisely specified behavior.
- I personally have used docker-compose to mock a postgress database and the application itself

### System tests
- A system test is the largest scale test that engineers run for an undeployed system. 
- All modules belonging to a specific component, such as a server that passed integration tests, are assembled into the system. 
- Then the engineer tests the end-to-end functionality of the system.
 - Smoke tests
 - Performance tests
 - QA tests
 - Regression test

### Key 
Take away - Don’t comment out failing test. Delete it if it’s not relevant or refactor the test.
- Keep the build and test process short
- Speed is essential because there is an opportunity cost associated with not delivering software. 
- Delivering fast is also important because it allows you to verify whether our features and bug fixes are really useful.

SEE - Builing and deploying
