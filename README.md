About ant-yui-compressor
==================

Version 1.0

ant-yui-compressor is an ant task for compressing multiple JavaScript and CSS files using [YUI compressor](http://developer.yahoo.com/yui/compressor/). It is based on earlier work by Simon Buckle (https://code.google.com/p/yui-compressor-ant-task/) and adds some extra features:
* Support for CSS minification
* Option to automatically delete original source files after generating minified files

### Usage
```
<ant-yui-compressor todir="js" deleteOriginal="true">
	<fileset dir="js">
    	<include name="config.js" />
		<include name="model.js" />
		<include name="main.js" />
	</fileset>
	<mapper type="glob" from="*.js" to="*-min.js"/>
</ant-yui-compressor>
```
Note: Both fileset and mapper elements are required.