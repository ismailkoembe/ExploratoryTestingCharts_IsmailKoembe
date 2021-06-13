
# Exploratory test charters Nr:1 Analyze the Dashboard 
## QA Engineer : Ismail Koembe
## Timebox : 30 minutes
## Purpose, actors, setup, mission, tactic
Actor : Normal user (Community Version)
Setup: A most preferred iOS device, software version higher than 12.1.5, screen size 6,46 inches 
Priority : High because the dashboard screen and function represent all company efforts. 
Besides,in point of user view the dashboard is the most used part.

# Explore 
To evaluate if the dashboard function works correctly

# Resources 
In order to sniff the communication between client and server use Charles and configure proxy.
Other visual part will be tested manually by QA Engineer.

## To discover information

# Expected Output :
1. After installation Currency should match either preferred language or App Store country.
2. In first use, calendar set as monthly, should be daily.
3. A tool tips gives some hint regarding the app.
4. All (15) default Category Icon should visible in Dashboard
5. User should be able to submit its income for all free options.
6. All incomes should be represented in pay chart.
7. User should see all income records once taps charts.
8. User should see all expense records once taps chart slice or Balance tap.    
9. Since expenses are represented red colour, expense pages should have red header.
10. Submitted expense icon moves through dashboard.

# Actual Output : 
1. After each and every installation app starts with US dollar, even if user app store is not configured for US market.
2. Once user starts to use app, the default calendar set as "Monthly" and swiping for next or previous days does not 
   work. 
3. A tool tips guides user based on user behaviour.
4. Even though app has 15 categories for expense for community version, on Dashboard there are 14 icons and Billing icon
   is missing.Either tool tips could warn user or this icon also appear in dashboard. UI-UX references should be review 
   in order to understand it is BUG or Business decision.
5. Users can submit all kinds of expenses. The expense can be submitted multiple times ,and the user can see a total of 
   a particular expense. Moreover, in the Balance section user can see the quantity of expense and amount. Upon every 
   new expense submits, the pay chart should be updated ,and the user informed.
6. All expenses are shown in pay charts.
7. When user tabs pay charts or Balance, all income shown up in next page.
8. When user tabs pay charts or Balance, all expense shown up in next page.
9. In app green represents income and red represent expense. However, on Dashboard expenses are shown in green colour.
    UI-UX references should be review in order to understand it is BUG or Business decision.
10. Once user submit its own expense, expense icons moves in Dashboard randomly. Those icons can be sorted according
    the percentages. UI-UX references should be review in order to understand it is BUG or Business decision.


# Observations :
 Pay chart and balance calculation are tested and approved.

#Debriefing Information
#Defects / Bugs
Once app language is English (United States), negative numbers presented in parentheses without minus sign.
(It should be compared with business requirement and UI/UX design, then Bug ticket would be required)

#Conclusion / Notes
All mentioned suspicious behaviour in Dashboard should be review with UI-UX department and PM. 
After the review potentially new bug tickets would be created.


-----------------

# Exploratory test charters Nr:2 Analyze the Account Functions
## QA Engineer : Ismail Koembe
## Timebox : 45 minutes
## Purpose, actors, setup, mission, tactic
Actor : Normal user (Community Version)
Purpose : To evaluate if the app Categories and Account works as expected.
Setup: A most preferred iOS device, software version higher than 12.1.5, screen size 6,46 inches
Priority : High. The customization options are in high demand in terms of user perspective and domain competition.

# Explore
To evaluate if the Account functions work correctly

# Resources
In order to sniff the communication between client and server use Charles and configure proxy.
Other visual part will be tested manually by QA Engineer.

## To discover information

# Expected Output :
1. User should be able to add new accounts and specify emblem, name and initial balance of new account.
2. User should be able to delete existing accounts.
3. User should be able to transfer money between its own accounts.
4. User should not be able to transfer money for same account.
5. When transferring money from one account to another account, the amount of the transferred account should increase
    while the amount of the transferring account should decrease by the same amount.
6. Upon existing account deletion, the amount of money should be considered as expense in Dashboard.
7. The user can disable all accounts or merge them with another account.
8. When accounts are merged, both account amounts must be maintained and added together. 
9. n case of merging accounts, a backup file is created ,and the user is informed with a 
    message that appears on the screen.    
10. The balance of the disabled accounts should still be shown in the main balance.
11. If desired, all accounts can be kept separate from the main balance.


# Actual Output :
1. No problem was observed in account creation, naming, initial balance notification and emblem selection.
2. All accounts can be deleted. In case of account deletion, the balance of the deleted account reduces the total 
   balance amount.
3. Transfer between accounts is possible and this is compatible with the total balance calculation.
4. Transfer for the same account is not logical and possible. When this operation is desired to be done,
   the user is warned. 
