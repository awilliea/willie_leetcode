 舉例完後，數字加一的現象必須要從vector尾端開始檢查是否為9
 
 有個特點是當全digits都是9時，整個vector長度會變長，可使用insert或是第一個改1，再使用push_back

```c++
class Solution {
public:
    vector<int> plusOne(vector<int>& digits) {
        for(int i=digits.size()-1;i>=0;i--){
            if(digits[i]==9){
               digits[i]=0;
            }
            else{
                digits[i]++;
                return digits;
            }
        }
        #digits.insert(digits.begin(),1,1);
        digits[0]=1;
        digits.push_back(0);
        return digits;
    }
};
```
