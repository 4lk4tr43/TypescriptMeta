<h2 style="font-weight: normal; line-height: 1.2; color: rgb(51, 51, 51); font-family: sans-serif, Arial, Verdana, 'Trebuchet MS'; font-style: italic;">
	<strong>TypescriptMeta</strong></h2>
<h3 style="font-weight: normal; line-height: 1.2; font-family: sans-serif, Arial, Verdana, 'Trebuchet MS'; color: rgb(170, 170, 170); font-style: italic;">
	A typescript library to add classes with annotated functions</h3>
<hr style="border-right-width: 0px; border-bottom-width: 0px; border-left-width: 0px; border-top-style: solid; border-top-color: rgb(204, 204, 204); color: rgb(51, 51, 51); font-family: sans-serif, Arial, Verdana, 'Trebuchet MS'; font-size: 13px; line-height: 20.7999992370605px;" />
<p style="color: rgb(51, 51, 51); font-family: sans-serif, Arial, Verdana, 'Trebuchet MS'; font-size: 13px; line-height: 20.7999992370605px;">&nbsp;</p>
<h3 style="font-weight: normal; line-height: 1.2; color: rgb(51, 51, 51); font-family: sans-serif, Arial, Verdana, 'Trebuchet MS';">
	<strong>Create an annotation for class methods:</strong></h3>
<ol style="padding: 0px 40px; color: rgb(51, 51, 51); font-family: sans-serif, Arial, Verdana, 'Trebuchet MS'; font-size: 13px; line-height: 20.7999992370605px;">
<li>Derive a class from Meta.Annotation</li>
<li>Override the execute method to manipulate the annotated instance/class (instance variables should be created with lazy getters)</li>
</ol>
<p style="color: rgb(51, 51, 51); font-family: sans-serif, Arial, Verdana, 'Trebuchet MS'; font-size: 13px; line-height: 20.7999992370605px;">&nbsp;</p>
<ul style="padding: 0px 40px; color: rgb(51, 51, 51); font-family: sans-serif, Arial, Verdana, 'Trebuchet MS'; font-size: 13px; line-height: 20.7999992370605px;">
<li><code>module MyModule {</code></li>
<li><code>&nbsp; &nbsp; MyAnnotation extends Meta.Annotation {</code></li>
<li><code>&nbsp; &nbsp; &nbsp; &nbsp;static execute<span style="font-family: Consolas, 'Liberation Mono', Menlo, Courier, monospace; font-size: 12px; line-height: 16.7999992370605px; white-space: pre;">(</span><span class="pl-vpf" style="box-sizing: border-box; font-family: Consolas, 'Liberation Mono', Menlo, Courier, monospace; font-size: 12px; line-height: 16.7999992370605px; white-space: pre;">info</span><span style="font-family: Consolas, 'Liberation Mono', Menlo, Courier, monospace; font-size: 12px; line-height: 16.7999992370605px; white-space: pre;">:AnnotationInfo):void {</span></code></li>
<li><code>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; // ... modify instance with the info</code></li>
<li><code><span style="font-family: Consolas, 'Liberation Mono', Menlo, Courier, monospace; font-size: 12px; line-height: 16.7999992370605px; white-space: pre;">}}}</span></code></li>
</ul>
<p style="color: rgb(51, 51, 51); font-family: sans-serif, Arial, Verdana, 'Trebuchet MS'; font-size: 13px; line-height: 20.7999992370605px;">&nbsp;</p>
<h3 style="font-weight: normal; line-height: 1.2; color: rgb(51, 51, 51); font-family: sans-serif, Arial, Verdana, 'Trebuchet MS';">
	<strong>Usage:</strong></h3>
<ol style="padding: 0px 40px; color: rgb(51, 51, 51); font-family: sans-serif, Arial, Verdana, 'Trebuchet MS'; font-size: 13px; line-height: 20.7999992370605px;">
<li>Create a class derived from Meta.Annotated</li>
<li>Insert an annotation to the annotation class, must be single quotes</li>
</ol>
<p style="color: rgb(51, 51, 51); font-family: sans-serif, Arial, Verdana, 'Trebuchet MS'; font-size: 13px; line-height: 20.7999992370605px;">&nbsp;</p>
<ul style="padding: 0px 40px; color: rgb(51, 51, 51); font-family: sans-serif, Arial, Verdana, 'Trebuchet MS'; font-size: 13px; line-height: 20.7999992370605px;">
<li style="line-height: 20.7999992370605px;"><code>module MyApp {</code></li>
<li style="line-height: 20.7999992370605px;"><code>&nbsp; &nbsp; MyClass&nbsp;extends Meta.Annotated {</code></li>
<li style="line-height: 20.7999992370605px;"><code>&nbsp; &nbsp; &nbsp; &nbsp;a()<span style="font-family: Consolas, 'Liberation Mono', Menlo, Courier, monospace; font-size: 12px; line-height: 16.7999992370605px; white-space: pre;">:void {</span></code></li>
<li style="line-height: 20.7999992370605px;"><code>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&#39;MyModule.MyAnnotation&#39;;</code></li>
<li style="line-height: 20.7999992370605px;"><code>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;// arguments to an annotation are passed as json string</code></li>
<li style="line-height: 20.7999992370605px;"><code>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;// -&gt;&nbsp;<span style="line-height: 20.7999992370605px;">&#39;MyModule.MyAnnotation={&quot;recursive&quot;:true}&#39;;</span></code></li>
<li style="line-height: 20.7999992370605px;"><code><span style="font-family: Consolas, 'Liberation Mono', Menlo, Courier, monospace; font-size: 12px; line-height: 16.7999992370605px; white-space: pre;">}</span><span style="font-size:12px;"><span style="line-height: 20.7999992370605px;">}}</span></span></code></li>
</ul>
<p style="color: rgb(51, 51, 51); font-family: sans-serif, Arial, Verdana, 'Trebuchet MS'; font-size: 13px; line-height: 20.7999992370605px;">&nbsp;</p>
<p style="color: rgb(51, 51, 51); font-family: sans-serif, Arial, Verdana, 'Trebuchet MS'; font-size: 13px; line-height: 20.7999992370605px;"><strong>More information can be found in the file comments.</strong></p>