5. There is no increase in the total balance in the transfer between accounts. If an amount greater than its balance is
   transferred from an account, this account balance is shown in parentheses.
6. Deleted account information is also displayed on the dashboard and pay chart.
7. A disabled account is not among the transferable accounts. Disabled accounts can be enabled.
8. When two accounts were merged, it was seen that the balance of the merged account was not transferred to the other. 
    In this case, the total balance is calculated incorrectly.(BUG)  
9. When the accounts are merged, a backup file is created ,and a user notification message is seen. 
    Thanks to the created backup file, the account merging state is restored.    
10. It was seen that if the accounts were disabled, they were still in the balance.
11. Any account can be excluded from the main balance and still transfers can be made to this account.

# Observations :


#Debriefing Information

#Defects / Bugs
Once the merge is complete, the merged account will no longer appear, but the account amount should be transferred to 
the other account, preserving the total balance and previous user experience

#Conclusion / Notes



--------------------------
# Exploratory test charters Nr:3 Analyze the Settings
## QA Engineer : Ismail Koembe
## Timebox : 30 minutes
## Purpose, actors, setup, mission, tactic
Actor : Normal user (Community Version)
Purpose : To evaluate if the Settings function
Setup: A most preferred iOS device, software version higher than 12.1.5, screen size 6,46 inches
Priority : High. The customization options are in high demand in terms of user perspective and domain competition.

# Explore
To evaluate if the Settings function works correctly

# Resources
In order to sniff the communication between client and server use Charles and configure proxy.
Other visual part will be tested manually by QA Engineer.

## To discover information

# Expected Output :
1. As a Balance Mode, user should be able to use Budget mode. In Budget mode, user should be able to set monthly 
   budget amount.
2. When the Budget mode is disabled, the total income should be shown on the dashboard again. 
   In this case, the main balance calculation must be changed.
3. As a Balance Mode, user should be able to use Carry over mode.
4. Community version should allow user to use Future Recurring Records mode.  
5. All three balance modes must be applicable both separately and together. 
6. Only paid version allows users to use Dark theme.
7. Regardless app version, user should be able to change app language and change will be applied after re-start. 
8. Regardless app version, user should be able to change currency.
9. Currency and its emblem should match.
10. User should be able to set start "First Day of Week and Month".
11. User should be able to interact Passcode.
12. User data must be exportable.
13. All synchronization ability should be applicable.
14. Data backup functionality.

# Actual Output :
1. When the budget mode is enabled, the user is prompted to enter the amount that can be spent monthly. 
   This amount is applied in accordance with the calendar option.
2. Total income shown in dashboard and balance calculation updated.
3. When the Carry over mode is selected, the balance transferred to the previous month is also displayed
   on the dashboard. The carried over amount is included in the total balance calculation.
4. Even though it's only allowed in the paid version, it's a bit confusing that normal users are also allowed to choose
   this option. Although a tooltip explains it in the first use, it is possible to forget and think that the function does not work.
5. The mentioned function is available but #4 should be taken in to account.
6. Upon dark theme intention, the user is encouraged to have paid version.
7. No issue observed regarding changing app language.
8. There is no need to recalculate the balance after the exchange rate change, but all income and expenses are thus 
   shown at the new exchange rate.
9. For randomly chosen two language, it observed that currency and emblems do not match.
10. When the first day of the month or week is changed, the app shows the dashboard instead of the settings page. 
    It should be verified via UI/UX references or PO.
11. Paid version allows user to user Passcode protection.
12. User data is exportable as csv file and file can be stored or shared via mobile phone.
13. Only paid version provides user to use Google Drive and Dropbox synchronization.
14. Creation, restoring and erasing data backup perfectly works. The backup files sorted in chronological order.

# Observations :
Only English version is available for "Future recurring records" phrase. Regardles paid or free version it seem that
app has some missing translation.

#Debriefing Information

#Defects / Bugs
BUG 1. Dashboard should represent correct currency emblem relevant currency itself. It is a BUG ,and
it has High Severity, should be solved Address Immediately. (i.e. Turkish lira, app use UK Pound emblem and Afghanistan
currency represented by Albania currency)
#Conclusion / Notes


------------------------

# Exploratory test charters Nr:4 Analyze the Categories
## QA Engineer : Ismail Koembe
## Timebox : 15 minutes
## Purpose, actors, setup, mission, tactic
Actor : Normal user (Community Version)
Purpose : To evaluate if the app Categories and Account works as expected.
Setup: A most preferred iOS device, software version higher than 12.1.5, screen size 6,46 inches
Priority : Medium. 

# Explore
To evaluate if the Category functions work correctly

