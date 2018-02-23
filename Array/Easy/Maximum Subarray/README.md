DP解法 用一維array紀錄，同時更新answer

```c++
class Solution {
public:
    int maxSubArray(vector<int>& nums) {
        int max=0,answer=nums[0];
        for(int i=0;i<nums.size();i++){
            if(max+nums[i]<nums[i]){
                max=nums[i];
            }
            else{
                max+=nums[i];
            }
            if (answer<max){
                answer=max;
            }
        }
        return answer;
    }
};
```
Divide and Conquer
目前只想到O(nlogn)解法，merge方面是從中間往兩旁擴展，不過應該有更好的merge方法。
