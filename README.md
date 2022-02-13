# MoonBot
MoonBot is a Telegram bot developed by EarnX team with the aim of helping Moonbeam community keep track of delegations, rewards and other informations of the blockchain. It's very common to verify your wallet address twice a day to check if the staking rewards was distributed or even if your collator is in the active pool set. Using MoonBot you can easily receive these notifications wherever you stay.

We see on Moonbeam Discord almost everyday delegators trying to figure out why did they stop receiving rewards. The answer is very long and we embedded all the possibilities in just one notification in the Moonbot, make the delegations life easier. Besides that we developed other functionalities of great value to Moonbeam Community.

Please find the bot on Telegram as @earnx_moon_bot (MoonBot).

**List of commands:**

1. `/start`: initialize the bot;
2. `/help`: list of the available commands;
3. `/setAddress num address`: register a Moonbeam address with the num id. The num can be in the range 1 to 5, that means you can track up to 5 addresses;
4. `/balance num`: shows the balance of a Moonbeam address with the id num;
5. `/listAddress`: lists the Moonbeam addresses registered;
6. `/checkDelegations num`: check delegations for all collators associated with the address num;
7. `/alarmBalanceTarget num value`: configure an alarm that will trigger in threshold value to the address associated with num;
8. `/alarmBalanceChange num`: configure an alarm that will notify you every time the balance of the address num changes
9. `/alarmRewards num`: configure an alarm that will notify the address num whenever you stop receiving rewards regardless of the reason
10. `/cleanAlarmBalanceTarget num`: delete the AlarmBalanceTarget alarm configuration of the address num;
11. `/cleanAlarmBalanceChange num`: delete the AlarmBalanceChang alarm configuration of the address num;
12. `/cleanAlarmRewards num`: delete the AlarmRewards alarm configuration of the address num;

You need to use the `/setAddress` command to associate the id num (1 to 5) to your Moonbeam addresses, so you can refer them on the other bot commands.

## How to use the MoonBot

1. How to register my Moonbeam address?

  `/setAddress 1 <myaddress>`

2. How to list my registered addressed?

  `/listAddress`

3. How to check the status of all delegations of my address 1?

  `/checkDelegations 1`

4. How to configure an alarm to send me a notification when my balance of the address 1 change?
  
  `/alarmBalanceChange 1`
  
5. How to configure an alarm to send me notification when I stop receiving rewards of the address 1?
  
  `/alarmRewards 1`
  
6. How to configure an alarm to send me a notification when my balance reach a threshold of 100 GLMR?
  
  `/alarmBalanceTarget 1 100`

7. How to clean an alarm of Balance Change of the address 1?

  `/cleanAlarmBalanceChange 1`

## Use-Cases

1. How do I know if I continue receiving rewards? <br />
Resp: You can execute a `/checkDelegations` to verify the status of all of your delegations and the following info is showed: 
- collator name; 
- the GLMR staked; 
- if the collator is in the active set; 
- your position in the delegators list; 
- if you are receiving rewards and the percentage of your GLMR allocated in each collator in case you have more than one. <br />

**Besides that, you can also set an alarm to notify you whenever you stop receiving rewards regardless of the reason.**

2. How do I know if my collator is in the active pool set? <br />
Resp: You set an alarm to notify you whenever you stop receiving rewards, and one of the reasons is the collator be kicked out of the active pool set. Executing `/checkDelegations` also shows this info, but setting an `/alarmRewards` is better because there is no need to take time to verify in the blockchain.

3. How do I know if I have enough GLMR in my Address to use for example in a DeFI operation? <br />
Resp: You can execute `/alarmBalanceTarget` to receive a notification when your balance reaches a threshold defined by you.

4. What happens if my collator was kicked out of the active pool set just for a couple of rounds?
Resp: To deal with this situation, you have to set an `/alarmRewards` to your address. When the first collator go out of the active pool, you will receive a notification. So you can execute a revoke without lose time. Two rounds after that, your collator come back to the active pool set. So you will receive another notification warning that you begin receiving rewards again. In this case, you can decide to cancel the revocation.

5. What happens if I staked GLMR in two collators and both were kicked out from the active pool set?
Resp: You set an `/alarmRewards` and whenever you stop receiving rewards regardless of the collator you will receive a notification. And when both collators come back to the active set you will receive a notification that you begin receiving rewards again. 


PS: It's important to highlight that all informations that the bot handles are already public in the blockchain.
