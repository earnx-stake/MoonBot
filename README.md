# EarnX-Moon-Bot
EarnX-Moon-Bot is a Telegram bot developed by EarnX team with the aim of helping Moonbeam community keep track of delegations, rewards and other variables of the blockchain. It's very common to verify your wallet address twice a day to check if the staking rewards was distributed or even if your collator is in the active pool set. Using EarnX-Moon-Bot you can easily receive these notifications wherever you stay.

Please find the bot on Telegram as @earnx_moon_bot (MoonBot).

**List of commands:**

1. /start: initialize the bot;
2. /help: list of the available commands;
3. /setAddress num address: register a Moonbeam address with the num id. The num can be in the range 1 to 5, that means you can track up to 5 addresses;
4. /balance num: shows the balance of a Moonbeam address with the id num;
5. /listAddress: lists the Moonbeam addresses registered;
6. /checkDelegations num: check delegations for all collators associated with the address num;
7. /alarmBalanceTarget num value: configure an alarm that will trigger in threshold value to the Moonbeam address associated with de id num;

You need to use the /setAddress command to associate the id num (1 to 5) to your Moonbeam addresses, so you can refer them on the other bot commands.

## Use-Cases

1. How do I know if I continue receiving rewards? <br />
Resp: You can execute a /checkDelegations to verify the status of all of your delegations and the following info is showed: 
- collator name; 
- the GLMR staked; 
- if the collator is in the active set; 
- your position in the delegator list; 
- if you are receiving rewards and the percentage of your GLMR allocated in each collator in case you have more than one. <br />
Besides that, you can also set an alarm to notify you whenever you stop receiving rewards regardless of the reason.

2. How do I know if my collator is in the active pool set? <br />
Resp: You set an alarm to notify you whenever you stop receiving rewards, and one of the reasons is the collator be kicked out of the active pool set. Executing /checkDelegations also shows this info, but setting an alarm is better because there is no need to take time to verify in the blockchain.

3. How do I know if I have enough GLMR in my Address? <br />
Resp: You can execute /alarmBalanceTarget to receive a notification when you balance reaches a threshold defined by you.


PS: It's important to highlight that all informations that the bot handles are already public in the blockchain.
