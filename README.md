<h1>TypescriptMeta</h1>
<h2>A typescript library to add classes with annotated functions</h2>
<hr>
<br>
<br>
<h3>Create an annotation for class methods</h3>
<ol>
<li>Derive a class from Meta.Annotation<li>
<li>Override the execute method to manipulate the annotated instance/class (instance variables should be created with lazy getters)</li>
<br>
<pre>
module MyModule {
    MyAnnotation extends Meta.Annotation {
       static execute(info:AnnotationInfo):void {
                    // ... modify instance with the info
}}}
</pre>
