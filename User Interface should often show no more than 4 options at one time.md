- `date created:` 2024-10-12 21:58
- `date modified:` `=dateformat(this.file.mtime, "yyyy-MM-dd HH:mm")`
- `tags:` #Practical-Application 
- `parents:` [[Grouping by 3-4 elements = fastest search]]

***

> [!tip] Practical application
> User Interface should often show no more than 4 options at one time.

***

# Details

Take your phone and open the settings. How many options do you see right at the start? On an iPhone 15 (iOS 17.6.1) there are <span style="color: #F33;"><b>27</b></span>. Upon going to "General" category there are <span style="color: #F33;"><b>18</b></span> options. On a OnePlus 7 phone (OxygenOS 12.1, Android 12) there are <span style="color: #F33;"><b>26</b></span>. Upon going deeper into "System Settings," there are <span style="color: #F33;"><b>16</b></span> options. Companies like these supposedly think about how to make the phone easier to use, yet no one considers how many options are visible to the user at one time.

It would be enough to carefully divide these settings into sections with a maximum of 4 items each, making everything much easier to find.

Regarding the iPhone vs. Android debate, there are some arguments that are repeated often, like:
- Android offers far more options for customising the phone to one’s needs.
- iPhone offers far fewer customisation options, but the default options, which cannot be changed, are usually very convenient for most users.
- Because iPhone has fewer configuration options, it is easier to use, as the user does not need to go through hundreds or even thousands of different options.
- So we have a trade-off situation: either the user can choose easier usage (iPhone) or more configuration options (Android).

But by using a division of 4, we can significantly increase the number of available configuration options without losing ease of use.

We can apply this same principle in many other places. Websites would be simpler for users if they employed divisions of 3-4. For example, it would be nice if the top navbar had 4 options instead of 7. If a training company offers, say, 100 courses, it would be better if they weren’t all thrown into one big basket but instead organised into categories and subcategories of 3-4 items each.

# Exceptions

Some user interfaces should not be designed this way. The main example is the main window in a program like MS Paint or Photoshop. Can you imagine if it only had 4 tools on a tool palette? That would not be comfortable at all. If we can assume that a user should undergo some training before using an application, and therefore he can be expected to memorise the existence and placement of multiple options on a given window, then sure, this should be taken into account and the application should be designed in such a way that a skilled user works the most efficiently.

Let's use long term memory to the fullest and allow the user to create custom keybindings too.

However the options visible after expanding on of the top buttons of an app, like "File", "Edit", "View" - those could often benefit from implementing the division by 4.

## IVR System

Scenario - you call Orange and hear:
- if you are calling about X - press 1,
- if about Y - press 2,
- ...
- if it’s something else - press 9

Suppose you choose 4, but the category didn’t sound exactly like what you needed, so you listened to all 9 options. After choosing 4, you hear another 9 options, and again none of them sounded like what you needed, but you decide that option 2 sounds like the nearest thing. Sometimes this is the end of it, but other times you’ll hear yet more options.

For the algorithm to be the fastest to get through, there should be a maximum of 3-4 options at each stage.

<span style="color: #F33;"><b>This one algorithm wastes so much time for so many people every single day that it’s almost unbelievable when you think about it.</b></span> Most likely one day of work by one person to improve this could save hundreds of hours per month for Orange customers or other companies with similar telephone systems.