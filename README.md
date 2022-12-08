# todos_app
//Overview 

/*1. when user enters the task on the input box and clicks add, a task card should be added
on the bottom of add button.

2. The task card contains a checkbox, task name and a delete button.

3. When checkbox is checked, the task name should be striked off. When check box is unchecked, striker should be removed

4. When delete button is clicked, the task card should be delted.

5. When the page is reloaded, the items should not be changed. 



// Working procedure


1. We totally have 6 functions. They are as follows

  1.onAddTodo()
  2.createAndAppendTodo()
  3.addStriker()
  4.onDeleteTodo()
  5.getLabelId()
  6.getTodoId()



  1. onAddTodo():
         
    1.This function would be called when the user enters text on the input box 
      and presses enters.
    
    2. If the value of the input box is an empty string, this function raised an error.
    
    3. If the value of the input box is not an empty string, 
      then it creates a todoObject with properties 'text','id',isTaskCompleted and appends 
      this todoObject to an array todoList that we already defined.
      
      The value of the properties are as follows.

      I. The value of text property or key would be, the value of the input box.
     II. The value of id property or key would be the "length" of todoList+1.
    III. The value of isTaskCompleted would be 'false', since the task can't be completed while adding
   
   4. This function then calls, antother Function  createAndAppendTodo() by passing todoObject
      as a parameter, to dynamically create a todo card and clears the user input on input Box

      
  2. createAndAppendTodo()

      1.This function would be called in two times.
        one is every time, we enter text and click on add button
        two is when the whole page is reloaded.

        Note: We have declared an array for for storing todoObjects.
        when the page is reloaded, we get the todoJSON object from local Storage.
        and we iterate over it and create todo cards for all todoObjects

      2.This function dynamically creates, todoCard and appends it to the todosItemContainer


  3. addStriker():

      1. This an eventLister call back function accepts event object as a parameter. This function is attached to 
      input check box element. whenever the use clicks on the check box, this function would be called.


      2. When this function is called it either adds or removes a veritcal line on the label element, we get its target checked status (event.target.checked). 
      
      3. After getting target checked status, if checked status is true, 
      we get the label element associated with checkbox and add the striker class to it.

      4. If the checked status is false, we get the label element associated with it and 
      remove the striker class.

      5. whenever the target Checked staus is changed, we update the isTaskCompleted property with eiter true or false

  4. onDeleteTodo():

     1. This is also a eventlistenr call back function accteps event object as a perameter. 
     This function is added as an event listener function of delete icon.
     This would be called, whenever, delete icon is pressed.

     2. When delete icon is pressed, it retrives its id, by event.target.id. 
     3. After getting delete id, by using that ID, it extracts todoID. 
     4. with that todo ID, we get the element using getElementById method and removes it from the todosItemContainer

     5. Whenever, we delete that Item, we symultaniously removes the particular object form todo list.

  5. getLabelId():
      1. this function takes a string and extract letters from it. and retuns an interger corresponding to 
      extracted number.
      
  6. getToDoID():
        1. this function takes a string and extract letters from it. and retuns an interger corresponding to 
      extracted number.





*/
