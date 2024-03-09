# Elixir

_9/3/2024_

## Do we really need another language?

Back in the old days, before the 90s, we largely used to manually manage our memory.  In a language like C or C++ any items that we wanted to store in memory which weren't a fixed size would be stored on the _heap_, and we'd need to allocate space for them beforehand, and deallocate the space for them afterwards.

This type of memory management lead to a large number of bugs and placed a burden on the programmer.  They are a cause of an important security flaw, the [buffer overflow](https://en.wikipedia.org/wiki/Buffer_overflow).

While there were other languages with memory management, when [Java](https://en.wikipedia.org/wiki/Java_(programming_language)) came along it was clear that for the vast majority of tasks,  automatically managing memory was the future.  Introducing a language without a form of memory management today simply would not make sense.  [Java](https://en.wikipedia.org/wiki/Java_(programming_language)) made you more productive than what came before it.

[Java](https://en.wikipedia.org/wiki/Java_(programming_language)) used a form of memory management called [garbage collection](https://en.wikipedia.org/wiki/Garbage_collection_(computer_science)). There have been many improvements to the first garbage collector for java, but it was the introduction of this new technology that shifted the landscape.

I think [Elixir](https://en.wikipedia.org/wiki/Elixir_(programming_language)) does the same for parallel computing.

### Why parallel computing is important

The answer is in hardware. In the 60s, Gordon Moore observed that every 2 years we were doubling the number of components per integrated circuit.  This became known as [Moore's Law](https://en.wikipedia.org/wiki/Moore%27s_law).  Year after year our computer chips sped up, and that new power drove new applications.

This was partly due to another observation called [Dennard Scaling](https://en.wikipedia.org/wiki/Dennard_scaling).  This basically meant that as transistors get smaller, the power required to drive them is less.  Less power = less heat, and less heat = faster clocks. Combining these two ideas, we come up [Koomley's law](https://en.wikipedia.org/wiki/Koomey%27s_law) with performance per watt doubling every 18 months.

By the mid 2000's, we started running into physical limits.  In 2012 Koomley re-examined the data and found that the doubling had slowed since 2000.  Around that time, chipmakers started getting around these limits in a different way - instead of making chips faster, they started adding more of them.  This is widely known as multi-core computing.

The challenge with multi-core computing is similar to the expression, "too many cooks in the kitchen".  You need to coordinate between each core, and the coordination can be the thing that sucks up a lot of the time.  Further more, many tasks can't be sped up by running them parallel.  To illustrate this point I ask the question - If a women can make a baby in 9 months, why can't 2 women make a baby in 4 1/2 months? 

Fortunately by this time our computers were running multiple applications at the same time.  So if we have 2 cores, we can just run 2 applications doing different things and get the use out of the cores.  But there is a limit to this - how many applications do we really need at the same time? 

The other problem is that when you have a single task to do, running different applications 

This coordination is generally done in software and hence why we must go back to programming languages.

### Current status quo

