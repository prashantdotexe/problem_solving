public class Solution {
    public int findMedian(int[][] A) {
        int rows=A.length;
        int cols=A[0].length;
        int required=(rows*cols+1)/2;

        int lo=1;
        int hi=1000000000;

        while(lo<hi){
            int mid=lo+(hi-lo)/2;

            int count=countLessThanNumber(mid,A);

            if(count<required){
                lo=mid+1;
            }
            else{
                hi=mid;
            }
        }

        return lo;
    }

    int countLessThanNumber(int x,int[][] A){
        int count=0;

        for(int i=0;i<A.length;i++){
            int[] nums=A[i];

            count+=countLessThanTarget(nums,x);
        }

        return count;
    }

    int countLessThanTarget(int[] nums,int target){
        int lo=0;
        int hi=nums.length;

        while(lo<hi){
            int mid=lo+(hi-lo)/2;

            if(nums[mid]<=target){
                lo=mid+1;
            }
            else{
                hi=mid;
            }
        }

        return lo;
    }
}
