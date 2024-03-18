# R.O.B.U.S.T. check (v.1.0)

![logo](https://miro.medium.com/v2/resize:fit:400/format:webp/1*4em6vs3ZgBa4bxhQaSbzqA.jpeg)

A checklist for php composer packages by Michael Kraft.

This could be also used for other programming languages and/or other dependency managers.

## Description
One of the biggest problem in PHP are bad composer dependencies, specially when its comes to security reasons and update scenarios.

Over the years I discussed different problems/ideas/solutions and learned the hard way: 
*a few hours of analyzing by one person can safe years of unhappy coding for the whole team*

I call it **R.O.B.U.S.T. check** and it contains some manual package analyzes, that could help you to choose the right one for a happy dev life. 
Use the checklist when you comparing new packages or with existing packages/composer.json.

### Thanks you for accompanying work in the past with
Peter Petermann, Stefan Priebsch, Sebastian Bergmann

## Definition
**R.O.B.U.S.T.** stands for
- **R**esearch: find the best described package
- **O**verload: find the unique root package
- **B**enchmark: find the cheapest package
- **U**pdates: find the freshest package
- **S**ource: find the cleanest package
- **T**ests: find the most reliable package

## All “Do not” Points (TLTR)
### Research
- Don’t never compare with other packages
- Don’t use completely unknown packages
- Don’t use packages with many open bugs/issues with slow/no responses
- Don’t use packages from inactive or deleted users
- Don’t use packages without documentations, readme or changelogs
- Don’t use packages with no open/free discussions

### Overload
- Don’t use packages that requires a lot of other packages
- Don’t use packages that uses other insecure, unstable, untested or dead packages
- Don’t use packages that delivery other functionality like bundles

### Benchmark
- Don’t use high costs packages
- Don’t use over complexed packages, everyone should understand the usage quickly

### Updates
- Don’t use dead packages
- Don’t use packages with a long pipeline on important bugs
- Don’t use packages without semantic versioning
- Don’t use packages in alpha or beta status
- Don’t use unstable packages
- Don’t use old outdated packages
- Don’t use packages that needs 2+ month for php-updates

### Source
- Don’t use packages that you could write by yourself
- Don’t use packages that doesn’t following the PHP-FIG PSR standards
- Don’t use packages that doesn’t follow the SOLID principles
- Don’t use packages that forces you to use anti patterns or bad practices
- Don’t use packages with bad or no own error handling
- Don’t use packages without functionality standards

### Tests
- Don’t use untested packages
- Don’t use packages with broken tests
- Don’t use packages with uncovered code

## Details explained
### Research
**Find the best described package**

Check articles, user feedbacks, discussions, bugs, problems and issues

- **Don’t never compare with other packages**
- **Don’t use completely unknown packages**
- **Don’t use packages with many open bugs/issues with slow/no responses**

Check if the contributor is active

- **Don’t use packages from inactive or deleted users**

Check documentations and changelogs on GitHub or website

- **Don’t use packages without documentations, readme or changelogs**

Check active communities and active user feedback

- **Don’t use packages with no open/free discussions**

*Creating a bad package is easy, creating a good package is hard.*

**Problems that can be prevented**

- The package need hours to integrate and then it doesn’t work like you expected.
- The package start throwing errors after a period, while several services from you app depends on that package now, and you cant find help/support.
- The package did an undocumented update and nothing works anymore.

### Overload
**Find the unique root package**

Check all new dependencies in composer.json from that package and recursive all required

- **Don’t use packages that requires a lot of other packages**
- **Don’t use packages that uses other insecure, unstable, untested or dead packages**

Check for cohesion. It should do only one thing and this at its best

- **Don’t use packages that delivery other functionality like bundles**

**Problems that can be prevented**

- The package get updates and breaking changes because of functionality, that you never use.
- The package load own components and steal resources like memory, for functionality that you never use.
- The package has known or unknown security issues in functionality that you never use.
- The package cant be updated from them, because of an external required change/update.
- The package cant be updated from them, because they wait for other external update to the current php-version.
- The package doesn’t work anymore, because a dependencies has switched his requirements or removed older versions.

### Benchmark
**Find the cheapest package**

Check speed, cpu and memory while running the package and compare with other packages and native methods. search for benchmarks if you cant bench.

- **Don’t use high costs packages**

Check the learn curve, how easy is it for new users to understand

- **Don’t use over complexed packages, everyone should understand the usage quickly**

**Problems that can be prevented**

- The package uses 300% more cpu and memory like a native function or root/original bundle.
- The package needs at least 1month study from every employee, instead of using a self described solution

### Updates
**Find the freshest package**

When was the last update? no updates since 1year means often “dead“

- **Don’t use dead packages**

How fast did they communicate and fix reported issues/bugs on GitHub

- **Don’t use packages with a long pipeline on important bugs**

Check if it use semantic versioning

- **Don’t use packages without semantic versioning**

Check if the package is over v1.0.0?

- **Don’t use packages in alpha or beta status**

Check if the current/last major version is stable

- **Don’t use unstable packages**

Check if the current package version is for the current php-version

- **Don’t use old outdated packages**

Check how fast they update their package when php update his core

- **Don’t use packages that needs 2+ month for php-updates**

**Problems that can be prevented**

- The package forces you to work with older php-versions, because there is no newer package.
- The package integrate a package that has open security leaks.
- The package has an active dev-mode that show secret informations.
- The package doesn’t work in edge-cases well.

### Source
**Find the cleanest package**

Check how complex is that code

- **Don’t use packages that you could write by yourself**

Check if PSR is used

- **Don’t use packages that doesn’t following the PHP-FIG PSR standards**

Check the design from that code

- **Don’t use packages that doesn’t follow the SOLID principles**
- **Don’t use packages that forces you to use anti patterns or bad practices**
- **Don’t use packages with bad or no own error handling**
  
Check if the package uses the current standards for this functionality
- **Don’t use packages without functionality standards**

**Problems that can be prevented**

- The package destroys your code discipline or team guidelines.
- The package consumes your whole memory, remove decoupling and testability.
- Spend lot of time to struggle with a package instead of using native php functions as you need.

### Tests
**Find the most reliable package**

Check if the package has own tests

- **Don’t use untested packages**

Check the test quality

- **Don’t use packages with broken tests**

Check the test coverage

- **Don’t use packages with uncovered code**

**One of thephp.cc rule:** if there is no documentation -> **read the tests!**

**Problems that can be prevented**

- The package has weird methods that returned or worked differently as described.
- The package has weird methods that are unused, unfinished or old and not deleted.


https://medium.com/@mkraft_berlin/r-o-b-u-s-t-check-v-1-0-187ed8db8264
