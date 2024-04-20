# t5_text_2_sql
pretraining t5 model for text 2 sql task using huggingface.

the input format is as follows.

code sql query: schema: ...(enter schema) question: ...(enter question)


### example:

code sql query:

schema: | department : department_id , name , creation , ranking , budget_in_billions , num_employees | head : head_id , name , born_state , age | management : department_id , head_id , temporary_acting | management.head_id = head.head_id | management.department_id = department.department_id |

question: How many heads of the departments are older than 56 ?

**without new lines.**
