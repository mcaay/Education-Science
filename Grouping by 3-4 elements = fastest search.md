- `date created:` 2023-09-12 11:52
- `date modified:` `=dateformat(this.file.mtime, "yyyy-MM-dd HH:mm")`
- `tags:` #Strong-Fact 
- `parents:` [[Strong facts]]

***

> [!success] Fact
>  Grouping elements by 3 or 4 elements is optimal in terms of information finding speed.

***

# Short summary

In 1972, David K. Dirlam calculated how many chunks in memory would be optimal for the fastest information retrieval. We can compare this to folders on a computer and the situation where we need to find a file but have no idea where it is located.

For example, if we have 64 elements (files) in memory and all of them are in one "folder," then <span style="color: #F84;"><b>on average</b></span> (statistically), we would have to read $\frac{1 + 64}{2} = 32.5$ file names to find the correct file, and <span style="color: #F33;"><b>at most</b></span> 64 file names.

If we were to divide these 64 files into 2 levels of 8 files each, we would have 8 subfolders with 8 files each. Then, <span style="color: #F84;"><b>on average</b></span> we would need to read $\frac{1+8}{2} + \frac{1+8}{2} = 9$ file or folder names, and <span style="color: #F33;"><b>at most</b></span> $8 + 8 = 16$, which is already much less.

If we go even further and divide these files into 3 levels of 4 elements each, we have 4 folders, each containing 4 subfolders, which in turn contain 4 files each ($4^3=64$). Then, <span style="color: #F84;"><b>on average</b></span> we would need to read $\frac{1+4}{2} + \frac{1+4}{2} + \frac{1+4}{2} = 7.5$ file names, and <span style="color: #F33;"><b>at most</b></span> $4 + 4 + 4 = 12$, so again, even better than with 2 levels.

Let’s go even further and divide it into 6 levels of 2 elements each ($2^6=64$). Then, <span style="color: #F84;"><b>on average</b></span> we would need to read $\frac{1+2}{2} \cdot 6 = 9$ file names, and <span style="color: #F33;"><b>at most</b></span> $2 \cdot 6 = 12$, so this time, the <span style="color: #F84;"><b>average</b></span> number of file names to read is worse than with the division into 4 elements, but the <span style="color: #F33;"><b>maximum</b></span> number of files to read is just as good.

This simple numerical example has demonstrated that there is some optimal way of organising files in folders if our goal is to find the needed file as quickly as possible. Since files and folders are just one example of a place where data is organised, this will be relevant in very many other areas. This might not be so important when one person is looking for one file on his computer, but if **a million** people are looking for concrete information a couple of times a day in a large body of knowledge, it becomes **extremely important** to have this body of knowledge organised as optimally as possible.

So what is the most optimal way? Practically speaking, we can say that:
- the lowest <span style="color: #F84;"><b>average</b></span> number of checks occurs at division by <span style="color: #69F;"><b>4 elements</b></span>
	- 1st place - <span style="color: #69F;"><b>4 elements</b></span>
	- 2nd place - 3 elements - 0.9% more checks
	- 3rd place - 5 elements - 3.4% more checks
	- 4th place - 6 elements - 8.3% more checks
	- 5th place - 7 elements - 14.0% more checks
	- 6th place - 2 elements and 8 elements - 20.0% more checks
- the lowest <span style="color: #F33;"><b>maximum</b></span> number of checks occurs at division by <span style="color: #69F;"><b>3 elements</b></span>
	- 1st place - <span style="color: #69F;"><b>3 elements</b></span>
	- 2nd place - 2 elements and 4 elements - 5.7% more checks
	- 4th place - 5 elements - 13.8% more checks
	- 5th place - 6 elements - 22.6% more checks
	- 6th place - 7 elements - 31.7% more checks

The results presented above have some important caveats and possible variations, which are described further down in the note, but the general takeaway is that no matter from which perspective we look at the data, dividing by 3 or 4 elements is universally the most optimal.

The context for this research had more to do with a memory in a human brain rather than with files and folders. Since a related finding was that human working memory can hold only 4±1 elements at a given time, Dirlam wanted to find out that perhaps it is not bad that our working memory is so limited, but perhaps it is in some important aspects very optimal that our working memory is limited in this way.

# Scientific evidence

## Dirlam, 1972

The calculations done by Dirlam in his study are all included below and expanded upon in several places. The level of verbosity is also higher, so it might be easier to follow the calculations here than in the original paper.

### Considerations before diving into the math

In terms of memory, if we have 64 files and place them in folders, we end up with more things to remember than before. For example, if we divide these 64 files into 8 folders with 8 files each, we now have 64 files and 8 folder names to remember.

This raises the question: should we count these 8 additional folder names in the pool of things to remember or not?

Dirlam referenced other research and concluded that we should not count these folder names in the pool of things to remember, but he wasn't fully convinced and left the topic somewhat unfinished, subjectively speaking.

His argument for not counting them is: "folders" are like mnemonic devices (memory tricks) that bring order from chaos and improve learning speed and effectiveness, so their impact can be overlooked.

