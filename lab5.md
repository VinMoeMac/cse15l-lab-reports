# Lab Report 5

# Part 1

## Student Question
__What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?__

I am on my windows computer logged into ieng6 bash terminal running a bash script to test ListExamples.java



__Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.__

I am getting this when I run a bash script to grade the ListExamples:

<img width="758" alt="image" src="https://github.com/VinMoeMac/cse15l-lab-reports/assets/130107058/ab94c740-ab0a-4079-902a-385f4ae8887e">

I was expecting to have the tests to give a 4/4

__Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.__

These tests are failing because they are running too long:

```
  @Test(timeout = 500)
  public void testMergeRightEnd() {
    List<String> left = Arrays.asList("a", "c", "e");
    List<String> right = Arrays.asList("b", "h");
    List<String> merged = ListExamples.merge(left, right);
    List<String> expected = Arrays.asList("a", "b", "c", "e", "h");
    assertEquals(expected, merged);
  }

  @Test(timeout = 500)
  public void testMergeLeftEnd() {
    List<String> left = Arrays.asList("a", "c", "z");
    List<String> right = Arrays.asList("b", "d");
    List<String> merged = ListExamples.merge(left, right);
    List<String> expected = Arrays.asList("a", "b", "c", "d", "z");
    assertEquals(expected, merged);
  }
```

I believe its a problem with my merge function which looks like this:
```
static List<String> merge(List<String> list1, List<String> list2) {
    List<String> result = new ArrayList<>();
    int index1 = 0, index2 = 0;
    while(index1 < list1.size() && index2 < list2.size()) {
      if(list1.get(index1).compareTo(list2.get(index2)) < 0) {
        result.add(list1.get(index1));
        
      }
      else if (list1.get(index1).compareTo(list2.get(index2)) == 0) {
        result.add(list1.get(index1));
        
      }
      else {
        result.add(list2.get(index2));
        
      }
    }
    while(index1 < list1.size()) {
      result.add(list1.get(index1));
      
    }
    while(index2 < list2.size()) {
      result.add(list2.get(index2));
      
    }
    return result;
  }
```

## TA Response
Hello,
Considering that your problem relates to how long the merge function is running it is important to ensure that if a while loop is in your program that it is being broken

## Fix
Prior to the fix the code for merge looked like this:

```
static List<String> merge(List<String> list1, List<String> list2) {
    List<String> result = new ArrayList<>();
    int index1 = 0, index2 = 0;
    while(index1 < list1.size() && index2 < list2.size()) {
      if(list1.get(index1).compareTo(list2.get(index2)) < 0) {
        result.add(list1.get(index1));
        
      }
      else if (list1.get(index1).compareTo(list2.get(index2)) == 0) {
        result.add(list1.get(index1));
        
      }
      else {
        result.add(list2.get(index2));
        
      }
    }
    while(index1 < list1.size()) {
      result.add(list1.get(index1));
      
    }
    while(index2 < list2.size()) {
      result.add(list2.get(index2));
      
    }
    return result;
  }
```

After the fix:

```
static List<String> merge(List<String> list1, List<String> list2) {
    List<String> result = new ArrayList<>();
    int index1 = 0, index2 = 0;
    while(index1 < list1.size() && index2 < list2.size()) {
      if(list1.get(index1).compareTo(list2.get(index2)) < 0) {
        result.add(list1.get(index1));
        index1 += 1;
      }
      else if (list1.get(index1).compareTo(list2.get(index2)) == 0) {
        result.add(list1.get(index1));
        index1 += 1;
        index2 += 1;
      }
      else {
        result.add(list2.get(index2));
        index2 += 1;
      }
    }
    while(index1 < list1.size()) {
      result.add(list1.get(index1));
      index1 += 1;
    }
    while(index2 < list2.size()) {
      result.add(list2.get(index2));
      index2 += 1;
    }
    return result;
  }
```

The problem was with the indexes were not being increased as they should have been leading to while loops that run forever.

Now running grade.sh returns this:

<img width="440" alt="image" src="https://github.com/VinMoeMac/cse15l-lab-reports/assets/130107058/7f450e58-07e7-4c90-82eb-929688ec4dbd">


## Setup Info
- First I had to git clone the grader for skill demo 2 with `git clone https://github.com/ucsd-cse15l-s23/grader-skill-demo2`
- After changing into the directory with `cd grader-skill-demo2` I was in a directory with these files: GradeServer.java grade.sh Server.java grading-area student-submission TestListExamples.java lib.
- I then had to use this command `bash grade.sh git@github.com:VinMoeMac/list-examples-duplicates.git` to run the code that I wanted from my github account.

# Part 2

## Reflection 
In this last half of the quarter I have learned a lot about bash scripts which I find to be a very useful for running things easier. I think there interesting, but a little tedious sometimes.
