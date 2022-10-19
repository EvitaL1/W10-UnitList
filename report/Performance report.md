# Extension: performance

**Name:** Evita liu

**ID:** 103061916

## Introduction

Performance is an important factor in designing mobile applications. Mobile phones need efficient apps since they do not have as much processing power, RAM and power aas a dedicated desktop set up. 

This test aims to measure the perfomance of a simple android app using the profiler. The app generates a recycler view list of units with an image. There are different methods to create the image in the application - a constant icon, fixed icon or a generated icon. Furthermore the list size can be changed.

## Methodology

The different icon loading methods will be tested against a list of 200, 500, then 1000 items. 

1. Uncomment the function you want to test according to the [Extension: performance page](https://swinburne.instructure.com/courses/44802/pages/extension-performance?module_item_id=2777423) 
2. Set the list size to 200 in `MainActivity.kt`
3. Click the profile app icon and run the app and profiler
4. Record results for CPU, memory and energy use. More specific details below on what will be recorded.
   1. The beginning peak when the program starts
   2. The peak when pressing the FAB button
   3. No interaction with the app
   4. Scrolling through


## Results



## Discussion

- Which of your scenarios performed the best? Why do you think this is?
- Which of your scenarios performed the worst? Why do you think this is?
- What is your takeaway from this task, especially in terms of working with lists and images?
- How could concurrent approaches assist with loading a large number of items from a file?

## Conclusion

    reflect briefly on how performance could be improved by using concurrency, for example, when loading a large number of items into a list from a file. Note code is not required for this task.

# References