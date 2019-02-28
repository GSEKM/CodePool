##Here's a guide on how to install and run Analizo, a toolkit for source code analysis and visualization.

Add the repositories on the /etc/apt/sources.list:

```
deb http://analizo.org/download/ ./
deb-src http://analizo.org/download/ ./

deb http://debian.joenio.me unstable/
deb-src http://debian.joenio.me unstable/
```
Get the repositories signing key as root (you can use 'sudo -i' for Debian users):

```
wget -O - http://debian.joenio.me/signing.asc | apt-key add -
wget -O - http://analizo.org/download/signing-key.asc | apt-key add -
```

And install the doxyparse and the last version of analizo:

```
apt install doxyparse=1.8.11-1
apt install analizo
```

##Guide to Analizo
Go into the project folder from the terminal and run the analizo with the "metrics option":
```
analizo metrics
```

And it'll list a series of metrics measuring each file. Here is a list of each metric that'll show up:

Global Metrics:
- change_cost - Change Cost
- total_abstract_classes - Total Abstract Classes
- total_cof - Total Coupling Factor
- total_loc - Total Lines of Code
- total_methods_per_abstract_class - Methods per Abstract Class
- total_modules - Total Number of Modules
- total_modules_with_defined_attributes - Total number of modules with at least one defined attributes
- total_modules_with_defined_methods - Total number of modules with at least one defined method
- total_nom - Total Number of Methods

Module Metrics:
- acc - Afferent Connections per Class (used to calculate COF - Coupling Factor)
- accm - Average Cyclomatic Complexity per Method
- amloc - Average Method Lines of Code
- anpm - Average Number of Parameters per Method
- cbo - Coupling Between Objects
- dit - Depth of Inheritance Tree
- lcom4 - Lack of Cohesion of Methods
- loc - Lines of Code
- mmloc - Max Method LOC
- noa - Number of Attributes
- noc - Number of Children
- nom - Number of Methods
- npa - Number of Public Attributes
- npm - Number of Public Methods
- rfc - Response for a Class
- sc - Structural Complexity