It's hard to agree with that. You could say that remembering various additional things helps in recalling the things we are interested in (advantage), but the need to dedicate more memory is still there (disadvantage). Folders do not really resemble mnemonic devices that much. A simple example of a mnemonic device is a technique that helps you remember long sequences of numbers, such as phone numbers or bank account numbers. In the simplest version, you imagine 3 things for each digit from zero to nine: a person, an action, and an object. Let's assume that:
- zero - Einstein, reading, book
- one - Napoleon, setting fire, cannon
- two - Shrek, hitting, club
- and so on.

When you get a string of numbers, for example, 012 121 201, you group the digits into three-element chunks and get strange scenes:
- 012 - Einstein sets fire to a club
- 121 - Napoleon hits a cannon
- 201 - Shrek reads some text on a cannon

Remembering three weird scenes is much easier than remembering nine digits, and the more digits there are, the easier it is to remember the scenes compared to the numbers.

Additionally, if someone places these scenes in order in a memory palace (another mnemonic technique), they can remember really long sequences of numbers. Masters have memorized three characters, actions, and objects not for each digit, but for each number from zero to 999. This allows them to memorize ridiculously long numbers, like a few thousand digits of pi.

But back to the topic—folder names do not seem to be "like mnemonic devices." If we move away from the analogy of files and folders towards small elements in human memory, such as specific words when learning a new language, a "folder" may take up a similar "amount" of memory as a "word."

We can look at this from another angle, which Dirlam did not address in his publication. In our question, we don't focus on whether version A requires memorizing more elements than version B. The question is solely about the speed of finding information. One possible answer is:

"The fewer chunks memory is divided into, down to a certain minimum (e.g., the number 4):
- the faster information retrieval is <span style="color: #9D5;"><b>(advantage)</b></span>
- but the more additional elements need to be remembered <span style="color: #F33;"><b>(disadvantage)</b></span>."

We are not claiming here that 3 or 4 chunks are always 100% the ideal, best choice. We simply found one specific application where 3 or 4 chunks are the best choice. There may be other applications or aspects where 3 or 4 chunks are not the best choice. To generally determine what number of chunks is best for the human brain, all of these applications or aspects would need to be tested, and weights would have to be assigned depending on the importance of each application, and then the weighted average would need to be checked. This would be interesting and difficult, and especially difficult, because some applications are more important to some people, so the weights could not be truly objective.

Nevertheless, out of curiosity, we also checked what number of chunks is optimal for search speed if category names or "folders" can also be something we are looking for.

One more thought worth considering—regardless of whether we want to include category or "folder" names in the pool of things to remember, the shape of the memory tree is exactly the same. Put another way, using our example—if we have 64 files and place them in 8 subfolders, we have 8 folder names to remember, but it's not like there are suddenly 64 + 8 = 72 elements on the last level of the tree. On the last level, there are still only 64 elements. If we are searching for a folder, not a file, we will statistically find it faster because it is on a higher level of the tree.

### Purely mathematical results

Purely mathematical results refer to answering the question: *"If we determine the function of the average or maximum number of checks depending on how many chunks the memory is divided into, at what chunk size will the function reach its minimum?"*. Here, the result can be a non-integer number, while in the practical results section, the results will concern only integers, as you cannot have memory divided into, for example, 3 and a half elements.

- if <span style="color: #9D5;"><b>additional elements</b></span> (categories - "folders") <span style="color: #9D5;"><b>can be omitted</b></span>
	- the lowest <span style="color: #F84;"><b>average</b></span> number of checks occurs at <span style="color: #69F;"><b>3.59 elements</b></span>
	- the lowest <span style="color: #F33;"><b>maximum</b></span> number of checks occurs at <span style="color: #69F;"><b>2.72 elements</b></span>
- if <span style="color: #E8F;"><b>additional elements cannot be omitted</b></span>
	- the lowest <span style="color: #F84;"><b>average</b></span> number of checks occurs at <span style="color: #69F;"><b>2.72 elements</b></span>
	- the lowest <span style="color: #F33;"><b>maximum</b></span> number of checks occurs at <span style="color: #69F;"><b>2.72 elements</b></span>

### Practical results

- if <span style="color: #9D5;"><b>additional elements</b></span> (categories - "folders") <span style="color: #9D5;"><b>can be omitted</b></span>
	- the lowest <span style="color: #F84;"><b>average</b></span> number of checks occurs at <span style="color: #69F;"><b>4 elements</b></span>
		- 1st place - <span style="color: #69F;"><b>4 elements</b></span>
		- 2nd place - 3 elements - 0.9% more checks
		- 3rd place - 5 elements - 3.4% more checks
		- 4th place - 6 elements - 8.3% more checks
		- 5th place - 7 elements - 14.0% more checks
		- 6th place - 2 elements and 8 elements - 20.0% more checks
	- the lowest <span style="color: #F33;"><b>maximum</b></span> number of checks occurs at <span style="color: #69F;"><b>3 elements</b></span>
		- 1st place - <span style="color: #69F;"><b>3 elements</b></span>
		- 2nd place - 2 elements and 4 elements - 5.7% more checks
		- 4th place - 5 elements - 13.8% more checks
		- 5th place - 6 elements - 22.6% more checks
		- 6th place - 7 elements - 31.7% more checks