# Resources
In order to sniff the communication between client and server use Charles and configure proxy.
Other visual part will be tested manually by QA Engineer.

## To discover information

# Expected Output :
1. User should be able to see all expense and income options.
2. User should be able to change the name of expenses and incomes option.
3. User should be able to delete both expense and income category.   
4. Only paid version allows user to add new expense and income category.
5. Only paid version allows user to change the icon of existing expense or income category.
6. User should be able to disable both expense and income category
7. The merged category emblem should not appear in the dashboard and category section.
8. Expenditures for the combined categories are now represented together on the dashboard.
9. After the merge process, the user is given the opportunity to undo the merge operation by tapping the message on 
   the screen or by using the created backup file.
10. The user should be able to disable one of the expense and income categories. Disabled categories appear in 
    a different color in the category section and are not displayed in dashboard.   
11. User should be able to enable any disabled income or expense category. In this case, these categories are displayed 
    in dashboard again.
12. If a category for which an expense has been previously reported is disabled, it should still be shown in the pay 
    chart on the dashboard.    


# Actual Output :
1. All default expense and income options are shown.
2. User can change the name of expenses and incomes option.
3. User can delete both expense and income category.
4. Community user can not add new expense and income category.
5. Community user can not change the icon of existing expense or income category.
6. User can disable both expense and income category.
7. The merged category emblem does not appear in the dashboard and category section.
8. Expenditures for the combined categories are now represented together on the dashboard.
9. User can undo the merge operation by tapping the message on the screen or by using the created backup file.
10. The user can disable one of the expense and income categories. Disabled categories appear in a different color
    in the category section and are not displayed in dashboard.
11. User can enable any disabled income or expense category. In this case, these categories are displayed
    in dashboard again.
12. If a category for which an expense has been previously reported is disabled, it should still be shown in the pay
    chart on the dashboard.
    
# Observations :
No issue observed. In order to approve whole feature, the paid version also should be tested. 

#Debriefing Information

#Defects / Bugs
-

#Conclusion / Notes


------------------------

# Exploratory test charters Nr:5 Analyze the Categories Calendar Function
## QA Engineer : Ismail Koembe
## Timebox : 15 minutes
## Purpose, actors, setup, mission, tactic
Actor : Normal user (Community Version)
Purpose : To evaluate if the app Categories and Account works as expected.
Setup: A most preferred iOS device, software version higher than 12.1.5, screen size 6,46 inches
Priority : High.

# Explore
To evaluate if the Calendar functions work correctly

# Resources
In order to sniff the communication between client and server use Charles and configure proxy.
Other visual part will be tested manually by QA Engineer.

## To discover information

# Expected Output :
1. When the app is first installed, the monthly date selection should be applied by default.
2. It is possible to switch daily, weekly, monthly, and yearly period.
3. User should be able to set date interval via calendar.
4. User should be able to see specific date via calendar.
5. Once user sets initial balance date of account(s), user should swipe to past dates.  

# Actual Output :
1. The monthly period comes as default, and the current month is displayed correctly. Since the app newly installed, 
   swiping to next and previous months is not available.
2. Upon switching daily period, the correct day appeared in dashboard. The weekly period is shown regarding first day of
   the week.  
3. When the date interval selection is applied, the data of this period and the calculation are displayed on the board. 
   Daily, weekly, monthly, and yearly date filters are applied in accordance with this range.
4. Choose Date option provides user to specify the day and presents daily information.  
   Daily, weekly, monthly, and yearly date filters are applied in accordance with particular date.  
5. Default date period is monthly and as long as user does not set initial balance date, left and right swiping is not
    applicable.

# Observations :

#Debriefing Information

#Defects / Bugs
BUG 2. Upon change of the first day of the week, the weekly period does not recalculate and the old preference
shown in the dashboard. It can be caused by architectural deficiency and need to consult with the Technical Architecture
team or developers.

#Conclusion / Notes
The configuration changes could be converted into a queue message and consumed by other services. It makes the app more
responsive.
I think it will be more useful for the user to always show the current date when the date range is selected, or a 
special day is selected. Otherwise, the user will have to select the current day again each time. 
However, I think the Today button could be very useful.

---------------------------------

# Exploratory test charters Nr:6 Analyze the All available options for Pro version
## QA Engineer : Ismail Koembe
## Timebox : 45 minutes
## Purpose, actors, setup, mission, tactic
Actor : Normal user (Community Version)
Purpose : To evaluate if the app works as expected when switch pro version.
Setup: A most preferred iOS device, software version higher than 12.1.5, screen size 6,46 inches
Priority : High.

# Explore
To evaluate if the Pro version functions works correctly

