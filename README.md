# PromptEngineering

![image](https://github.com/user-attachments/assets/ea87be4a-587c-48ea-975d-5661a454b180)

To test out the api the LLMS provide a playground to test out the apis 

![image](https://github.com/user-attachments/assets/ad68f46d-bda6-4b68-997f-7b747ec5e3f6)

![image](https://github.com/user-attachments/assets/18ae70ac-a4af-4df9-8a86-f1cb42062f32)

![image](https://github.com/user-attachments/assets/136ea63b-e82b-40cf-8ea4-0a2235abd1c7)

use : Either Temperature or Top P 
      Either Maximum length or stop sequence
      Either Frequency penalty or pressence penalty 

Top p or Temperature is jist for making sure the response is creative and is not repatative i.e increasing randomness and not relying on just facts 

these are setting u can set via interacting with the LLM as an API 

![image](https://github.com/user-attachments/assets/df041fd1-ef22-4584-b10c-9b22eb49c163)

Here system is the persona like who are you what role are you in (like i am a software engineer) 

User is the response that has to be returned for that prompt in system 

Assistent is the response you want the model to give back 

![image](https://github.com/user-attachments/assets/bc17e904-30dd-4d40-9680-c2ee19eadabe)

So when giving prompt these are the four Prompt Elements to keep in mind 

Instruction : What u want to do 

Context : for whom or onbehalf of whom what role (software engineer or doctor etc) 

Input date : The input you want to give 

output Indicator or Format : Json , CSV , excel etc 


## Prompt Engineering Techniques 

This shoting technique is only for Q & A types 

- Zero Shot prompting :
- One shot prompting :
- Few Shot prompting :

  ![image](https://github.com/user-attachments/assets/c886f957-8d8f-497e-ac0f-9dfdcbca93c0)


But for logical and Mathematical Reason the above Method fails Like 

- If you give a series of In tegration question with solution and finally as a Integration question the ai wont give correct answer as the computational logoc for that is different

- For this reasoning , mathematical and  logical task we use the

# Chain of Thought Prompting Technique (COT) Chain of Thought 

Explain your thought process for a problem with its solution and ask for a similar problem it solves it perfectly 

But COT fails for aptitude and reasoning like for complex ones So we use 

# self consistency 
 
![image](https://github.com/user-attachments/assets/4b81bf3b-f187-4003-8e22-4952c35e27d9)

![](https://arxiv.org/abs/2203.11171)

# Out of Date Prompting (for llms have trained upto only so and so date) 

To ask about present match can give commentary from cricbuzz and do the needed prompt to get info ot that match 

![image](https://github.com/user-attachments/assets/3a0d2bae-de8b-4110-9b79-5f04ea5f8ca1)

# Role Play Prompting ( Role Playing ) 

Since LLM is super inteligent it knows about all domain so role Playing is important to tailor your response with respect to your domain 

Three Steps in this way of prompting 
1) Role Assignment : Ex: Your are an experienced Doctor   Ex : Your are Experienced devops engineer
2) Actual Question you want to ask for
3) Output Instruction : Means in what format you want the output as like csv or just plain response explaination text Ex : Programming Language means which language and which package

 Ex: answer in yes or no format or json format etc

 Ex: You are an experienced software engineer . I want to generate QR code for website . Provide the code in Javascript with step by step explaination 

 You are an experienced software engineer . => Role Assignment 
 
I want to generate QR code for website . => Actual Question 

Provide the code in Javascript with step by step explaination  => Output Instruction 

Ex2 : You are experienced script writer . I want script for a youtube video on chatgpt . Make it engaging with hooks and interesting elements 

# RAG Prompting 

- Retrieval Augumented Generation (RAG)
- Generation as LLMs generate the response Augumented as they add some things in the response Retrieval maans get some data
- LLMS work based on the context

- So to your LLM for your Companie Queries chatbot Obviously LLMS wont be trained with your company data so you can use RAG prompting there 
- We have to add out company data for LLMS context

- We first retrive Company data
- then we augument or add that company data in our prompt
- Finally with this augumented prompt we generate our required response


  ![image](https://github.com/user-attachments/assets/78dc7a48-0d03-4284-b5e8-a8b438e3ca2e)

  Retrival => Involves
  1)Data source
  2) Indexing the data
  3) Querying
  4) Ranking

  RAG is used when ur using LLM through APIS

  we retreive data from external data source , we augument that with our prompt and finally generate the response using that prompt through the LLMs apis

  But using RAG we provide additional context that LLMs are not trained with ( and LLM dont have this info ) 

  Through UI means can use out of data Prompting

  Implementation
  - with Langchain (Python)
  - without Langchain (Python)


whats next ? 

- AutoPrompting
- ReAct prompting
- LangChain
- In Hugging Face Learn about transformers and Transformer models 



For ReAct Prompting read this : 
[](https://x.com/i/grok/share/0Wdny6n1hLRRlRM6EodOACwU3)

We can never create a LLM like chat as the train cost is very expensive in  terms of resources 

SO more than learning AI/ML , Learning LangChain is beneficial 

LangChain is open-source framework to build applications using LLMS (Large Language Models) 

![image](https://github.com/user-attachments/assets/207ad028-0050-438c-8ceb-f19d63d02c5f)

Langchain abstracts the complexity of interaction of multiple apis happening one after the other in a specified sequence 

Langchain Deals with LLMS , Prompt templates 

Using Langchain can create chains and Agents as well 

Agents automate things like by creating workflows allowing to automate the sequence of data and responses between mutliple apis 

![image](https://github.com/user-attachments/assets/7e87da67-ce89-47f2-9b99-52e09a011ac3)



Conclusion 

# The More Step by Step prompt you give to LLMS , you will get a better results for it 

- prompt => 1) Persona
            2) Task - that what work need to be done  
            3) Context - what are the things . what is going to happen
Example: Your are a witty social media expert Give me a funny instagram caption about happily coding 12 hours straight

 Your are a witty social media expert => Persona
 Give me a funny instagram caption => Task 
about happily coding 12 hours straight => Context

Now with this prompt GPT knew what had to be done, when ,what are writing the psot for 

This is called Multi step prompting that works on persona , task and context

Noe you can compare the generative AI with mimicry artist , the more you teach it , the better context you give it . you will be getting better 
output

So Persona , Task and Context are like buidling blocks for an effective prompt 

Also Adding this line " Lets think step by step " in the prompt also proves to be effective in terms of results 


Ex : What's the meaning of life 
     Let's Think Step By Step 

Prompt engineering is not about complexity its about how simple you keep the prompt 

How simple can you divide the task/it into multiple steps, 
Tell about it , you can explain your problem and if your able to tell the type of result you want then you will get to see better final results 

For Beginners Just focus on two things 

1) Multi Step Prompting as mentioned Above

2) Adaptive prompting

In Adaptive Prompting , You need to add a little more context with existing information 
with the help of which , ChatGPT or any LLMs can analyse the information in an even better way 

it will be able to fix the problems and give you good output 



 

 

  


