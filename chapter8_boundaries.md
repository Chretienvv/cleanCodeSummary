# Clean code chapter 8 Boundaries

## Tips & Learnings
- Using third party code
    - How much acces does the code have? 
    - A nice example is the following:

```
// Using generics is an improvement
Map<Sensor> sensors = new HashMap<sensor>();
Sensor s = sensors.get(sensordId);

// Even better because the getByID doesnt know the HasHmap
public class Sensors{
    private Map sensors = new Hashmap()
    public Sensor getById(STring id){
        return (sensor) sensors.get(id)
    }
}

```

- Do not pass maps, interfactes around in your system
    - Keep it in a class 
- Exploring and learning boundaries
    - Write some tests and explore the third party code in a test project instead on production.
    - These are called learning tests
- Using code that does not yet exist
    - Code created because you wished you had it can be usefull for detecting and setting boundaries. 
    - The change needed when the real code is available will be smaller
- We manage boundaries by referring to third party code as least as possible.

## Own Opinion
I think this concept is intersting. This can combined very nicely with testing and the use of fake services.  In general this is an advanced concept in my opnion because it requires domain knowledge, experience and an high abstract level of conceptualizing. 

