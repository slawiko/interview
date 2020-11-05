# Angular

## Modules

1. What is `declarations`? - **things you want to use in templates (components, pipes, etc.)**

1. What is `providers`? - **services. _Note: since Angular 6 you do not need this_**

1. What is the scope of `declarations` and `providers`? - **`declarations` are local, `providers` are global**

1. Why some modules are needed to be imported once, and some many times? - **because of scope difference, see above**

1. Imagine the hierarchical application with modules imported on different levels. How these modules will be placed? (flat or hierarchicaly) - **flat**

  1. And what about lazy loaded modules? - **Lazy loaded modules DO create hierarchy, BUT it’s the hierarchy of injectors, not modules. All imported modules are still merged into one factory during compilation just the same as with non-lazy modules**

1. What to do if you want to create module with services and components? How to import such module? - **`.forRoot()` and `.forChild()`**

1. When writing `.forRoot()` and `.forChild()` static methods are also needed? - **when you want to write a module which is going to imported into both eager and lazy modules**

1. What is `entryComponents`? - **components that are not referenced in template**

1. When you write root module, you should put root component in `bootstrap`. But is it an entry component? - **`bootstrap` array is automatically added in `entryComponents` by compiler**

1. When you write routing, should you put routing components in `entryComponents` array? - **no, routing components are automatically added in `entryComponents` array by compiler**

1. Why `entryComponents` is no longer needed after Angular 9? - **because previously compiler did analyze of application based on NgModule configurations. Ivy does compilation of decorator level. (does it mean that each component in fact is an entryComponent?)**

-----------

#### Sources

* https://medium.com/@cyrilletuzi/understanding-angular-modules-ngmodule-and-their-scopes-81e4ed6f7407
* https://stackoverflow.com/questions/61541876/why-entrycomponents-is-not-necessary-anymore-in-angular-9-ivy-compiler
* https://indepth.dev/avoiding-common-confusions-with-modules-in-angular/
* https://angular.io/guide/entry-components

