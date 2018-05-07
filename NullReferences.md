## Null/ Nil References

### Java

Ultimately, the main way to catch a null reference in java is to implement a try {} catch() {} block that throws a NullPointerException. In java, the keyword 'null' is used to check and set null objects.

### Swift 

In swift, you aren't given the option to catch null pointer excpetions. Swift developers do this because a null pointer indicates the system is in a unrecoverable state, of which the developer has to debug and fix. Swift uses the 'nil' keyword rather than null in Java