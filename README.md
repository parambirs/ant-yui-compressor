About ant-yui-compressor
==================

ant-yui-compressor is an ant task for compressing multiple JavaScript and CSS files using [YUI compressor](http://developer.yahoo.com/yui/compressor/). It is based on earlier work by Simon Buckle (https://code.google.com/p/yui-compressor-ant-task/) and adds some extra features:
* Support for CSS minification
* Option to automatically delete original source files after generating minified files

### Basic Usage
```xml
<ant-yui-compressor todir="js">
	<fileset dir="js">
		<include name="backbone.js" />
		<include name="jquery.js" />
	</fileset>
	<mapper type="glob" from="*.js" to="*-min.js"/>
</ant-yui-compressor>
```
Note: The 'toDir' attribute, as well as <fileset> & <mapper> elements are required.

### Example

A working ant sample project is available with the source code (https://github.com/parambirs/ant-yui-compressor/tree/master/example).

### Options

*JavaScript*

The ant task supports the following attributes:
<table>
    <tr>
        <th>Attribute</th>
        <th>Required?</th>
        <th>Default</th>
    </tr>
    <tr>
    	<td>toDir</td>
    	<td>Yes</td>
    	<td>N/A</td>
    </tr>
    <tr>
        <td>linebreak</td>
        <td>No</td>
        <td>-1</td>
    </tr>
    <tr>
    	<td>munge</td>
    	<td>No</td>
    	<td>true</td>
    </tr>
</table>