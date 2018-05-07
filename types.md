# Types

## Java
1. What types does the language support?
  * Primitive Data Types
    * boolean: True or false, 1 bit
    * byte: Twos complement integer, 8 bits
    * char: Unicode character, 16 bits
    * short: Twos complement integer, 16 bits
    * int: Twos complement integer, 32 bits
    * long: Twos complement integer, 64 bits
    * float: IEEE 754 floating point, 32 bits
    * double IEEE 754 floating point, 64 bits
  * Object/Reference Types
    * Programmer created Types
2. Are both reference and value types supported?
  * Technically Java only supports call by value, but there are references to
  objects
  * There are references to objects in Java, but when that reference is used as
  parameter in a method, a copy of the reference is made. Therefore, Java only
  supports call by value
3. Can new value types be created?
  * New value types cannot be created

## Swift
1. What types does the language support?
  * Primitive Data Types
    * Int or UInt
    * Float
    * Double
    * Bool
    * String
    * Character
    * Optional
    * Tuples
  * Reference Types
    * Classes
    * Functions
2. Are both reference and value types supported?
  * Yes. Class instances and functions are reference types. Anything else is
  value type. This includes structs and enums
3. Can new value types be created?
  * If creating a struct or an enum is considered creating a new value type, then
  yes, value types can be created.
