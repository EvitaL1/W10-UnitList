# Extension: performance

This is an extension task.

You have been given an app to play with using Profiler. You will need to change some code and variables and take note of the performance.

The app shows a list (a RecyclerView) of strings with an icon. It also allows adding new items to the list.

For those who are unable to use Profiler on their personal setup, this might be a task to complete on campus if possible.


## Experimental setup

The app can be found at https://github.com/SDMD-2022/W10-UnitListLinks to an external site.. 

For the rest of this spec, bind() refers to the binding function in your ViewHolder, imageView is the variable name of your imageView, and R.drawable.image is the name of your drawable.

Your experiment has some variables:

- the type of icon, and where it is generated:
    - a fixed icon as a resource -- this needs to be decoded, which can be done on bind()
    - a generated icon -- this can be generated when the list object is initialised, or again in the bind() call
- the number of items in the list at start up. Start with 200 items; you might like to try up to 1000 if you have a particularly grunty computer.

## Process

1. Firstly ensure the app runs on your system. Run it and see how it works. Note what happens when the FAB is clicked.

1. Explore the code to ensure you are familiar with the code that needs to be adapted. In most cases this will be simply uncommenting and commenting code. There is no expectation that you will fix any errors. Add the code for each icon scenario as follows:

    - a constant icon: add the following to bind() in your adapter
imageView.setImageBitmap(BitmapFactory.decodeResource(itemView.context- resources, R.drawable.image))

    - a generated icon created on bind: add the following to bind() in your adapter
        imageView.setImageBitmap(item.drawIcon())

    - a generated icon but created on initialisation: add the following to bind() in your adapter
        imageView.setImageBitmap(item.icon)
        and ensure that you have this in your model:
        var icon: Bitmap? = drawIcon() // this needs to be null for the other scenarios!!

1. For each experimental scenario (icon types and length of list), use the Profiler to explore the performance of the app. Record your results.
1. Finally, reflect briefly on how performance could be improved by using concurrency, for example, when loading a large number of items into a list from a file. Note code is not required for this task.

##  The report

The report should consist of about 2-3 pages of text. Images can be included but do not contribute to the word count and should illustrate the text. No code submission is required for this task.

Your report should have an introduction and conclusion, and should clearly describe how you carried out this task.

The following questions might also guide you:

- Which of your scenarios performed the best? Why do you think this is?
- Which of your scenarios performed the worst? Why do you think this is?
- What is your takeaway from this task, especially in terms of working with lists and images?
- How could concurrent approaches assist with loading a large number of items from a file?

## Tips

Profiler is tricky to use on slower systems -- be aware of this when starting this task as it might take some time to collect the data you need.

