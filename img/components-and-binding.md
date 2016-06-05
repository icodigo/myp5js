### General notes on concepts we need to understand
__Decorators__
> An expression that evaluates to a function allowing annotation
of classes at design time. Hum.
 
__@Component()__ is a decorator.
>It tells a Angular that you intend a class to be used as a component.

To use a Decorator such as @Componet() on a class, you need to import it
using ES2015 module loading sytax: import { Component } from ' ';

Importing mutiple modules can be separated by commas; the module can be bare module name
or a relative path to a file/module, as a string.

```
import { Component } from '@angular/core';
```

The @Component decorator comes from a module bundle
found in @angular/core, and this will be inside node_modues.

__Class definition for component__
```
export class AppComponent { }
```

The export syntax is what will allow this class to be loaded by another script file to 
bootstrap it or start up the application.

The @Component decorator takes in an `{ }` object with some known properties 
to configure the class you __decorate__ as an angular component, and these
as known as __metadata__. Two of these properties are required:
1. selector
2. template, or templateUrl

__Binding__

Square `[ ]` brackets used for property binding, and for event 
binding we use `( )` parentheses. 

Create a function avaiable in the component class that is called
from a `(click)` event inside an anchor element:

Event:

```
<a (click)="onDelete()"> Remove Me </a>
```

Function in component class:

```
export class AppComponent {
    onDelete() {
        console.log('I am deleted.');
        }
    }
```

