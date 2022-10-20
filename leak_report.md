# Leak report

The leak appeared in check_whitespace because it allocated memory to store all the non-whitespace characters +1 more for the null terminator. But it didn't free the callocated space stored. 
