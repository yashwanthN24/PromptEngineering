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










