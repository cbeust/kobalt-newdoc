## Build.kt contents

* #### Imports
* #### Project declaration(s) using the project directive
* #### Since it's a Kotlin file, it can also contain any class or function you need


#### Example

{% highlight kotlin %}
import com.beust.kobalt.*
import java.time.ZonedDateTime
import java.time.format.DateTimeFormatter

fun getVersion() = ZonedDateTime.now().format(DateTimeFormatter.BASIC_ISO_DATE)

val kobalt = project {
    name = "kobalt"
    group = "com.beust"
    artifactId = name
    version = getVersion()
    directory = homeDir("kotlin/kobalt")
}
{% endhighlight %}

Note: the output of the project <i>directive</i> is assigned to the val <code>kobalt</code>.  You could refer to the project via the val <code>kobalt</code> further in the build file, should you ever need to.

-----

## project directive

#### Parameters

This directive accepts these **required** and optional parameters

- **name**
- group
- artifactId
- version
- description
- directory
  
  Specifies the directory of a project that not in the root.  This means that one build file can be used to build multiple projects.

#### Directives

Within this directive you can use these other directives:

- sourceDirectories
- sourceDirectoriesTest
- dependencies
- dependenciesTest
- application
- assemble

-----

## dependencies directive

#### Parameters

This directive accepts these **required** and optional parameters

- compile()

#### Directives


-----

## dependenciesTest directive

#### Parameters

This directive accepts these **required** and optional parameters

- compile()

#### Directives


-----

## application directive

#### Parameters

This directive accepts these **required** and optional parameters

#### Directives


-----

## assemble directive

#### Parameters

This directive accepts these **required** and optional parameters

#### Directives

Within an assemble directive you may use these other directives:

- jar
  - fatJar
  - manifest
- zip
  - include
- war
  - include
