1. I want to add tasks to my todo list.
2. I want to see all the tasks in my todo list.
3. I want to change the status of a task between incomplete and complete.
4. I want to be able to get only the complete tasks.
5. I want to be able to get only the incomplete tasks.
6. I want to search for a task and receive a message that says it wasn't found if it doesn't exist.
7. I want to remove tasks from my list.
8. I want to see all the tasks in my list ordered alphabetically in ascending order.
9. I want to see all the tasks in my list ordered alphabetically in descending order.



| Methods                           | Variables                                      | Scenario                                    | Results                                           |
|-----------------------------------|------------------------------------------------|---------------------------------------------|---------------------------------------------------|
| `addTask(String task)`            | `Hashmap<String task, String status> toDoList` | 1.                                          |                                                   |
|                                   | (task is key, status is value)                 | Add a new tasks to the list                 | Output success message                            |
|                                   |                                                |                                             | Update toDoList                                   |
|                                   |                                                |                                             | Return true                                       |
|                                   |                                                | 6.                                          |                                                   |
|                                   |                                                | Fail to add an existing task                | Output failure message                            |
|                                   |                                                |                                             | Don't update the toDoList                         |
|                                   |                                                |                                             | Return false                                      |
| `showToDoList()`                  |                                                | 2.                                          |                                                   |
|                                   |                                                | If the toDoList is empty                    | Output empty message                              |
|                                   |                                                |                                             | Return false                                      |
|                                   |                                                | 2.                                          |                                                   |
|                                   |                                                | If the toDoList is not empty                | Print all the tasks from the toDoList             |
|                                   |                                                |                                             | Return a list of Strings                          |
| `changeStatus(String newStatus)`  |                                                | 3.                                          |                                                   |
|                                   |                                                | Change status of an existing task           | Output success message                            |
|                                   |                                                | newStatus is different from the old         | Update toDoList                                   |
|                                   |                                                |                                             | Return true                                       |
|                                   |                                                | 3.                                          |                                                   |
|                                   |                                                | Fail updating status of non-existing task   | Output failure message                            |
|                                   |                                                | newStatus is the same as the old            | Don't update the toDoList                         |
|                                   |                                                |                                             | Return false                                      |
| `getCategoryTasks(String status)` |                                                | 4.                                          |                                                   |
|                                   |                                                | If the status is equal to complete and      | Output completed message                          |
|                                   |                                                | if there are completed tasks in the list    | Print all the completed tasks from the toDoList   |
|                                   |                                                |                                             | Return a list of Strings                          |
|                                   |                                                | 4.                                          |                                                   |
|                                   |                                                | If the status is equal to complete and      | Output non-completed message                      |
|                                   |                                                | if there aren't completed tasks in the list | Don't print anything from list                    |
|                                   |                                                |                                             | Return empty list                                 |
|                                   |                                                | 5.                                          |                                                   |
|                                   |                                                | If the status is equal to incomplete and    | Output incompleted message                        |
|                                   |                                                | if there are incompleted tasks in the list  | Print all the incompleted tasks from the toDoList |
|                                   |                                                |                                             | Return a list of Strings                          |
|                                   |                                                | 5.                                          |                                                   |
|                                   |                                                | If the status is equal to incomplete and    | Output completed message                          |
|                                   |                                                | if there are incompleted tasks in the list  | Don't print anything from list                    |
|                                   |                                                |                                             | Return empty list                                 |
| `removeTask(String task)`         |                                                | 7.                                          |                                                   |
|                                   |                                                | Remove existing task from list              | Output success message                            |
|                                   |                                                |                                             | Update toDoList                                   |
|                                   |                                                |                                             | Return true                                       |
|                                   |                                                | 7.                                          |                                                   |
|                                   |                                                | Remove non-existing task from list          | Output failure message                            |
|                                   |                                                |                                             | Don't update the toDoList                         |
|                                   |                                                |                                             | Return false                                      |
| `orderedTasks(String orderType)`  |                                                | 8.                                          |                                                   |
|                                   |                                                | If orderType is equal to ascending          | Print all the tasks with ascending order          |
|                                   |                                                |                                             | Return a list of Strings                          |
|                                   |                                                | 9.                                          |                                                   |
|                                   |                                                | If orderType is equal to descending         | Print all the tasks with ascending order          |
|                                   |                                                |                                             | Return a list of Strings                          |