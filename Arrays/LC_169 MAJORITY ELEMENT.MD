LC_169_Majority_elements
https://leetcode.com/problems/majority-element/submissions/1754331905/

APPROACH
Initiate a for loop and if we find the same element count++ else negate it , and if count goes 0 then replace the element with that element having 0 frequency

CODE
public int majorityElement(int[] nums) {
    int e = nums[0];
    int count =0;
    for(int c : nums){
        if (count == 0) {
            e = c;
            count = 1;
        } else if (c == e) {
            count++;
        } else {
            count--;
        }
    }
    return e;
}
