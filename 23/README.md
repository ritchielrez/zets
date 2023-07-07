# How to remove brackets from strings

Suppose there is a string, `(8%)`, returned from a grep output. I want to filter the string out of the parantheses. I can use the `tr` command to remove it. 
To do so, I need to pipe the string to this command, `tr -d "()"`.`-d` flag deletes those paranthese characters.
