# Animal-descriptions
This repository consists of two different programs with similar goals of creating classes to log and present information about animals.


## Part 1: Zoo information kiosk


The first section simulates an information kiosk at a zoo. The program creates animal classes (as shown below) that store the sound an animal makes and an interesting fact or statement about the animal. 


```java

class Animal {
    int age;
    String name;

    public Animal() {
        age = 0;
        name = "";
    }

    public void makeSound() {
        System.out.println("Animal makes a sound");
    }

    public void getDescription() {
        System.out.println("This is a generic animal");
    }
}
// create the Lion class that extends Animal
class Lion extends Animal {
    public Lion(int i, String x) {
        age = i;
        name = x;
    }

    @Override
    public void makeSound() {
        System.out.println("Roar!");
    }

    @Override
    public void getDescription() {
        System.out.println("The lion is the king of the jungle");
    }
}
// create the Elephant class that extends Animal
class Elephant extends Animal {
    public Elephant(int j, String y) {
        age = j;
        name = y;
    }

    @Override
    public void makeSound() {
        System.out.println("Trumpet!");
    }

    @Override
    public void getDescription() {
        System.out.println("Elephants are the largest land animals");
    }
}

// create the Parrot class that extends Animal
class Parrot extends Animal {
    public Parrot(int k, String z) {
        age = k;
        name = z;
    }

    @Override
    public void makeSound() {
        System.out.println("Squawk!");
    }

    @Override
    public void getDescription() {
        System.out.println("Parrots can mimic human speech");
    }
}
```

The example creates objects from these classes and then outputs the individual animals' name, age, sound they make, and fact about them, as if it were on a display at a zoo. This is the example output for a lion, parrot, and elephant:


Name: Leo, Age: 5

Roar!

The lion is the king of the jungle
    
Name: Ellie, Age: 8

Trumpet!

Elephants are the largest land animals
    	
Name: Polly, Age: 2

Squawk!

Parrots can mimic human speech


## Part 2: Animal Shelter

The second section simulates an information center for an arbitrary pet hotel or animal shelter. The program creates animal classes, as shown in the code below, with distinct descriptions for each species' cost of boarding, sound they make, how they eat, favorite trick, and how they go to sleep. 
```java
interface Pet {
    void sound();
    void food();
    int board();
}

interface Train {
    void trick();
}

abstract class Animal implements Pet {
    int age;
    String name;

    Animal() {
    }

    int getAge() {
        return age;
    }

    String getName() {
        return name;
    }

    public void sleep() {
        System.out.println(name + " goes to sleep.");
    }

    abstract void special();
}
class Dog extends Animal implements Train {
    Dog(int x, String a) {
        age = x;
        name = a;
    }

    public void sound() {
        System.out.println(name + " barks loudly!");
    }

    public void food() {
        System.out.println(name + " eats kibble happily.");
    }

    public int board() {
        return 30;
    }

    public void trick() {
        System.out.println(name + " performs a trained trick and rolls over");
    }

    void special() {
        System.out.println(name + " fetches a toy");
    }
}
class Cat extends Animal {
    Cat(int x, String a) {
        age = x;
        name = a;
    }

    public void sound() {
        System.out.println(name + " meows softly");
    }
    public void food() {
        System.out.println(name + " eats kibble with elegance");
    }
    public int board() {
        return 25;
    }
    void special() {
        System.out.println(name + " engages in her special behavior and scratches the post");
    }

    public void sleep() {
        System.out.println(name + " curls up and goes to sleep");
    }
}
class Parrot extends Animal {
    Parrot(int x, String a) {
        age = x;
        name = a;
    }

    public void sound() {
        System.out.println(name + " squawks brightly");
    }

    public void food() {
        System.out.println(name + " pecks at the kibble");
    }

    public int board() {
        return 20;
    }

    void special() {
        System.out.println(name + " performs her special behavior: mimics a phrase");
    }

    public void sleep() {
        System.out.println(name + " tucks her head and goes to sleep");
    }
}
```

The example then takes individual animals as data points along with each idividual animal's name, species, and age. The method then outputs all of the information on each animal in the shelter. This is the example output for a dog, a cat, and a parrot:


Dog (Buddy, Age 3)

Buddy barks loudly!

Buddy eats kibble happily.

Buddy performs a trained trick and rolls over

Buddy fetches a toy

Buddy goes to sleep.


Cat (Misty, Age 2)

Misty meows softly

Misty eats kibble with elegance

Misty engages in her special behavior and scratches the post

Misty curls up and goes to sleep


Parrot (Polly, Age 5)

Polly squawks brightly

Polly pecks at the kibble

Polly performs her special behavior: mimics a phrase

Polly tucks her head and goes to sleep


--- Boarding Cost Summary ---

Buddy daily cost: $30

Misty daily cost: $25

Polly daily cost: $20

Total Daily Boarding Cost: $75.0

--- End of Day Report ---
