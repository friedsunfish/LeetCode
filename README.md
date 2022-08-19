Test....

Two Sum (leet code)

Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target. You may assume that each input would have exactly one solution, and you may not use the same element twice. You can return the answer in any order.

```javascript
var twoSum = function (nums, target) {
    for (let i = 0; i < nums.length; i++) {
        if (
            nums.indexOf(target - nums[i]) != -1 &&
            nums.indexOf(target - nums[i]) != i
        ) {
            return[i, nums.indexOf(target - nums[i])];
        }
    }
};
```

배열에서 2개의합이 목표와 같아지는 경우찾기 (경우수1개)
```jacascript
function solution(money, cost){
  let result = [];

  for(let i=0; i<cost.length; i++){
    let spend = money - cost[i]
    
    for(let j=0; j<cost.length; j++){
      if(j == i) continue
      if(spend == cost[j]){
        result.push(cost[i])
      }
    }
  }
  return (result)
}
console.log(solution(14,[1,2,6,7,8]))
```