- if <span style="color: #E8F;"><b>additional elements cannot be omitted</b></span>
	- the lowest <span style="color: #F84;"><b>average</b></span> number of checks occurs at <span style="color: #69F;"><b>3 elements</b></span>
		- 1st place - <span style="color: #69F;"><b>3 elements</b></span>
		- 2nd place - 2 elements and 4 elements - from 4.9% (for $n = 10$) to 5.6% (for $n = 10^{12}$) more checks
		- 4th place - 5 elements - from 11.9% (for $n = 10$) to 13.6% (for $n = 10^{12}$) more checks
		- 5th place - 6 elements - from 19.5% (for $n = 10$) to 22.3% (for $n = 10^{12}$) more checks
		- 6th place - 7 elements - from 27.4% (for $n = 10$) to 31.3% (for $n = 10^{12}$) more checks
	- the lowest <span style="color: #F33;"><b>maximum</b></span> number of checks occurs at <span style="color: #69F;"><b>3 elements</b></span> - since finding the folder name would mean performing fewer checks than the maximum, the results here are identical to the case where additional elements (categories - "folders") can be omitted

We obtained 4 different result categories, where the division into 3 elements won in three, and the division into 4 elements won in one. In my opinion, the most important categories are those concerning the <span style="color: #F84;"><b>average</b></span> number of checks, as optimizing the <span style="color: #F84;"><b>average</b></span> search time means the least wasted time in life or, for example, processor time.

There are applications where the <span style="color: #F33;"><b>maximum</b></span> path could be the most crucial, especially if the search process must fit within a specific time frame. However, these are exceptional cases. One example is when a server has a set amount of time to respond to a query and if it doesn’t respond within this time, the system will return an error, such as a connection error.

In one of the <span style="color: #F84;"><b>average</b></span> categories, the division into 3 won (decisively, by about 5%), and in the other, the division into 4 (narrowly, by 0.9%). Which of these two categories is more important? It might depend on the specific application, but in the case of folders and files on a computer, it’s common to have a situation where a folder contains, for example, one file (an end element) and two subfolders. In such a non-uniform "tree," which category wins? If we’re always interested in the final file, then it seems that division into 4 wins. However, sometimes we want to find a folder to, for example, compress it and send it to someone. If someone does this often, then the division into 3 could win. Normally, though, this is a relatively less frequent situation than searching for a file to work with, so personally, I’d lean towards the division into 4.

