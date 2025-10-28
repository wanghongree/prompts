This project deploy a shiny dashboard in docker. @dockerfiles/dockerfile and relavent files eg: @shiny_sitrep/functions/data_functions.R, shiny_sitrep/data_preparation.R, think hard and explain to me concisely how does the code update data from database?


Correct! Here are some background information. My source database update every day in the morning and almost always don't change until the next day. Their update start from 05:30 and takes about 3 hours.

Now I found there is a issuse with the first update. This cause my data stored in history_vetting_status_path wrong. Looks to me it's due to incompleted data when update. Therefore, I hope to add logs for me to diagnose the problem. Here are some requirements for the log as far as I can think of:
- The log should be stored in a folder called logs.
- Each day's log is stored in a file with date time in name.
- We only keep last 2 month's log, that is the log before two month ago is deleted every day.
- Each log record should contains date time
- For now, the log focus on the deployment and daily data update part, such as shiny_sitrep/data_preparation.R and some functions in @shiny_sitrep/functions/data_functions.R. check_if_pull_data functions is an important one for me to understand what happens. 

Please think hard and suggest a plan for this. You can raise what you think useful and veto my inapproprated suggestions.
