這題我是先使用排序，之後再與原vector做比較，找出不同的element有幾個

但以Easy題來說程式碼有點太長，應該還有滿大的改進空間。

```c++
class Solution {
public:
    void quicksort(vector<int>& nums,int left,int right){
        if(left<right){
            int pivot=nums[right];
            int i=left-1,j=left;
            int temp;
            while(j<right+1){
                if(nums[j]<=pivot and i<j){
                    i=i+1;
                    temp=nums[i];
                    nums[i]=nums[j];
                    nums[j]=temp;
                }
               j++;
            }
            quicksort(nums,left,i-1);
            quicksort(nums,i+1,right);
        }
    }
    int findUnsortedSubarray(vector<int>& nums) {
        int first=0,last=0,flag=0;
        vector<int> v1=nums;
        quicksort(nums,0,nums.size()-1);
        for(int i=0;i<nums.size();i++){
            if(v1[i]!=nums[i] and flag==0){
                first=i;
                flag=1;
            }
            else if(v1[i]!=nums[i] and flag==1){
                last=i;
            }
        }
        if (last==first)
            return last;
        else
            return (last-first+1);
    }  
};
```
