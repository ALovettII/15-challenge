# 15-Challenge
 Combine AWS skills with Python to create a bot that will recommend an investment portfolio for a retirement plan.


## Technologies
Need set up before completing project:
* AWS Billing
* Amazon Simple Storage Service (Amazon S3)
* Amazon Lex
* Amazon Lambda
* AWS Identity and Access Management (IAM)


## Usage
You’ll accomplish the following main tasks:
1. Configure the initial robo advisor:
    * Define an Amazon Lex bot with a single intent that establishes a conversation about requirements to suggest an investment portfolio for retirement.
2. Build and test the robo advisor:
    * Make sure that your bot works and accurately responds during the conversation with the user.
3. Enhance the robo advisor with an Amazon Lambda function:
    * Create an Amazon Lambda function that validates the user's input and returns the investment portfolio recommendation.
    * This includes testing the Amazon Lambda function and integrating it with the bot.


#### RoboAdvisor Configuration**
**Slots**
| Slot Name | Slot Type | Prompt | 
| --------- | --------- | ------ | 
| firstName | AMAZON.US_FIRST_NAME | Thank you for trusting me to help, could you please give me your name? |
| age | AMAZON.NUMBER | How old are you? | 
| investmentAmount | AMAZON. NUMBER | How much do you want to invest? |
| riskLevel | AMAZON.AlphaNumeric | What level of investment risk would you like to take? (None, Low, Medium, High) | 

**Confirmation Prompt**
“Confirmation prompt” section, and then set the following messages:
Confirm: Thanks, now I will look for the best investment portfolio for you.
Cancel: I will be pleased to assist you in the future.

**Testing Bot Conversation**
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

**Final Cofiguration**
* Code Lambda Function
* Test Lambda Function with 'Test Events' found in Resources Folder
* Integrate your new Lambda function into the bot by selecting it in:
    * “Lambda initialization and validation”
    * “Fulfillment” sections.


## Bot Testing Recordings
Proper deployment of this proejct should yield the following results:

**Initial RoboAdvisor Testing**
![Initial RoboAdvisor Testing](https://github.com/ALovettII/15-challenge/blob/main/Recordings/initial_Bot.mov)

**Final Lambda-Enhanced RoboAdvisor Testing**
![Final Lambda-Enhanced RoboAdvisor Testing](https://github.com/ALovettII/15-challenge/blob/main/Recordings/enhanced_Bot.mov)


## Contributors
Created by Arthur Lovett
