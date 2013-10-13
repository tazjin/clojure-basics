# Diving into Clojure

So you want to start with Clojure, good. This will help you getting your environment up and running and point you to things that can easily get you started.

## Installing Clojure  
Installing Clojure is as easy as getting [Leiningen](http://leiningen.org) up and running, this should be easy on most operating systems because package managers like Homebrew on OS X or your typical APT repos on $whatever already have it. So run `brew install leiningen` or the equivalent for your OS - also make sure you have a version >= 2.0

You also (obviously) need the JDK/JRE installed.

After this you open your favourite terminal and run `lein repl` which downloads Clojure and opens a REPL for you to experiment with. Quit this with (quit)

## Editing Clojure
Clojure is a dialect of Lisp and, as such, very well suited for structural editing using a tool like [Paredit](http://www.youtube.com/watch?v=D6h5dFyyUX0) in Emacs. Emacs is also the editor I recommend above all others, if you already use it make sure you have `nrepl.el`, `rainbow-delimiters` and `paredit` installed and running - take some time to get familiar with Paredit if you aren't already!

If you're new to Emacs and want to focus on Clojure you might want to look at [Emacs for Clojure](https://github.com/stuarth/emacs-for-clojure) which installs an easy default configuration for Clojure programming.

If you're a vim user I can't help you, make sure you get plugins that provide automatic paranthesis balancing, nrepl integration, structural editing like paredit and something to colour matching parens pairs (rainbow-delimiters). Feel free to send a pull request if you figure it out!

If you're an IntelliJ user there's the new and experimental [Cursive Clojure](http://cursiveclojure.com/).

If you're a Sublime user: I honestly don't know, find otu and send a pull request!

## Basics  
Leiningen is Clojure's dependency manager that downloads libraries for you to use from Maven repositories. If you come from the Java world, building Clojure with Maven is possible but I'm the wrong person to ask about that :-)

It also organizes your projects and creates them according to templates, there are a few important ones for learning.

* `default`: Used by default if you specify nothing else. Creates an empty, simply structured project for library development.
* `app`: This is a simply structured Clojure project that compiles to an executable jar file.  
* `experiment`: This is a pretty cool recent template which just gives you a single source file and a project file to quickly experiment with things. **I recommend using this while learning**.
* `compojure-app`: A simple web application template based on Compojure/Ring. (More about this later)

You can now create an empty project using `lein new experiment my-thing`, where "my-thing" is the name of the project.

Have a look at the `project.clj` file to understand its structure! This is also where you add dependencies which are then automatically downloaded by Leiningen.

## Learning Clojure

Before doing anything else, do some very basic experimentation with [Try Clojure](http://tryclj.com/). If you like this style of learning I recommend that you get the [Clojure Koans](https://github.com/functional-koans/clojure-koans) and work through them.

If you still want to continue in this style register on [4Clojure](http://www.4clojure.com/) and start doing some of the more advanced "Koans" there.

You want a classic manual? I recommend [Programming Clojure](http://pragprog.com/book/shcloj2/programming-clojure).

More of a web developer and like to get your hands dirty right away? Have a look at the beta of [Web Development with Clojure](http://pragprog.com/book/dswdcloj/web-development-with-clojure).

These should be enough to get you started.

## Other resources

There are lots of interesting things about Clojure on the internet, this includes talks, cool libraries and interesting tutorials. I'll try to collect the best here.

### Talks
* Rich Hickey (the creator of Clojure) gave one talk that I think everybody must see, not just Clojure developers, every developer: [Are We There Yet?](http://www.infoq.com/presentations/Are-We-There-Yet-Rich-Hickey)
* Chris Ford's [Functional Composition](http://www.youtube.com/watch?v=Mfsnlbd-4xQ) is a great talk about the functional nature of music (and also, a bit, about Clojure).


### Cool projects
* [ClojureScript](https://github.com/clojure/clojurescript) - Never write Javascript again! Clojure to JS compiler.
* If you come from a statically typed language and are already missing your types, don't fret and look at [core.typed](https://github.com/clojure/core.typed). Ambrose, the guy who made core.typed, also appeared on the Relevance (now Cognitect) podcast and [explained core.typed](http://thinkrelevance.com/blog/2013/10/08/ambrose-bonnaire-sergeant-cognicast-episode-042).
* [Pedestal](http://pedestal.io/) is a cool framework for client/server web applications, made by Cognitect (formerly Relevance)
* [Overtone](http://overtone.github.io/) is a programmable music library which is also the one featured in Chris Ford's talk linked above. Fun to play with!

### Libraries you should know
* For all JSON needs, [Cheshire](https://github.com/dakrone/cheshire)  
* [Ring](https://github.com/ring-clojure/ring) and [Compojure](https://github.com/weavejester/compojure), the basics of almost all Clojure web stacks  
* [Luminus](http://www.luminusweb.net/) or [lib-noir](https://github.com/noir-clojure/lib-noir), both collections of useful libraries on top of Compojure and Ring
* [Korma](http://www.sqlkorma.com/), a Clojure DSL for generating SQL queries
* more to come ...

### Clojure podcasts
* [ThinkRelevance](http://thinkrelevance.com/blog/tags/podcast), the Relevance (now Cognitect) podcast. I think they're renaming it to Cognicast. This one is very good and has featured many interesting people!  
* [Mostly λazy](http://mostlylazy.com/), a more informal Clojure podcast

### Other tutorials
* For front-end developers: The [pedestal-app tutorial](https://github.com/pedestal/app-tutorial) is great I hear, it takes some time to work through though.
* More to come ...
