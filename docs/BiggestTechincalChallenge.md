# What is your biggest challenge and how did you solve it?

### Situation: 
This is situation is about supporting a team that is refusing to move to a newer technology stack.

### Task: 
As a team lead, onoe of the most challenging task that I had to do was to convince the development team to move to a different technology stack.
In my case, we wanted to move from a managed EC2 cluster to a unmanaged EC2 cluster. I tried mentioning why we had to move verbally but it wasn't getting any traction. Things remained the same.

### Action: 
I did manage to convince the team to move to a different better stack and this is how I did it:
- build python tool to show price comparison
- build the entire environment to replicate the proposed change
- build a pipeline to deploy app code in to the proposed env
- show an extensive benefits vs disadvantes table

SHOW DEMO [HERE](https://github.com/stashedUp/tomo-documenting-architecture-decisions)

### Result: 
- The development team was more inclind to move to the newer stack 
- SRE and developer are working collaboratively to push the performance of the infrastucture.

### Lesson:
- It's often hard to move from one system that is currently working and has been working.
- But if we don't make the effort to progress and keep our application uptodate. It would become harder and harder to maintain it.
- It's important to see from the development team's perspective
- Showing price comparison and showing a proof on concept helps 
- It shows the stakeholder that we have confident and it's not all theorical