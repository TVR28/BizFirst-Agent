## Initial Prompt
Prompting Technique - Role Prompting\
Model - Claude Sonnet 3.7 Thinking

```text
You're an experienced AI Engineer who've built generative AI applications from inception to production using AI Agents, with custom tools and agent communications (MCP). Generate me an entire project plan for the below AI project idea. Make sure the project plan consists everything required to start such a project from scratch till deployment and ready for users. Keep the main emphasis on AI Agents.

Generate a README.md file and add the entire project plan to it.

I want to build an application that uses production grade AI Agents that can take a PDF form which consists of a tax payers information (like text, numerical, boolean, date, duration, SSN, driver's license number, etc.,). Now when a user uploads this pdf using my web application, it starts the AI agent process, where an AI Agent that interacts with the users by asking questions like a human and collecting information, and putting it properly in MongoDB database. We'll be deploying this application in Azure

The agent's conversational flow should feel natural, where even if the user wants to visit some of the previous questions and needs to correct his/her answers or information, then the agent should be able to handle that flow and return to the current phase. All of this should happen in natural language english texts like a human conversation.

The tech stack I'm plannign to use is MEAN stack
MongoDB, Angular, Express and Node.js.. deployment in Azure, and I'm looking for opensource tools /frameworks to build AI Agents.
```

## Follow-up prompt:
Prompting Technique: Step-Back and few-shot prompting (for better reasoning)\
Model - Claude Sonnet 3.7 Thinking
```text
Take a step back and think about the project. I'd like the project to be the following way:
- We'll have a web application (conversational interface like ChatGPT) built using the MEAN stack.
- A user uploads a PDF (which can consist tables, columns, images, checkboxes, text, numbers, SSN info and more of tax related stuff required by a CPA)
- Once the user uploads the PDF, I need that to be parsed by the best PDF parsing mwthod/tool currently used by top companies in production.
- The questions and respective answers/information in the PDF should be used to create an AI agent, which will now be responsible for asking the user the questions and getting information from him and implement conditional branching on it's own, collect respective information and store in our MongoDB database.
- The agent should ask natural language questions and should understand and derive answers based on user responses.. the conversation should depict a human like conversation where the user can simply ask follow-ups, but the agent has context of the conversation so it understands users intent and responds accordingly.
- Once the agent conversation is started, and the user wants to re-visit to change some of the information for the previous questions, he should be able to do that simply using natural language responses. like
Assistant: "Okay now since we're done with W2, let's move on to property taxes. Do you have any properties to pay tax for?"
User: "Actually, I forgot that I had one more W2 form for just 6 months.. can we add that as well?"
Assistant: "Absolutely, let me go back and add your W2 information. Can you tell me the empler details, your information, and more...".
As mentioend above, the agent should be capable of visiting to any question in point of time on its own based on user responses and queries.
- The agent should be provided with tools to implement the above mentioned tasks.
- Finally, it should provide a snapshot or summary of what all the details it collected from the user, and ehat are still left (if any).
- Then all of this information should be stored in MongoDB (need a seperate tool for that) based on user information.
- Remmeber all of this application should be deployed on Azure.

Now revisit the above prompt again and re-think and reason through it to understand the workflow and agent duties better. Then proceed further and write a very well documented EADME.md file with the project steps, sub steps, workflow, pipeline/architecture, tools needed, step-by-step implementation.
```
