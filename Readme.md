# Groovy on Windows docker file

The purpose of this project is to load Groovy on Windows in Docker. For the official Groovy project see <https://github.com/groovy/docker-groovy/>.

## What is Groovy?

[Apache Groovy](http://groovy-lang.org/) is a powerful, optionally typed and dynamic language, with static-typing and static compilation capabilities, for the Java platform aimed at improving developer productivity thanks to a concise, familiar and easy to learn syntax. It integrates smoothly with any Java program, and immediately delivers to your application powerful features, including scripting capabilities, Domain-Specific Language authoring, runtime and compile-time meta-programming and functional programming.


## Building the container
```#powershell
docker build -t groovy-windows .
```

## Running a Groovy script
```
docker run --rm -v "$(gl):c:\groovy\scripts" -w 'c:\groovy\scripts' groovy-windows groovy.bat HelloWorld.groovy
```