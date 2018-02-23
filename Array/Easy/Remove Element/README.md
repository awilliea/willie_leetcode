這題跟上一題的做法其實差不多，也是用兩個座標去跑就可以。

```c++
class Solution {
public:
    int removeElement(vector<int>& nums, int val) {
        if(nums.empty()){
            return 0;
        }
        int j=-1;
        for(int i=0;i<nums.size();i++){
            if (nums[i]!=val){
                j++;
                nums[j]=nums[i];
            }
        }
        return j+1;
        
    }
};
```
