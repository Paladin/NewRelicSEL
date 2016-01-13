New Relic SELinux Policy Module
===============================

This is the type enforcement file for creating a policy module that allows the New Relic monitoring agents to run properly on SELinux systems. This is probably not the ultimate type enforcement file, but it contains everything I know about what it needs.

Installation
------------

This is just the type enforcement file. It needs to be compiled and installed in your system in order to function:

    checkmodule -M -m -o newrelic.mod newrelic.te
    semodule_package -o newrelic.pp -m newrelic.mod
    semodule -i newrelic.pp

