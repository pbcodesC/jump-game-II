# jump-game-II

class Solution {
public:
    int jump(vector<int>& nums) {
        int n = nums.size();
        int maxindx = 0;
        int jump = 0;
        int current_end = 0;
        for(int i = 0; i <n-1; i++){
            maxindx = max(maxindx,(i+nums[i]));
            if (i== current_end){
                jump ++;
                current_end= maxindx;
             }
                
         }
        return jump;
     }

};
