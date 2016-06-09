## Build.kt contents

* #### Imports
* #### Project declaration(s) using the project <i>directive</i>
* #### Since it's a Kotlin file, it can also contain any class or function you need


#### Example

{% highlight kotlin %}
import com.beust.kobalt.*

val kobalt = project {
    name = "kobalt"
    group = "com.beust"
    artifactId = name
    version = "0.62"
    directory = homeDir("kotlin/kobalt")
}
{% endhighlight %}

Note: the output of the project <i>directive</i> is assigned to the val <code>kobalt</code>.  You could refer to the project via the val <code>kobalt</code> further in the build file, should you ever need to.

-----

## project Directive

#### Fields

This directive accepts these **required** and optional fields

- **name**
- group
- artifactId
- version
- description
- directory
  
  Specifies the directory of a project that not in the root.  This means that one build file can be used to build multiple projects.

#### Directives

Within this directive you can use these other directives:

- dependencies
- dependenciesTest
- application
- assemble

-----

## dependencies Directive

#### Fields

This directive accepts these **required** and optional fields

#### Directives


-----

## dependenciesTest Directive

#### Fields

This directive accepts these **required** and optional fields

#### Directives


-----

## application Directive

#### Fields

This directive accepts these **required** and optional fields

#### Directives


-----

## assemble Directive

#### Fields

This directive accepts these **required** and optional fields

#### Directives

Within an assemble directive you may use these other directives:

- jar
  - fatJar
  - manifest
- zip
  - include
- war
  - include
