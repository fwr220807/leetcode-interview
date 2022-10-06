### 题目链接

「[剑指 Offer 03. 数组中重复的数字](https://leetcode.cn/problems/shu-zu-zhong-zhong-fu-de-shu-zi-lcof/)」

### 解题思路

1. 利用哈希 Set 存储出现过的数字，出现重复数字后就返回结果；
2. 时间复杂度 O(n) = n。

### 代码

```js
/**
 * @param {number[]} nums
 * @return {number}
 */
var findRepeatNumber = function(nums) {
    const numsTemp = new Set()

    while(nums.length !== 0) {
        let num = nums.pop()

        if (numsTemp.has(num)) {
            return num
        } else {
            numsTemp.add(num)
        }
    }
};
```

