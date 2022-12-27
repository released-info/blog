---
layout: post
title: Objective Pascal
---
<div class="row">
    <div class="col-sm-2">
        <img src="/images/objective-pascal-logo.png" alt="objective pascal logo"/>
    </div>
    <div class="col-sm-10">
        Objective Pascal is a programming language created by Apple Inc. It was first released in 2002 as part of Mac OS X and later ported to iOS in 2008. It is a combination of the classic Object Pascal language found in Borland Delphi, with added features from C++ and Objective-C. This programming language combines the best features of both languages and provides a great deal of flexibility and power for developers. With this language, you can create cross-platform applications, games, and more.
        Object Pascal was developed by Apple in 2002 as part of their Mac OS X operating system. It was designed to replace their original programming language, Object Pascal, and incorporate C++ and Objective-C features. Objective Pascal was officially released in 2003 and included with Mac OS X 10.2.
        In 2008, Apple released iOS, a mobile operating system based on the same codebase as Mac OS X. This opened the doors for developers to create native apps that ran on Apple’s mobile devices. Objective Pascal was updated and included with the new iOS SDK.
    </div>
</div>


## Introduction
Objective Pascal is an object-oriented language with a syntax similar to that of Object Pascal, which is also known as Delphi or Turbo Pascal. Object Pascal was originally developed by Niklaus Wirth in the 1970s and later expanded upon by Borland Software Corporation in the 1980s. Object Pascal has since been adopted by Apple Inc. and Borland Software Corporation as the primary development language for their desktop and mobile platforms, respectively.
Objective Pascal is a strongly-typed, object-oriented programming language that supports multiple paradigms such as procedural and functional programming paradigms. It is source code compatible with the earlier Pascal language, which makes migrating existing code easy. It also boasts many modern features such as garbage collection, generics, closures, iteration statements, and type inference.
Objective Pascal is known for being easy to learn and use, and its syntax is relatively simple compared to other object-oriented programming languages. This makes it well suited for students who are just starting to learn programming. It is also suitable for experienced developers who need to create fast and reliable applications quickly.
Objective Pascal can be used to develop a wide variety of applications, such as web-based applications, mobile apps, desktop applications, and games. It integrates seamlessly with the Cocoa frameworks on OS X and iOS, making it easy to develop apps for those platforms. 

## History 

Objective Pascal is a dialect of the Pascal programming language developed in the early 1990s. It is an object-oriented version of the language, and includes concepts such as classes, objects, and inheritance. The language was developed by Apple Computer to support their Macintosh operating system, and was initially referred to as "MacApp".
Objective Pascal is similar to the popular C++ programming language, although it is not compatible with it. It was based on the popular Clascal (Class Pascal) system, which was created by Portland Software in the mid-1980s. This system was later modified by Apple to become Objective Pascal.
Objective Pascal is designed to facilitate the development of software for the Mac OS operating system. The language supports multiprocessing, making it ideal for high-end applications and scientific programming. It also has support for event handling, which allows for the program to interact with the user, making it suitable for GUI-based applications.
Objective Pascal is based on the same syntax as traditional Pascal, and the code looks very similar. However, there are several features that help separate it from traditional Pascal. These include:

* Object-Oriented Programming. By using Object-Oriented Programming, developers can more easily create components that can be reused in a variety of programs.
* Classes and Inheritance. Classes are groups of related properties and methods that can be used to encapsulate functionality within a program. This allows for easy reuse of code in multiple programs. In addition, inheritance allows for the reuse of code from other classes that share the same properties and methods.
* Memory Management. In addition to classes and inheritance, Objective Pascal features a sophisticated memory management system. This allows for the efficient use of computer resources and helps to prevent memory leaks.
* Threading. Threading allows for multiple tasks to be executed simultaneously, making it ideal for programs that require heavy multitasking.
* Exception Handling. The exception handling feature allows developers to catch errors in their program and respond accordingly.
* GUI Support. Objective Pascal is well-suited for creating graphical user interfaces, due to its support for the AppKit framework.
  Objective Pascal is still used today in a variety of applications, most notably as the language behind the Cocoa framework used in macOS and iOS. The language is also used in many popular third-party applications, such as Microsoft Office for Mac.

### Features of Objective Pascal
Objective Pascal is a strongly typed, object-oriented language. It supports multiple paradigms including procedural, functional, and object-oriented. It also has built-in garbage collection and generics support. 

Objective Pascal is source code compatible with the original Pascal language, which makes it easy to migrate existing code. It also has many modern features such as the ability to define custom data types, iterative statements, and type inference.

