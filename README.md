# Robotmaster.CollectionRecommendation

A set of code analyzers that determines the proper .NET Collection to use in the context.

Determining precisely how to pick a collection or which API to use is hard task for a software developer. It makes all the different between an application feature that executes within 1 second and 1 minute. This is one of the core fundamentals of computer science and software engineering. Even when the portion of the software you're maintaining/updating isn't performance specific, selecting the correct data structure(s) for your context will provide huge benefits.

In .NET, most collections automatically expand in capacity when the current capacity is reached. The memory is reallocated, and the elements are copied from the old collection to the new one. This reduces the code required to use the collection; however, the performance of the collection might be negatively affected. For example, for List<T>, If Count is less than Capacity, adding an item is an O(1) operation. If the capacity needs to be increased to accommodate the new element, adding an item becomes an O(n) operation, where n is Count. The best way to avoid poor performance caused by multiple reallocations is to set the initial capacity to be the estimated size of the collection.
