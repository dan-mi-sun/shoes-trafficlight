TrafficLight
============

A traffic light application to drive home some Ruby OOP principles.

# INSTALL

1. Get a copy of Shoes running, resources online at:

> https://github.com/shoes/shoes/wiki/Building-Shoes

> http://shoesrb.com/manual/Installing.html

I had to add the following line to my ~/.bashrc to get this running on OSX:

```
PATH=/Applications/Shoes.app/Contents/MacOS:$PATH
```

2. Fork your own copy of this exercise and clone it

```
  git clone https://github.com/dmgarland/TrafficLight.git
  cd TrafficLight
```

3. Run it!
```
    shoes traffic.rb
```

# TODO

We'll be modifying a Shoes application that models a traffic light.

* Using inheritance, implement 3 subclasses of Bulb: GoBulb, WaitBulb and
StopBulb. Change the subclasses so that when we define them, the correct colour
is displayed. Suggest that the following colours are used:

|State|Colour|
|:----------|:-----------|
|Go  | "#00FF30" |
|Wait| "#FFFC00" |
|Stop| "#FF0000" |

* Refactor the implementation so that the colours are defined once in a module
called TL, and we can refer to colours with the following syntax:

|State|Colour|
|:----------|:-----------|
|TL::Go  | "#00FF30" |
|TL::Wait| "#FFFC00" |
|TL::Stop| "#FF0000" |

* Refactor the implementation so that a bulb only shows its true colour when it
is switched on, otherwise it shows grey. Fix the application so that it shows
the TL::Stop state on startup.
* Implement the click method, so that every time the traffic light is clicked,
the colours cycle through the states given in the TrafficLight class
* Animate the traffic light so that it cycles through its colours automatically, changing once a second. Use either an animate block (see the manual) to pull out each entry in turn or try Thead.new and sleep.
* When you're done, submit a pull request so that I can review your work.
* Don't forget that you can use the debug method to show output to the shoes console.
