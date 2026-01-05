class Solution {
    public int[] twoSum(int[] nums, int target) {

        // HashMap to store number and its index
        HashMap<Integer, Integer> map = new HashMap<>();

        for (int i = 0; i < nums.length; i++) {

            int needed = target - nums[i];

            // check if required number already exists
            if (map.containsKey(needed)) {
                return new int[] { map.get(needed), i };
            }

            // store current number with index
            map.put(nums[i], i);
        }

        return new int[] {};
    }
}

