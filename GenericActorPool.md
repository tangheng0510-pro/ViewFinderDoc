1.Enable Plugin

<img width="1015" height="127" alt="image" src="https://github.com/user-attachments/assets/f5ab3581-0b52-40ea-ac35-b2b354b6c3f2" />

2.GenericActorPoolComponent

<img width="334" height="251" alt="image" src="https://github.com/user-attachments/assets/88c59982-5800-49ef-b581-0931af6d27ba" />


Initialize:

<img width="1093" height="455" alt="image" src="https://github.com/user-attachments/assets/8eead14e-f6ff-4480-beb8-272ae446332f" />

InCreateActorDelegate:Pass in a custom function to create an Actor.

InOnActorGetFromPoolDelegate:Executed when obtaining an Actor from the object pool, it is generally used to reset the Actor's state.

InOnActorReturnToPoolDelegate:Executed when the Actor is reclaimed into the object pool, for example, to cancel the timer.

Get Actor From Pool:

<img width="780" height="338" alt="image" src="https://github.com/user-attachments/assets/ddf2ca6d-4ed6-431f-b1c1-f35fe41671df" />

Payload:It is a FInstancedStruct, you can pass any structure through it.

Recycle Actor:

<img width="415" height="248" alt="image" src="https://github.com/user-attachments/assets/18874e4b-7188-4e83-a268-a88a064c6057" />

3.GenericActorPoolObject

If you don't want to use GenericActorPoolComponent, you can use the GenericActorPoolObject to build your own system.
