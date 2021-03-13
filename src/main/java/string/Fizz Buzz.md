##412. Fizz Buzz
写一个程序，输出从 1 到 n 数字的字符串表示。

1. 如果 n 是3的倍数，输出“Fizz”；

2. 如果 n 是5的倍数，输出“Buzz”；

3.如果 n 同时是3和5的倍数，输出 “FizzBuzz”。
###示例
    n = 15,
    
    返回:
    [
        "1",
        "2",
        "Fizz",
        "4",
        "Buzz",
        "Fizz",
        "7",
        "8",
        "Fizz",
        "Buzz",
        "11",
        "Fizz",
        "13",
        "14",
        "FizzBuzz"
    ]
    
###思路

###code
    class Solution {
        public List<String> fizzBuzz(int n) {
            List<String> ans = new ArrayList<String>();
            for(int i = 1;i<= n;i++){
                boolean divided3 = (i % 3 == 0);
                boolean divided5 = (i % 5 == 0);
                if(divided3 && divided5){
                    ans.add("FizzBuzz");
                }
                else if(divided3){
                    ans.add("Fizz");
                }
                else if(divided5){
                    ans.add("Buzz");
                }
                else{
                    ans.add(Integer.toString(i));
                }
            }
            return ans;
        }
    }