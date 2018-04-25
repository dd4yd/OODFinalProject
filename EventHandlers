# Listeners and Event Handlers

## Java
* EventHandlers and Listeners are added to Objects to determine a state change or interaction with the object
* ```Java
ChangeListener<Number> lambdaChangeListener = (ObservableValue<? extends Number> observable, Number oldValue, final Number newValue) -> {
      refresh();
  };

  this.stage.widthProperty().addListener(lambdaChangeListener);
  ```

## Swift
* Event handlers and Listeners are used for the same purpose in Swift
* class Cat {
  *    let events = EventManager();
  *    func meow() {
      *        println("Cat: MRaawwweeee");
      *        self.events.trigger("meow", information: "The cat is hungry!");
  * }
* }
* class Human {
  * func adoptCat(cat:Cat) {
    * cat.events.listenTo("meow", action: self.dayDream);
  * }
  * func dayDream() {
    * println("Human daydreams about owning a dog");
  * }
* }
