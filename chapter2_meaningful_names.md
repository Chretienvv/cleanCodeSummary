# Clean code chapter 2 meaningful names

## Tips & Learnings
- Intention revealing Names
    - What does it do?
    - What do you get?
- Avoid disinformation
- Make meaningfull distinctions a.i. variable names mean something different so do not use films1 and films2.
- Use pronounceable names
- use searchable names
- Avoid endocings deciphering usually adds an extra burden.
- Dont specify the type in names because it creates confusion.
- Class names and object names
    -  should have nouns or noun phrase names. Customer, Account
    - should not be a verb -> Manager, processor, data
- methods should use verbs like get, post, delete
- Pick one word per concept: delete stays delete and not remove.
    - It needs to be semantic. For instance add and insert are two different things.
- Use Solution domain names such as pattern names.
- Use problem domain names so the developer can ask a domain expert. e.a. gtscharge.
- Don't add gratuitous context such as accountAdress vs GTSaccountAdress

## Own Opinion
I agree with most of these points except one. The abbrviations part. It could be very usefull to create "costs" and "gtsCosts". If it is for a small scope. On a bigger scope a class of object may be better. 
Same with interfaces and encodings. It could be usefull to set the keys and values.