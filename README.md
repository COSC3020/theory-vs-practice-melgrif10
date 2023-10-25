[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=12505784&assignment_repo_type=AssignmentRepo)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.

1. Asymptotic analysis can be misleading when it comes to actual performance because it doesn't account for memory allocation. It treats this as a constant when in reality it can vary becuase its based off of things like available memory and memory management. It also doesn't consider constants or constant factors. It only considers when n gets big or the input size changes which could misrepresent algorithms when given small input sizes. Finally, asymptotic analysis doesn't consider real world implications like security or time constraints which may influence the type of algorithm that should be used. 

2.The average case for the performance of a binary search tree is O(log n). If it take 5 seconds to find an element when the tree has 1,000 elements this information can be applied to the average case 5s = O(log_2(1,000)). To  find how long it would take to find the same element with a tree containing 10,000 elements take x = O(log_2(10,000)). Now that we have the mathematical description of the information given in the question a proportion can be set up:
5s/(log_2(1,000)) = x/(log_2(10,000)) 
Then just solve for x: 
x*(log_2(1,000)) = 5*(log_2(10,000)) 
x = 5*(log_2(10,000))/(log_2(1,000))
x = 66.44/9.966
x = 6.666 seconds 

3.The actual time for finding the element in a binary search tree with 10,000 elements was 100 seconds. The reason this could be so different from the theoretical time is because the binary search tree could be unbalanced which would bring about the worst case where the performance would be O(n). Another reason why it could take so much longer is whether the tree is sorted or not. If it is you could end up searching the entire tree in order to find the one element your looking for. Finally, how the memory is being allocated and distributed can make the runtime longer than anticipated. 