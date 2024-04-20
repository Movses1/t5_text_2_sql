# t5_text_2_sql
pretraining t5 model for text 2 sql task using huggingface API.

__The ideal evaluation method__ for text to sql would be to run the queries to see how many of them run at all + syntactic correctness, how many give the exact table that we wanted and compare the execution time and memory complexities with the original query. However for simplicity i'll just go with SacreBLEU.

### the input format is as follows.

code sql query: schema: ...(enter schema) question: ...(enter question)


### example:

code sql query:

schema: | department : department_id , name , creation , ranking , budget_in_billions , num_employees | head : head_id , name , born_state , age | management : department_id , head_id , temporary_acting | management.head_id = head.head_id | management.department_id = department.department_id |

question: How many heads of the departments are older than 56 ?

**all in the same line.**

### link to the model

https://huggingface.co/Movg/t5-small-finetuned-sql/tree/main
