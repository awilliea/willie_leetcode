使用兩個指標，一個全run一遍，一個在遇到不同的才前進就行。
有個要注意的地方是vector.size()的性質，在vector是空字串的時候與int做比較時會出錯，所以最前端可先對vector.empty()做檢查。


```c++
class Solution {
public:
    int removeDuplicates(vector<int>& nums) {
        int j=0;
        if (nums.empty()){
            return 0;
        }
        for(int i=0;i<nums.size();i++){
            if(nums[i]!=nums[j]){
                j++;
                nums[j]=nums[i];
            }
        }
        return j+1;
    }
};
```                                        
                                       
                                       
