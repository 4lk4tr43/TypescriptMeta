TypescriptMeta
## this library is included in TypescriptRouting
=================

A typescript library to add classes with annotated functions
<hr>


<h3>Create an annotation for class methods</h3>
<ol>
<li>Derive a class from Meta.Annotation</li>
<li>Override the execute method to manipulate the annotated instance/class (instance variables should be created with lazy getters)</li>
</ol>

<pre>
module MyModule {
    MyAnnotation extends Meta.Annotation {
       static execute(info:AnnotationInfo):void {
                    // ... modify instance with the info
        }
    }
}
</pre>

<h3>Usage</h3>
<ol>
<li>Create a class derived from Meta.Annotated</li>
<li>Insert an annotation to the annotation class, must be single quotes</li>
</ol>

<pre>
module MyApp {
    MyClass extends Meta.Annotated {
       a():void {
                   'MyModule.MyAnnotation';
                   // arguments to an annotation are passed as json string
                   // -> 'MyModule.MyAnnotation={"recursive":true}';
        }
    }
}
</pre>
<hr>
<b>More information can be found in the file comments.</b>
<hr>
Collaborators are always welcome!
