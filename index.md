# Lab report 2: 
---
**Part 1:**

 using `/add-message` screenshots: 
 
 ![Image](hello.jpg)
 
 ![Image](howareyou.jpg)
 
 In the first screenshot, the method handlerequest is called with /add-message?s= as the argument, which then adds the word after the = sign, which is Hello. In the second screenshot, handlerequest is called twice as the first time was with hello and the second time was with how are you. When I added the second message, it was saved into the "a" arraylist and then added to "rs", and then broke them into two lines due to "\n". Values of any relevant fields of the class change into a string value, as the method returns any inputted values back as a string and prints them out on the page. 
 
**Part 2:**

The reversed() method in lab 3 was buggy and did not work in its intended way. 

Failure inducing input: 

`@Test 
   public void testReversed2() {
        int[] arr = {1,2,3,4,5};
        int[] reversed = ArrayExamples.reversed(arr);
        aasertArrayEquals(new int[] {5,4,3,2,1}, reversed);
    }`

Working input:

` @Test
    public void testReversed(){
        int[] input = { };
        assertEquals(new int[]{ }, ArrayExamples.reversed(input1));
    }`

Output of tests: 

![Image](outputs.jpg)

The working input only worked because the input was empty, meaning that the reversed method would pass since there was nothing to reverse. Conversely, the failure inducing input failed because the method was simply copying the numbers into the inputted int list. 

**The Fix**

Reversed() before: 

` static int[] reversed(int[] arr){

        int[] newArray = new int[arr.length];
        for(int i =0; i<arr.length; i+=1){
            arr[i] = newArray[arr.length-i-1];
        }
        return arr; 
    }`

Reversed() after:

`static int[] reversed(int[] arr){

        int[] newArray = new int[arr.length];
        for(int i =0; i<arr.length; i+=1){
            newArray[i] = arr[arr.length-i-1];
        }
        return newArray; 
    }`

By switching arr and newArray, the fixed method creates a new empty list and copies the elements in the argument in reverse order.

**Part 3:**

In lab two I learned that github desktop tracks and records changes then pushes them out to Github. Previously I thought of it as a more convienient IDE, one that would let me code and push to github in the same app, but now I know it solely serves the purpose of tracking, recording, then pushing. 



