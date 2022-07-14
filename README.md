# 15-Challenge
 Combine AWS skills with Python to create a bot that will recommend an investment portfolio for a retirement plan.


You’ll be asked to accomplish the following main tasks:
1. Configure the initial robo advisor:
    * Define an Amazon Lex bot with a single intent that establishes a conversation about requirements to suggest an investment portfolio for retirement.
2. Build and test the robo advisor:
    * Make sure that your bot works and accurately responds during the conversation with the user.
3. Enhance the robo advisor with an Amazon Lambda function:
    * Create an Amazon Lambda function that validates the user's input and returns the investment portfolio recommendation.
    * This includes testing the Amazon Lambda function and integrating it with the bot.


This section divides the Challenge instructions into the following three steps:
1. Configure the initial robo advisor
2. Build and test the robo advisor
3. Enhance the robo advisor with an Amazon Lambda function

For the submission, you will upload the following files to your repo:
* A Python script with your final Lambda function.
* Two short videos or animated GIFs that demo your robo advisor in action from the “Test bot” pane as requested

Sample Utterances:
* I want to save money for my retirement
* I'm {age} and I would like to invest for my retirement
* I'm {age} and I want to invest for my retirement
* I want the best option to invest for my retirement
* I'm worried about my retirement
* I want to invest for my retirement
* I would like to invest for my retirement

| Slot Name | Slot Type | Prompt | 
| --------- | --------- | ------ | 
| firstName | AMAZON.US_FIRST_NAME | Thank you for trusting me to help, could you please give me your name? |
| age | AMAZON.NUMBER | How old are you? | 
| investmentAmount | AMAZON. NUMBER | How much do you want to invest? |
| riskLevel | AMAZON.AlphaNumeric | What level of investment risk would you like to take? (None, Low, Medium, High) | 


Testing Bot Conversation
```text
 User: I want to invest for my retirement

 Robo advisor: Thank you for trusting me to help, could you please give me your name?

 User: Arturo

 Robo advisor: How old are you?

 User: 42

 Robo advisor: How much do you want to invest?
 
 User: 4000

 Robo advisor: What level of investment risk would you like to take? (None, Low, Medium, High)

 User: Low
 
 Robo advisor: Thanks, now I will look for the best investment portfolio for you.
 ``` 
