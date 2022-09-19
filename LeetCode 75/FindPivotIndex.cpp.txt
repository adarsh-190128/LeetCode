class Solution {
public:
    int pivotIndex(vector<int>& nums) {
        
        //Let Us assume us that leftsum and rightsum is intially zero
        
        int ls=0,rs=0,n=nums.size();
        
        //lets assume that rightsum is equal to total sum 
        //Because while repating the loop. we can delete left sum from rightsum that is total sum  
        //so
        //Right sum = Total Sum 
        // Initializee a loop to iterate every element assuming as pivot element 
        // check every element left sum == right sum 
        // in loop totalsum-nums[i] is done to remove the pivot element from sum
        // if if condition excuute's it returns the index else -1 
        
        for(int i=0;i<nums.size();i++){
            rs+=nums[i];
    }
        for(int i=0;i<n;i++){
            rs-=nums[i];
           if(ls==rs){
                return i;
                break;
              }
           ls+=nums[i];
          }
         return -1;
        
    }
};


// If any Doubt's let us discuss

// Gd luck