Since it’s impractical to enforce a rule that every folder must have exactly 4 elements, the best practical rule might be that a folder can have up to 4 elements (with some allowed exceptions—see [[Grouping by 3-4 elements = fastest search#Additional conclusions|Additional conclusions]]). If it has 3 elements, that’s also great. Even if it has two, it’s less optimal, but still quite good. If it has one, it might seem pointless at first glance, but a logical justification can be made. For example, we may receive a file whose name cannot be changed, but the name is misleading or hard to identify what’s inside the file. In this case, we can give a meaningful name to the folder that contains this single file.

### Mathematics of purely mathematical results

Let:
- $y_n, y_m$ - the <span style="color: #F84;"><b>average</b></span> number of elements checked until the desired element is found, respectively <span style="color: #9D5;"><b>excluding categories</b></span> and <span style="color: #E8F;"><b>including categories</b></span>
- $z_n, z_m$ - the <span style="color: #F33;"><b>maximum</b></span> number of elements checked until the desired element is found, respectively <span style="color: #9D5;"><b>excluding categories</b></span> and <span style="color: #E8F;"><b>including categories</b></span>
- $x$ - the number of chunks into which one chunk, or "parent," is divided
- $u$ - the number of memory levels - e.g., the number of folder levels
- $n$ - the total number of elements to remember <span style="color: #9D5;"><b>excluding categories</b></span> ("folder names")
- $m$ - the total number of elements to remember <span style="color: #E8F;"><b>including categories</b></span> ("folder names")
- parent - a parent element in memory, similar to a folder on a computer that contains child elements, which can be other folders or files
- child - a child element in memory, similar to a folder or file on a computer, which is placed in a parent folder

Assumptions:
- Elements in memory are unordered, so it is not possible to predict whether the desired element is the first, last, or somewhere in the middle on a given level. In the case of folders and files, if folders are sorted by date in ISO format (i.e., "YYYY-MM-DD"), it could be quicker to find the correct folder than reading folder names from top to bottom. Generally, however, memory does not work like this, so we must assume that elements are unordered, and the search is random, meaning each element has an equal probability of being the correct one.

#### Step 1 - Calculating $y_n$

If $x = 4$, meaning one parent has 4 children, then, on <span style="color: #F84;"><b>average</b></span>, it takes 2.5 checks to select the desired child. This is simply the arithmetic mean of the possible number of checks, meaning we might find it on the first try, the second, etc. ($\frac{1+2+3+4}{4}$). Since this is the case at each level of memory, we can write the function formula as:
$$ y = \frac{1+x}{2} \cdot u $$
However, we would not want the function result to depend on $u$, because the value of $u$ depends on $x$. The function result can, however, depend on the total number of elements in memory, as this does not depend on $x$.
$$ n = x^u \implies \log_x(n) = u \implies u = \frac{\ln(n)}{\ln(x)} $$
Substituting:
$$ y_n = \frac{1+x}{2} \cdot \frac{\ln(n)}{\ln(x)} = \frac{\ln(n)}{2} \cdot \frac{1+x}{\ln(x)} $$
Assuming that $n$ is not a variable, let’s take $n=64$ to see how this function’s graph looks:

![[Pasted image 20230823120429.png|300]] ![[Pasted image 20230823120502.png|300]]

The case where $x < 1$ does not concern us, as memory cannot be less than 1-chunk. For $x > 1$, we see that the graph of $y_n(x)$ has a single global minimum, which is exactly what we want to find, or more specifically, for which $x$ this global minimum occurs.

To find this $x$, we need to locate where the derivative of $y_n$ is zero:
$$ (y_n)' = \frac{\ln(n)}{2} \cdot \left(\frac{1+x}{\ln(x)}\right)' = \frac{\ln(n)}{2} \cdot \frac{1\cdot\ln(x) - (1+x)\cdot\frac{1}{x}}{\ln^2(x)} = $$
$$ = \frac{\ln(n)}{2} \cdot \frac{\ln(x) - \left(\frac{1}{x}+1\right)}{\ln^2(x)} $$
$$ (y_n)' = 0 \iff \ln(x) - \left(\frac{1}{x}+1\right) = 0 \implies \ln(x) = \frac{1}{x} + 1 $$
It’s not easy to solve for $x$ from this equation, but by knowing the graphs of both sides of the equation, we know that for $x > 1$, these graphs will intersect at some point.

![[Pasted image 20230823122627.png|450]]

Taking the easy route, the website wolframalpha.com gives us the result of this equation as approximately 3.59112:
![[Pasted image 20230823122945.png|400]]

Without taking the easy route, the simplest way would be to check this programmatically, i.e., by increasing $x$ by 0.01, for example, and checking where the difference between the values of these functions is smallest—this would yield 3.59.

Output of my function:
```
x: 3.57  |  ln(x) = 1.27257  |  1 + 1/x = 1.28011  |  diff = 0.00754
x: 3.58  |  ln(x) = 1.27536  |  1 + 1/x = 1.27933  |  diff = 0.00397
x: 3.59  |  ln(x) = 1.27815  |  1 + 1/x = 1.27855  |  diff = 0.00040
x: 3.60  |  ln(x) = 1.28093  |  1 + 1/x = 1.27778  |  diff = 0.00315
x: 3.61  |  ln(x) = 1.28371  |  1 + 1/x = 1.27701  |  diff = 0.00670
x: 3.62  |  ln(x) = 1.28647  |  1 + 1/x = 1.27624  |  diff = 0.01023
```

#### Step 2 - Calculating $z_n$

If $x = 4$, meaning one parent has 4 children, then, at <span style="color: #F33;"><b>maximum</b></span>, it takes 4 checks to select the desired child. Since this is the case at each level of memory, we can write the function formula as:
$$ z = x \cdot u $$
To ensure the function result does not depend on $u$, we will replace $u$ with $x$ and $n$ as we did in step 1:
$$ n = x^u \implies \log_x(n) = u \implies u = \frac{\ln(n)}{\ln(x)} $$
Substituting:
$$ z_n = x \cdot \frac{\ln(n)}{\ln(x)} = \ln(n) \cdot \frac{x}{\ln(x)} $$
Assuming that $n$ is not a variable, let’s take $n=64$ to see how this function’s graph looks:

![[Pasted image 20230824112810.png|300]] ![[Pasted image 20230824112841.png|300]]

The case where $x < 1$ does not concern us, as memory cannot be less than 1-chunk. For $x > 1$, we see that the graph of $z_n(x)$ has a single global minimum.

To find the desired $x$, we need to locate where the derivative of $z_n$ is zero:
$$ (z_n)' = \ln(n) \cdot (\frac{x}{\ln(x)})' = \ln(n) \cdot \frac{1\cdot\ln(x) - x \cdot \frac{1}{x}}{\ln^2(x)} = $$
$$ = \ln(n) \cdot \frac{\ln(x) - 1}{\ln^2(x)} $$
$$ (z_n)' = 0 \iff \ln(x) - 1 = 0 \implies \ln(x) = 1 \implies x = e \approx 2,72$$
#### Step 3 - Calculating $y_m$

To account for remembering categories, the initial formula changes. To explain how to calculate this, let’s take $n = 64$ and $x = 4$ as an example. Then we have $u = 3$ levels. If we are searching for a category instead of the final element, our search may end earlier, perhaps even on the first level. For visual support, let’s look at the following memory structure:

```
1
    11
        111
        112
        113
        114
    12
        ...
    13
	    ...
    14
	    ...
2 ...
3 ...
4 ...
```

On the first level, we still have 4 options, so the average number of searches is, as before, $\frac{1+4}{2} = 2.5$. On the second level, we have 4 standard options (e.g., 11, 12, 13, 14 in the example above) plus a fifth "zero" option. The "zero" option means we were searching for the "folder we just entered," which, in the example above, is element "1". In other words, when descending one level into a folder, one of the possible options is zero searches. Thus, the average number of searches at a given level is the arithmetic mean of 0, 1, 2, 3, and 4, which equals 2. This is the case for all subsequent levels except the first level. The formula for the average number of searches is therefore:
$$ y_m = \frac{1+x}{2} + \frac{0 + x}{2} \cdot (u - 1) = \frac{1 + x + xu - x}{2} = \frac{1}{2} + \frac{u}{2} x $$
As in step 1, the formula for $u$ is:
$$ u = \frac{\ln(n)}{\ln(x)} $$
Substituting:
$$ y_m = \frac{\ln(n)}{2} \cdot \frac{x}{\ln(x)} + \frac{1}{2} $$
The graph of the function for $n = 64$ is as follows:

![[Pasted image 20230825150122.png|300]] ![[Pasted image 20230825150136.png|309]]

The case where $x < 1$ does not concern us, as memory cannot be less than 1-chunk. For $x > 1$, we see that the graph of $y_n(x)$ has a single global minimum, which is exactly what we want to find, or more specifically, for which $x$ this global minimum occurs.

To find this $x$, we need to locate where the derivative of $y_m$ is zero:
$$ (y_n)' = \frac{\ln(n)}{2} \cdot (\frac{x}{\ln(x)})' + (\frac{1}{2})' = \frac{\ln(n)}{2} \cdot \frac{\ln(x) - 1}{\ln^2(x)} $$
$$ (y_m)' = 0 \iff \ln(x) - 1 = 0 \implies \ln(x) = 1 \implies x = e \approx 2,72 $$

#### Step 4 - Calculating $z_m$

This is the simplest part. Since we are looking for the <span style="color: #F33;"><b>maximum</b></span> number of elements checked, it is the same as in step 2. Category names would be found "along the way", so they wouldn’t be part of the longest path through the possibility tree. Therefore, $z_m = z_n$, and the minimum value of $z_m$ is achieved for $x = e \approx 2.72$.

### Mathematics of practical results

#### Step 1 - Optimizing $y_n$

We need the formula determined in [[Grouping by 3-4 elements = fastest search### Step 1 - Calculating $y_n$|step 1 of the purely mathematical results]], which is:
$$ y_n = \frac{\ln(n)}{2} \cdot \frac{1+x}{\ln(x)} $$
By substituting natural numbers from 2 to 9, we can check which real division is the most optimal. It is also interesting to see how these results change for different values of $n$, so I used programming for convenience. The code below:

```python
from math import log
import pandas as pd


def calculate_chunk_score(n, x):
    score = log(n)/2 * (x + 1)/log(x)
    return f"${score:.2f}$"


interesting_n = [64, 100, 10**4, 10**6, 10**9, 10**12]
interesting_x = list(range(2, 10))
results = []
for x in interesting_x:
    chunk_results = [calculate_chunk_score(n, x)
                     for n in interesting_n]
    results.append(chunk_results)
headers = [f"$n={n}$"
		   for n in r"64 100 10^4 10^6 10^9 10^{12}".split()]
indices = [f"$x={x}$" for x in interesting_x]
print(pd.DataFrame(results,
                   columns=headers,
                   index=indices)
      .to_markdown())
```

generates the following table of $y_n(x)$ values:

|                                                |                                          $n=64$ |                                         $n=100$ |                                         $n=10^4$ |                                         $n=10^6$ |                                         $n=10^9$ |                                        $n=10^{12}$ |
| ----------------------------------------------:| -----------------------------------------------:| -----------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:|
|                                          $x=2$ |                                          $9.00$ |                                          $9.97$ |                                          $19.93$ |                                          $29.90$ |                                          $44.85$ |                                          $59.79$ |
|                                          $x=3$ |                                          $7.57$ |                                          $8.38$ |                                          $16.77$ |                                          $25.15$ |                                          $37.73$ |                                          $50.30$ |
| <span style="color: #9D5;"><b>$x=4$</b></span> | <span style="color: #9D5;"><b>$7.50$</b></span> | <span style="color: #9D5;"><b>$8.30$</b></span> | <span style="color: #9D5;"><b>$16.61$</b></span> | <span style="color: #9D5;"><b>$24.91$</b></span> | <span style="color: #9D5;"><b>$37.37$</b></span> | <span style="color: #9D5;"><b>$49.83$</b></span> |
|                                          $x=5$ |                                          $7.75$ |                                          $8.58$ |                                          $17.17$ |                                          $25.75$ |                                          $38.63$ |                                          $51.50$ |
|                                          $x=6$ |                                          $8.12$ |                                          $9.00$ |                                          $17.99$ |                                          $26.99$ |                                          $40.48$ |                                          $53.97$ |
|                                          $x=7$ |                                          $8.55$ |                                          $9.47$ |                                          $18.93$ |                                          $28.40$ |                                          $42.60$ |                                          $56.80$ |
|                                          $x=8$ |                                          $9.00$ |                                          $9.97$ |                                          $19.93$ |                                          $29.90$ |                                          $44.85$ |                                          $59.79$ |
|                                          $x=9$ |                                          $9.46$ |                                         $10.48$ |                                          $20.96$ |                                          $31.44$ |                                          $47.16$ |                                          $62.88$ |

from which we can clearly see which $x$ values are the most optimal. Let's derive a formula for the percentage by which $x_2$ requires more checks compared to $x_1$:
$$ \frac{y_{n}(x_2)}{y_{n}(x_1)} \cdot 100\% - 100\% = \frac{\frac{\ln(n)}{2} \cdot \frac{1+x_2}{\ln(x_2)}} {\frac{\ln(n)}{2} \cdot \frac{1+x_1}{\ln(x_1)}} \cdot 100\% - 100\% = $$
$$ = \frac{\ln(x_1)}{\ln(x_2)} \cdot \frac{1+x_2}{1+x_1} \cdot 100\% - 100\% $$
As we can see, $n$ does not affect this percentage at all. By adding the following piece of code:

```python
def calculate_percent_difference(x1, x2):
    # x2 should be worse than x1
    percent = log(x1)/log(x2) * (1+x2)/(1+x1) * 100 - 100
    return f"$+{percent:.1f}\%$"


non_winning_x = [2, 3, 5, 6, 7, 8, 9]
results2 = []
for x in non_winning_x:
    chunk_results = [calculate_percent_difference(4, x)
                     for n in interesting_n]
    results2.append(chunk_results)

results2[2:2] = [results[2]]
print(pd.DataFrame(results2,
                   columns=headers,
                   index=indices)
      .to_markdown())
```

we obtain the following table:

|                                                |                                          $n=64$ |                                         $n=100$ |                                         $n=10^4$ |                                         $n=10^6$ |                                         $n=10^9$ |                                      $n=10^{12}$ |
| ----------------------------------------------:| -----------------------------------------------:| -----------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:|
|                                          $x=2$ |                                       $+20.0\%$ |                                       $+20.0\%$ |                                        $+20.0\%$ |                                        $+20.0\%$ |                                        $+20.0\%$ |                                        $+20.0\%$ |
|                                          $x=3$ |                                        $+0.9\%$ |                                        $+0.9\%$ |                                         $+0.9\%$ |                                         $+0.9\%$ |                                         $+0.9\%$ |                                         $+0.9\%$ |
| <span style="color: #9D5;"><b>$x=4$</b></span> | <span style="color: #9D5;"><b>$7.50$</b></span> | <span style="color: #9D5;"><b>$8.30$</b></span> | <span style="color: #9D5;"><b>$16.61$</b></span> | <span style="color: #9D5;"><b>$24.91$</b></span> | <span style="color: #9D5;"><b>$37.37$</b></span> | <span style="color: #9D5;"><b>$49.83$</b></span> |
|                                          $x=5$ |                                        $+3.4\%$ |                                        $+3.4\%$ |                                         $+3.4\%$ |                                         $+3.4\%$ |                                         $+3.4\%$ |                                         $+3.4\%$ |
|                                          $x=6$ |                                        $+8.3\%$ |                                        $+8.3\%$ |                                         $+8.3\%$ |                                         $+8.3\%$ |                                         $+8.3\%$ |                                         $+8.3\%$ |
|                                          $x=7$ |                                       $+14.0\%$ |                                       $+14.0\%$ |                                        $+14.0\%$ |                                        $+14.0\%$ |                                        $+14.0\%$ |                                        $+14.0\%$ |
|                                          $x=8$ |                                       $+20.0\%$ |                                       $+20.0\%$ |                                        $+20.0\%$ |                                        $+20.0\%$ |                                        $+20.0\%$ |                                        $+20.0\%$ |
|                                          $x=9$ |                                       $+26.2\%$ |                                       $+26.2\%$ |                                        $+26.2\%$ |                                        $+26.2\%$ |                                        $+26.2\%$ |                                        $+26.2\%$ |

#### Step 2 - Optimizing $z_n$

This time, we need the formula determined in [[Grouping by 3-4 elements = fastest search### Step 2 - Calculating $z_n$|step 2 of the purely mathematical results]], which is:
$$ z_n = \ln(n) \cdot \frac{x}{\ln(x)} $$
With this formula, we will generate a table of interesting $z_n(x)$ results. We can use the same code as in step 1, just changing the function definition:

```python
def calculate_chunk_score(n, x):
    score = log(n) * x/log(x)
    return f"${score:.2f}$"
```

|                                                |                                           $n=64$ |                                          $n=100$ |                                         $n=10^4$ |                                         $n=10^6$ |                                         $n=10^9$ |                                      $n=10^{12}$ |
| ----------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:|
|                                          $x=2$ |                                          $12.00$ |                                          $13.29$ |                                          $26.58$ |                                          $39.86$ |                                          $59.79$ |                                          $79.73$ |
| <span style="color: #9D5;"><b>$x=3$</b></span> | <span style="color: #9D5;"><b>$11.36$</b></span> | <span style="color: #9D5;"><b>$12.58$</b></span> | <span style="color: #9D5;"><b>$25.15$</b></span> | <span style="color: #9D5;"><b>$37.73$</b></span> | <span style="color: #9D5;"><b>$56.59$</b></span> | <span style="color: #9D5;"><b>$75.45$</b></span> |
|                                          $x=4$ |                                          $12.00$ |                                          $13.29$ |                                          $26.58$ |                                          $39.86$ |                                          $59.79$ |                                          $79.73$ |
|                                          $x=5$ |                                          $12.92$ |                                          $14.31$ |                                          $28.61$ |                                          $42.92$ |                                          $64.38$ |                                          $85.84$ |
|                                          $x=6$ |                                          $13.93$ |                                          $15.42$ |                                          $30.84$ |                                          $46.26$ |                                          $69.40$ |                                          $92.53$ |
|                                          $x=7$ |                                          $14.96$ |                                          $16.57$ |                                          $33.13$ |                                          $49.70$ |                                          $74.55$ |                                          $99.40$ |
|                                          $x=8$ |                                          $16.00$ |                                          $17.72$ |                                          $35.43$ |                                          $53.15$ |                                          $79.73$ |                                         $106.30$ |
|                                          $x=9$ |                                          $17.04$ |                                          $18.86$ |                                          $37.73$ |                                          $56.59$ |                                          $84.88$ |                                         $113.18$ |

Formula for the percentage by which $x_2$ requires more checks compared to $x_1$:
$$ \frac{z_{n}(x_2)}{z_{n}(x_1)} \cdot 100\% - 100\% = \frac{\ln(n) \cdot \frac{x_2}{\ln(x_2)}} {\ln(n) \cdot \frac{x_1}{\ln(x_1)}} \cdot 100\% - 100\% = $$
$$ = \frac{\ln(x_1)}{\ln(x_2)} \cdot \frac{x_2}{x_1} \cdot 100\% - 100\% $$

In this case, $n$ also does not affect the percentage. Since the division into 3 won here, a larger piece of code needs to be changed:

```python
def calculate_percent_difference(x1, x2):
    # x2 should be worse than x1
    percent = log(x1)/log(x2) * x2/x1 * 100 - 100
    return f"$+{percent:.1f}\%$"


non_winning_x = [2, 4, 5, 6, 7, 8, 9]
results2 = []
for x in non_winning_x:
    chunk_results = [calculate_percent_difference(3, x)
                     for n in interesting_n]
    results2.append(chunk_results)

results2[1:1] = [results[1]]
print(pd.DataFrame(results2,
                   columns=headers,
                   index=indices)
      .to_markdown())
```

to obtain the table we are interested in:

|                                                |                                           $n=64$ |                                          $n=100$ |                                         $n=10^4$ |                                         $n=10^6$ |                                         $n=10^9$ |                                      $n=10^{12}$ |
| ----------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:|
|                                          $x=2$ |                                         $+5.7\%$ |                                         $+5.7\%$ |                                         $+5.7\%$ |                                         $+5.7\%$ |                                         $+5.7\%$ |                                         $+5.7\%$ |
| <span style="color: #9D5;"><b>$x=3$</b></span> | <span style="color: #9D5;"><b>$11.36$</b></span> | <span style="color: #9D5;"><b>$12.58$</b></span> | <span style="color: #9D5;"><b>$25.15$</b></span> | <span style="color: #9D5;"><b>$37.73$</b></span> | <span style="color: #9D5;"><b>$56.59$</b></span> | <span style="color: #9D5;"><b>$75.45$</b></span> |
|                                          $x=4$ |                                         $+5.7\%$ |                                         $+5.7\%$ |                                         $+5.7\%$ |                                         $+5.7\%$ |                                         $+5.7\%$ |                                         $+5.7\%$ |
|                                          $x=5$ |                                        $+13.8\%$ |                                        $+13.8\%$ |                                        $+13.8\%$ |                                        $+13.8\%$ |                                        $+13.8\%$ |                                        $+13.8\%$ |
|                                          $x=6$ |                                        $+22.6\%$ |                                        $+22.6\%$ |                                        $+22.6\%$ |                                        $+22.6\%$ |                                        $+22.6\%$ |                                        $+22.6\%$ |
|                                          $x=7$ |                                        $+31.7\%$ |                                        $+31.7\%$ |                                        $+31.7\%$ |                                        $+31.7\%$ |                                        $+31.7\%$ |                                        $+31.7\%$ |
|                                          $x=8$ |                                        $+40.9\%$ |                                        $+40.9\%$ |                                        $+40.9\%$ |                                        $+40.9\%$ |                                        $+40.9\%$ |                                        $+40.9\%$ |
|                                          $x=9$ |                                        $+50.0\%$ |                                        $+50.0\%$ |                                        $+50.0\%$ |                                        $+50.0\%$ |                                        $+50.0\%$ |                                        $+50.0\%$ |

#### Step 3 - Optimizing $y_m$

The formula determined in [[Grouping by 3-4 elements = fastest search### Step 3 - Calculating $y_m$|step 3 of the purely mathematical results]], which is:
$$ y_m = \frac{\ln(n)}{2} \cdot \frac{x}{\ln(x)} + \frac{1}{2} $$

Similar to step 2, here we can also use the code from step 1, changing only the function definition:

```python
def calculate_chunk_score(n, x):
    score = log(n)/2 * x/log(x) + 0.5
    return f"${score:.2f}$"
```

and we obtain the following table:

|                                                |                                          $n=64$ |                                         $n=100$ |                                         $n=10^4$ |                                         $n=10^6$ |                                         $n=10^9$ |                                      $n=10^{12}$ |
| ----------------------------------------------:| -----------------------------------------------:| -----------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:|
|                                          $x=2$ |                                          $6.50$ |                                          $7.14$ |                                          $13.79$ |                                          $20.43$ |                                          $30.40$ |                                          $40.36$ |
| <span style="color: #9D5;"><b>$x=3$</b></span> | <span style="color: #9D5;"><b>$6.18$</b></span> | <span style="color: #9D5;"><b>$6.79$</b></span> | <span style="color: #9D5;"><b>$13.08$</b></span> | <span style="color: #9D5;"><b>$19.36$</b></span> | <span style="color: #9D5;"><b>$28.79$</b></span> | <span style="color: #9D5;"><b>$38.23$</b></span> |
|                                          $x=4$ |                                          $6.50$ |                                          $7.14$ |                                          $13.79$ |                                          $20.43$ |                                          $30.40$ |                                          $40.36$ |
|                                          $x=5$ |                                          $6.96$ |                                          $7.65$ |                                          $14.81$ |                                          $21.96$ |                                          $32.69$ |                                          $43.42$ |
|                                          $x=6$ |                                          $7.46$ |                                          $8.21$ |                                          $15.92$ |                                          $23.63$ |                                          $35.20$ |                                          $46.76$ |
|                                          $x=7$ |                                          $7.98$ |                                          $8.78$ |                                          $17.07$ |                                          $25.35$ |                                          $37.77$ |                                          $50.20$ |
|                                          $x=8$ |                                          $8.50$ |                                          $9.36$ |                                          $18.22$ |                                          $27.08$ |                                          $40.36$ |                                          $53.65$ |
|                                          $x=9$ |                                          $9.02$ |                                          $9.93$ |                                          $19.36$ |                                          $28.79$ |                                          $42.94$ |                                          $57.09$ |

Formula for the percentage by which $x_2$ requires more checks compared to $x_1$:
$$ \frac{y_{m}(x_2)}{y_{m}(x_1)} \cdot 100\% - 100\% = \frac{\frac{\ln(n)}{2} \cdot \frac{x_2}{\ln(x_2)} + \frac{1}{2}} {\frac{\ln(n)}{2} \cdot \frac{x_1}{\ln(x_1)} + \frac{1}{2}} \cdot 100\% - 100\% $$

In this case, $n$ does affect the result. The code to generate the second table is as follows:

```python
def calculate_percent_difference(n, x1, x2):
    # x2 should be worse than x1
    score1 = log(n)/2 * x1/log(x1) + 0.5
    score2 = log(n)/2 * x2/log(x2) + 0.5
    percent = score2 / score1 * 100 - 100
    return f"$+{percent:.1f}\%$"


non_winning_x = [2, 4, 5, 6, 7, 8, 9]
results2 = []
for x in non_winning_x:
    chunk_results = [calculate_percent_difference(n, 3, x)
                     for n in interesting_n]
    results2.append(chunk_results)

results2[1:1] = [results[1]]
print(pd.DataFrame(results2,
                   columns=headers,
                   index=indices)
      .to_markdown())
```

from which we obtain:

|                                                |                                          $n=64$ |                                         $n=100$ |                                         $n=10^4$ |                                         $n=10^6$ |                                         $n=10^9$ |                                      $n=10^{12}$ |
| ----------------------------------------------:| -----------------------------------------------:| -----------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:|
|                                          $x=2$ |                                        $+5.2\%$ |                                        $+5.2\%$ |                                         $+5.4\%$ |                                         $+5.5\%$ |                                         $+5.6\%$ |                                         $+5.6\%$ |
| <span style="color: #9D5;"><b>$x=3$</b></span> | <span style="color: #9D5;"><b>$6.18$</b></span> | <span style="color: #9D5;"><b>$6.79$</b></span> | <span style="color: #9D5;"><b>$13.08$</b></span> | <span style="color: #9D5;"><b>$19.36$</b></span> | <span style="color: #9D5;"><b>$28.79$</b></span> | <span style="color: #9D5;"><b>$38.23$</b></span> |
|                                          $x=4$ |                                        $+5.2\%$ |                                        $+5.2\%$ |                                         $+5.4\%$ |                                         $+5.5\%$ |                                         $+5.6\%$ |                                         $+5.6\%$ |
|                                          $x=5$ |                                       $+12.7\%$ |                                       $+12.8\%$ |                                        $+13.2\%$ |                                        $+13.4\%$ |                                        $+13.5\%$ |                                        $+13.6\%$ |
|                                          $x=6$ |                                       $+20.8\%$ |                                       $+21.0\%$ |                                        $+21.8\%$ |                                        $+22.0\%$ |                                        $+22.2\%$ |                                        $+22.3\%$ |
|                                          $x=7$ |                                       $+29.2\%$ |                                       $+29.4\%$ |                                        $+30.5\%$ |                                        $+30.9\%$ |                                        $+31.2\%$ |                                        $+31.3\%$ |
|                                          $x=8$ |                                       $+37.6\%$ |                                       $+37.9\%$ |                                        $+39.3\%$ |                                        $+39.8\%$ |                                        $+40.2\%$ |                                        $+40.4\%$ |
|                                          $x=9$ |                                       $+46.0\%$ |                                       $+46.3\%$ |                                        $+48.1\%$ |                                        $+48.7\%$ |                                        $+49.1\%$ |                                        $+49.3\%$ |

#### Step 4 - Optimizing $z_m$

The results are the same as in [[Grouping by 3-4 elements = fastest search### Step 2 - Optimizing $z_n$|step 2]]. Explanation can be found in [[Grouping by 3-4 elements = fastest search### Step 4 - Calculating $z_m$|step 4 of the purely mathematical results]].


***

# References

1. Dirlam, D. K. (1972). Most efficient chunk sizes. _Cognitive Psychology, 3_(2), 255–359. [https://doi.org/10.1016/0010-0285(72)90012-6](https://psycnet.apa.org/doi/10.1016/0010-0285(72)90012-6)

