# Employing multiagents to collaborate, pose, discuss and answer questions

## What is an *Agent*?
Large language models are driven by conversation. Such an interaction is typically between a human and an LLM. In cases where we cannot have a human conversing with an agent to obtain responses to questions, we desire that the LLM operate autonomously and insert and answer questions by itself.
<br>
An LLM that can operate without constant user input, can use tools (calling an API, posting content, gathering datapoints etc) and can optionally manage other LLMs is known as an agent. A number of such self-sufficient agents that do not need constant supervision are known as *MultiAgents*.
<br>
Each Agent in the above group can be customized to perform a single task where each agent can run on a different LLM model ([ChatGPT](https://chatgpt.com/?oai-dm=1), [Mistral](https://auth.mistral.ai/ui/login?flow=517612c2-b660-42a5-8f7d-43cfaff68dbc) etc). Every such agent typically has a role, a goal and a backstory. The role-playing aspect of the LLM allows it to better understand its function and the context of the conversation while the goal mentions the end output that is required by the user. Different tasks can be given to an agent. As the crew operates on the tasks sequentially, the order of the tasks is important when being fed to the LLM. 
<br>
Below are some of the various tasks that can be performed/automated by MultiAgents. The corresponding code can be run on Colab or on Jupyter Notebook. An API key is needed to access the LLM being used. The requirements.txt contains the necessary libraries and the utils.py contains the functions that are needed to call and load the API key that has been stored as a .env file. 

# Tasks

1. Creating an agent to research and write an article
    A Content Planner, Content Writer and an Editor are built as the 3 agents that are responsible to research and write an article for a blog post. The Content Planner works on planning the blog article, the topic and collecting information that can help the Content Writer write the article. The Editor reviews the blog post and provides opinions when needed.

2. 

