========== Question ==========  

### What are tasks in event loop  

========== Answer ==========  

A task is any javascript code/program which is scheduled to be run by the standard mechanisms such as initially starting to run a program, run an event callback, or an interval or timeout being fired. All these tasks are scheduled on a task queue.

Below are the list of use cases to add tasks to the task queue,

1. When a new javascript program is executed directly from console or running by the `<script>` element, the task will be added to the task queue.

2. When an event fires, the event callback added to task queue

3. When a setTimeout or setInterval is reached, the corresponding callback added to task queue

========== Id ==========  
387

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#387-What-are-tasks-in-event-loop

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
