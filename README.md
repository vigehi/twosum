# twosum
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.  
You may assume that each input would have exactly one solution, and you may not use the same element twice. 
You can return the answer in any order.   
class Solution {
    public int[] twoSum(int[] nums, int target) {
        Map<Integer, Integer> num_map = new HashMap<>();
        for(int i=0; i<nums.length; i++){
            int compliment = target - nums[i];
            if(num_map.containsKey(compliment)){
                return new int[]{
                    num_map.get(compliment), i
                };
            }
            num_map.put(nums[i], i);
        }
        throw new IllegalArgumentException("not fount");
    }
}
