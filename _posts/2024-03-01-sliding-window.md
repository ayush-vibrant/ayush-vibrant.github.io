# How to solve Sliding window questions?
The concept of the sliding window accounts for almost 30% of interview questions.

**Identification:**
- Problems involving arrays or strings.
- Questions about subarrays or substrings.
- Often involves finding the largest, smallest, or greatest elements, etc.
- Involvement of a certain number \(k\) (representing window size). Sometimes, this might not be explicitly given, requiring you to determine the optimal window size based on the problem statement.

**Types of Windows:**

- **Fixed Size Window:** The value of \(k\) is provided.
  - #### Code pattern for fixed size sliding window
      ```
      int n = arr.length; // Length of the array
      int i = 0; // Start of the window
      int j = 0; // End of the window
    
      while(j < n) {
          // Work on j (e.g., perform calculations for the sliding window)
    
          if(j - i + 1 < k) {
              // Window size is less than k, move j forward to expand the window
              j++;
          } else if (j - i + 1 == k) {
              // Window size is exactly k
              // Update answer 'a' based on current window calculations
            
              // Move the window forward by incrementing both i and j
              // Note: Handle the removal of the i-th element's effect, as the condition
              // for j has already been addressed at the start of the loop
              i++;
              j++;
          }
      }
      return answer; // Return the final answer
      ```
- **Dynamic Size Window:** \(k\) might not be given but asked. In this case, you’d assume/calculate for different size windows and see if this particular size window matches the conditions. 
    > Hint: Questions would be like largest window having positive sum, smallest window. While solving such questions you might have to use an additional list / map / array.
    
  - #### Code pattern for dynamic size sliding window
      ```
      int n = arr.length; // Length of the array
      int i = 0; // Start of the window
      int j = 0; // End of the window
    
      while(j < n) {
          // Perform calculations
    
          if (condition < k) {
              // If the condition is not met, expand the window by moving 'j' forward
              j++;
          } else if (condition == k) {
              // If the condition is met exactly, update the answer
              ans = condition;
              // Then, try to find another potential solution by moving 'j' forward
              j++;
          } else if (condition > k) {
              // If the condition exceeds 'k', shrink the window from the start by moving 'i' forward,
              // and adjust calculations accordingly
              while(condition > k) {
                  // Adjust calculation for the removal of the 'i'th element's effect
                  i++;
              }
              // After adjusting, move 'j' forward to continue exploring other windows
              j++;
          }
     }

    return ans; // Return the final answer
    ```
In fixed-size problems, we are given the size of the window, and we might be asked to solve problems such as returning the maximum sum obtainable from a window of size (k). Conversely, in variable size sliding window problems, the task might involve finding the largest length of the window that can yield a given sum