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

The second section simulates an information center for an arbitrary pet hotel or animal shelter. The program creates animal classes with distinct descriptions for each species of cost of boarding, sound they make, how they eat, favorite trick, and how they go to sleep. The example then takes individual animals as data points along with each idividual animal's name, species, and age. The method then outputs all of the information on each animal in the shelter. This is the example output for a dog, a cat, and a parrot:


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