# Resources
In order to sniff the communication between client and server use Charles and configure proxy.
Other visual part will be tested manually by QA Engineer.

## To discover information

# Expected Output :
1. User should be able to buy Pro version for all available payment options such as PayPal
2. User should be able to set passcode protection.
3. Passcode protection support 4 digit pin and iOS Touch Id / Face Id methods.
4. Both pin and Touch / Face Id options are applicable at same time.   
4. Passcode requirement should be set accordingly given time period.
5. User should be able to add new expense and specify new icon and name.
6. User should be able to add new income and specify new icon and name.
7. User should access Currencies tab and sets main currency.
8. User should be able to set amount of decimal places for main currency.
9. User should be able to set amount of decimal places for all other currencies.
10. User should be able to se exchange rate from all currencies to main currency.
11. Exchange rate should be editable.
12. New exchange rate should be submitted and recorded.
13. Dark Theme should be applicable. 
14. Dark theme should not worsen user experience and visibility of mobile element/component.
15. User should synch with given Google Drive account.
16. User should synch with given Dropbox account.
17. Synched names of Google Driver and DropBox account should be visible.
18. User should be able to cancel synch with Google Drive and Dropbox.
19. At the same time only one option should be used for synchronization.

# Actual Output :
1. Pro version bought for all available payment options such as PayPal
2. User can set passcode protection.
3. Passcode protection support 4 digit pin and iOS Touch Id / Face Id methods.
4. Both pin and Touch / Face Id options are applicable at same time.
4. Passcode and Face Id protection work for given time period.
5. New expense can be added with new icon and name. As long as a expense submitted, new expense appears in dashboard.
6. New income can be added with new icon and name. As long as a income submitted, it will be taken into account.
7. User can access Currencies tab and sets main currency.
8. User can set amount of decimal places for main currency.
9. User can set amount of decimal places for all other currencies.
10. User can see exchange rate from all currencies to main currency.
11. Exchange rate can be editable.
12. New exchange rate can be submitted and recorded.
13. Dark Theme can be applicable.
14. Dark theme does not worsen user experience and visibility of mobile element/component.
15. User can synch with given Google Drive account.
16. User can synch with given Dropbox account.
17. Synched names of Google Driver and DropBox account should be visible.
18. User can cancel synch with Google Drive and Dropbox.
19. At the same time only one option can be used for synchronization.

# Observations :
No issue observed
#Debriefing Information

#Defects / Bugs
-
#Conclusion / Notes
 The pro version can be acquired easily and part of user experience. It is quite smooth transition and all promised
options are available for user.

-----------------------

# Findings from Charters
# Prioritization 
1. Dashboard and calculations    -Very High Priority   - 30 minutes    
2. Account                       -Very High Priority   - 45 minutes
3. Settings                      -High Priority         - 30 minutes
4. Calendar                      -Medium                - 15 minutes
5. Categories                    -Medium                - 15 minutes 

# General Explanation and prioritization reasons

Considering that the main purpose of the application is financial regulatory and financial monitoring, the Dashboard 
area, where the user will first contact and start using the application, should be tested first. The most important item
on the dashboard will be the share chart diagram and its components, which users use to monitor their financial status.
It should be noted that the use of the application can of course start when the user specifies an income. Later, 
the question of whether the current expense items will be suitable for him will come to the agenda.

Although all these possibilities and new configuration needs will of course lead the user to the paid version, it is 
also a known fact that many users decide whether to buy or not after reaching sufficient experience.

Many users with fixed income care more about when they earn income than when they download the app. At this point, 
it becomes important how user-friendly the application calendar is.

Considering the financial regulator role of the application and the positive comments it received from real users, 
it becomes clear that the budget mode should definitely not be ignored.

Of course, for domain competition, how much customization freedom is given to users is an important measure of value. 
Since financial information is within the scope of personal data security, application security or integrated use with 
existing security options is also a test subject.

# Risk and mitigate plan 

In order to perfectly understand risk and prepare mitigation plan, I tried to figure out risk areas and their triggers.
Then I classified the risks and prioritize them. To my understanding, Monefy app could face "User and functional 
requirements" based risk and issues. I believe that the app should capture all user need with respect to features, 
functions, and quality of service. I think that since the application is in a constantly competitive field, it needs 
constant feature delivery and innovation. The risk of creating a regression with each new change cannot be excluded. 
For this reason, I think that a regression suite, which has a very strong coverage, is very important.

A possible data loss or synchronization error will be the biggest problem.
Since the functions of accurately transferring income and expenses to users, tracking fixed budget, and expense are the 
most important parts of this application, these sections should be taken in the sanity suite.
Since the application offers customization possibilities to the user, user configurations should be tested to cover 
all edge cases.





