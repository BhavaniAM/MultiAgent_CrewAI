# Employing Multi-Agents to collaborate, pose, discuss and answer questions

## What is an *Agent*?
Large language models (LLMs) are driven by conversation. Such an interaction is typically between a human and an LLM. In case we cannot have a human conversing with an agent to obtain responses to questions, we desire that the LLM operate autonomously and pose and answer questions by itself.
<br>
<br>
An LLM that can operate without constant user input, can use tools (calling an API, posting content, gathering datapoints etc) and can optionally manage other LLMs is known as an agent. A number of such self-sufficient agents that do not need constant supervision are known as *Multi-Agents*.
<br>
<br>
Each *Agent* in the above group can be customized to perform a single task where each agent can run on a different LLM model ([ChatGPT](https://chatgpt.com/?oai-dm=1), [Mistral](https://auth.mistral.ai/ui/login?flow=517612c2-b660-42a5-8f7d-43cfaff68dbc) etc). Every such agent has a role, a goal and a backstory. The role-playing aspect of the LLM allows it to better understand its function and the context of the conversation while the goal mentions the end output that is required by the user. Further, every agent perferably handles a different task and in combination the multiple agents complete the total task specified by the user in the initial prompt. As the crew operates on the tasks sequentially, the order of the tasks that is fed to the large language model is important. 
<br>

## Usage 
The corresponding code in the directories can be run on Colab or on Jupyter Notebook. An API key is needed to access the LLM being used. The requirements.txt contains the necessary libraries and the utils.py contains the functions that are needed to call and load the API key that has been stored as a .env file. 

## Utility of Multi_Agents
1. **Creating an agent to research and write an article:**
   <br>
    A Content Planner, Content Writer and an Editor are built as the 3 agents that are responsible to research and write an article for a blog post. The Content Planner works on planning the blog article, the topic and collecting information that can help the Content Writer write the article. The Editor reviews the blog post and provides opinions when needed.

2. **Multi-agent Customer Support Automation:**
   <br>
   There are 2 different agents that are used to automate customer support: Senior Support Representative and Support Quality Assurance Specialist. The Senior Support Representative is responsible for providing full answers and be friendly to the customer. The Support Quality Assurance Specialist is responsible for verifying that the previous agent is prpviding the best support possible and making no assumptions. It can also delegate its work to another agent which might be better suited to complete the particular task. Multiple tools are specified to aid the agent in completing the tasks.
    - Serper dev tool - It is an external service that allows the agent to search Google for resources.
    - Scrape website - It is a single scraper to access a given URL and extract the contents
    - RAG - Performs semantic search over the contents of a website
  
3. **Customer Sales and Outreach**
   A Sales Representative agent is used to identify leads that match a customer's profile and analyze data, trends and interactions to unearth opportunities. The Lead Sales Representative agent is a bridge between the clients and the solutions that they need. There are instructions specified in markdown files for this task and are provided within the "instructions" directory. The task creates an in-depth analysis of a company to tailor the engagement strategy effectively.

4. **Event Planning Automation**
   The Venue Coordinator, Logistics Manager and the Marketing and Communication Agent are the three agents that are responsible for identifying and booking an appropriate venue, managing all the logistics for the event and effectively marketing and communicating with the participants. A Pydantic Object is used to store the venue details.

## Acknowledgement
Deeplearning.ai 
- Multi-Agent AI systems with crewAI 