It integrates seamlessly with the Cocoa frameworks on OS X and iOS, making it easy to develop apps for those platforms. It also has bindings for popular third-party software libraries such as OpenGL, GTK+, and Qt, making it easy to develop cross-platform applications.

### Uses of Objective Pascal
Objective Pascal can be used to develop a wide range of applications, from web-based applications to mobile apps and desktop software. It is well suited for projects that require high performance and reliability. 

Objective Pascal is often used for developing native applications for the Mac OS X and iOS platforms. It is also commonly used for developing cross-platform applications due to its integration with popular third-party software libraries.

### Code Examples
The following is a basic "Hello World" program written in Objective Pascal:
```objectpascal
program HelloWorld;

begin
    writeln('Hello world!');
end.
```
The following is an example of a function written in Objective Pascal:
```objectpascal
function factorial(x: integer): integer;
var
    result: integer;
begin
    if x <= 1 then 
        result := 1
    else 
        result := x * factorial(x - 1);
    factorial := result;
end;
```
And finally, here is an example of an object-oriented class written in Objective Pascal:
```objectpascal
type
    TMyClass = class
    private
        FData: string;
    public
        property Data: string read FData write FData;
        function DoSomething: string;
    end;

implementation

function TMyClass.DoSomething: string;
begin
    Result := FData;
end;
```

### Example Usage 

The following example shows how to use Objective Pascal to create a simple application that prints "Hello World" to the screen:

```objective-c
#import <Foundation/Foundation.h>
@interface AppDelegate : NSObject <NSApplicationDelegate>
- (void)applicationDidFinishLaunching:(NSNotification *)aNotification;
@end
@implementation AppDelegate
- (void)applicationDidFinishLaunching:(NSNotification *)aNotification {
    NSLog(@"Hello World!");
}
@end
int main(int argc, const char * argv[]) {
    @autoreleasepool {
        NSApplication * application = [NSApplication sharedApplication];
        AppDelegate * delegate = [[AppDelegate alloc] init];
        [application setDelegate:delegate];
        [application run];
    }
    return 0;
}
```

In this example, we first import the Foundation library and create an AppDelegate class. We then implement the applicationDidFinishLaunching method, which prints the “Hello World” message to the console. Finally, we create an NSApplication object and initialize the AppDelegate as its delegate. The application is then run, causing the “Hello World” message to be printed.

The following example shows how to create a simple class in Objective Pascal:

```objective-pascal
type 
  TMyObject = class(TObject)
  private
    FName: String;
  public
    constructor Create(const AName: String); 
    property Name: String read FName write FName; 
  end;

constructor TMyObject.Create(const AName: String); 
begin 
  inherited Create;
  FName := AName;
end;  
```

In this example, we create a class called TMyObject. The class has a single field called FName, which holds the name of the object. We then implement a constructor, which takes an AName parameter and sets the FName field to the value of AName. 

The following example demonstrates how to use this class to create an object:

```objective-pascal
var 
  Obj: TMyObject; 
begin 
  Obj := TMyObject.Create('Test');
  Writeln(Obj.Name); // Prints "Test"
end; 
```

In this example, we create an instance of TMyObject, passing in the string "Test" as an argument to the constructor. We then print out the value of the Name field, which will be "Test".

Let's look at a simple example of Objective Pascal code.

```objective-c
class MyClass {
  int _num;
  public int Num {
    get { return num; }
    set { num = value; }
  }
}
```

This code defines a class called MyClass which has a property called Num. The property is of type int and can be accessed and set using the get and set keywords.

Now let's look at a more complex example.

```objective-c
class StorageSystem {
  private Dictionary<string, object> _data;

  public object GetValue(string key) { return this._data[key]; }
  public void SetValue(string key, object value) { _data[key] = value; }
}
```

This code creates a class called StorageSystem which contains a Dictionary of key-value pairs. It has two methods, GetValue and SetValue, which allow you to get and set the values in the dictionary.

```
// Hello World program written in Objective Pascal
class HelloWorld
{
  private
    message: string;
  public
    constructor()
    begin
      message := 'Hello World!';
    end;
 
    procedure showMessage()
    begin
      Writeln(message);
    end;
}

begin
  var message := new HelloWorld();
  message.showMessage();
end.
```

The above code creates a class called HelloWorld with one member variable (message) and one method (showMessage). The method showMessage prints the message variable to the screen. The program then creates an instance of the class and calls the showMessage method to print out “Hello World!”.

## Conclusion

Objective Pascal is a powerful programming language that is used for a variety of software projects. It has support for multiple inheritance, generics, and multithreading, making it an ideal choice for developing large, complex software applications. With its deep roots in the Pascal programming language, Objective Pascal is easy to learn and use for both experienced and novice developers.
