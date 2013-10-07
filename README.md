About ant-yui-compressor
==================

ant-yui-compressor is an [Apache Ant](http://ant.apache.org/) task for compressing multiple JavaScript and CSS files using [YUI compressor](http://developer.yahoo.com/yui/compressor/).

### Features
* JS files minification 
* CSS files minification
* Option to automatically delete original source files after generating minified files

##### Origins

This project is based on [yui-compressor-ant-task](https://code.google.com/p/yui-compressor-ant-task/) by Simon Buckle 
which only supports JS minification. 

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
**Note: The `toDir` attribute, as well as `fileset` & `mapper` elements are required**. 
The `fileset` element specifies the list of files to be minified. The `mapper` elements describes the naming convention for minified files.
Both [fileset](http://ant.apache.org/manual/Types/fileset.html) and [mapper](http://ant.apache.org/manual/Types/mapper.html) are standard Ant types and have various configuration options.

### Example

A working ant sample project is available with the source code (https://github.com/parambirs/ant-yui-compressor/tree/master/example).

### Options

**JavaScript**

The ant task supports the following attributes for JS files:
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
        <td>deleteOriginal</td>
        <td>No</td>
        <td>false</td>
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
    <tr>
    	<td>preserveAllSemiColons</td>
    	<td>No</td>
    	<td>false</td>
    </tr>
    <tr>
    	<td>disableOptimizations</td>
    	<td>No</td>
    	<td>false</td>
    </tr>
    <tr>
    	<td>verbose</td>
    	<td>No</td>
    	<td>false</td>
    </tr>
</table>

**CSS**

There are only a couple of options available for CSS files:
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
</table>
