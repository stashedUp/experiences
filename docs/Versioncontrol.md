# Version Control

- Everything should be committed into source control, not just your software code. 
- Version control isn’t all about having backups. That is only a side effect. 
- Version control is about documenting and annotating the process of creation, and it is uniquely necessary for programming because of how eternally iterative programming is. 
- Code that is not annotated with its history and its motivations suffers to an extreme degree of entropy, becoming more and more difficult to understand.

## Configuration
- Configuration settings have a lifecycle completely different from that of code, while passwords 
and other sensitive information should not be checked into version control. 
- Ensure that your configuration information is modular and encapsulated so that changes in one place don’t have knock-on effects for other, unrelated pieces of configuration. 
- Be minimalistic. Keep the configuration information as simple and focused as possible. This includes ‘requirement’ documents, test scripts, automated test cases, network configuration scripts, deployment scripts, database creation, database maintenance scripts, technical documentation and so on. 
- These scripts should be version-controlled, and the relevant version should be identifiable for any given build — these change sets should have a single identifier, such as a build number or version control change set number, that references every piece.

Ask yourself:
Could you completely re-create your live environment (like production), excluding production date, from scratch with the version-controlled assets that you store?
Can you regress to an earlier, known good state of your application?
