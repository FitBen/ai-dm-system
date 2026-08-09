# Testing and Iteration

The workflow was developed iteratively.

## Test cases

- expected response
- one-word response
- user supplies multiple answers at once
- user asks a question instead
- user changes topic
- user wants the resource immediately
- user is highly qualified
- user is not ready
- unexpected scenario state
- repeated or delayed reply
- booking event changes lead state
- human intervention is required

## Evaluation

1. Did the correct ManyChat scenario start?
2. Did the conversation make sense for the entry point?
3. Was existing information respected?
4. Was the next question necessary?
5. Were fields/tags updated correctly?
6. Did Make receive the expected payload?
7. Was Google Sheets updated correctly?
8. Did the next-step logic make sense?
9. Did the flow recover gracefully from an unexpected reply?

The purpose of testing is not only to find technical errors. Awkward conversations are product-design failures too.
