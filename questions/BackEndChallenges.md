# Back-end Code Challenges
* Only send back the code require for your the challenges

## Task 1
Write a method that will take, as input, a string and dependent on the string length prints out the following:
1. If the length is a multiple of 2 your method must print out "Stack"
2. If the length is a multiple of 4 your method must print out "Overflow"
3. If the length is a multiple of 2 and 4 your method must print out "Stack Overflow!"
## Task 2

You are probably familiar with social media "like" systems. People can like posts and the UI displays who likes certain posts.
Write a method that takes in a list of names and produces the format below:

```csharp
Likes(new List<string>()) => "no one likes this"
Likes(new List<string> {"Peter"}) => "Peter likes this"
Likes(new List<string> {"Jacob", "Alex"}) => "Jacob and Alex like this"
Likes(new List<string> {"Max", "John", "Mark"}) => "Max, John and Mark like this"
Likes(new List<string> {"Alex", "Jacob", "Mark", "Max"}) => "Alex, Jacob and 2 others like this"
```

__Note__: if the amount of people who like something is 4 or more, print out the first 2 names following by how many others like it.

## Task 3
The last task is about refactoring of code. Below you are given a class that creates robots and cars, this class uses a robot service, a part service, and a car service, which can be any web services (RESTful or SOAP).

You need to refactor this class as you see fit. The goal is to make the class more maintainable. You should apply any principles or patterns you think are necessary.

Don't write out the web service classes. Assume they have an implementation and you are just consuming them.

* Bonus: what can be done to reduce tight coupling in a class?

```csharp
public class Factory
{
    private RobotService _robotService;
    private PartsService _partsService;
    private CarService _carService;
    
    public Factory(RobotService robotService, PartsService partsService)
    {
        _robotService = new RobotService();
        _partsService = new PartsService();
        _carService = new CarService();
    }

    public Robot BuildRobot(Enum RobotType)
    {
    if(RobotType == RoboticDog)
        var parts = GetRobotPartsFor(RoboticDog);
        return _robotService.BuildRobotDog(parts);
    else if(RobotType == RoboticCat)
        var parts = GetRobotPartsFor(RoboticCat);
        return _robotService.BuildRobotCat(parts);
    else if(RobotType == RoboticDrone)
        var parts = GetRobotPartsFor(RoboticDrone);
        return _robotService.BuildRobotDrone(parts);
    else if (RobotType == RoboticCar)
        var parts = GetRobotPartsFor(RoboticCar);
        return _robotService.BuildRobotCar(parts);
    else
        return null;
    }

    public Car BuildCar(Enum CarType)
    {
        if(CarType == Toyota)
            var parts = GetCarPartsFor(Toyota);
            return _carService.BuildCar(parts);
        else if(RobotType == Ford)
            var parts = GetCarPartsFor(Ford);
            return _carService.BuildCar(parts);
        else if(RobotType == Opel)
            var parts = GetCarPartsFor(Opel);
            return _carService.BuildCar(parts);
        else if (RobotType == Honda)
            var parts = GetCarPartsFor(Honda);
            return _carService.BuildCar(parts);
        else
            return null;
    }

    public List<Parts> GetRobotPartsFor(Enum RobotType)
    {
        return _partsService.GetParts(RobotType);
    }

    public List<Parts> GetCarPartsFor(Enum CarType)
    {
        return _partsService.GetParts(CarType);
    }
}
```