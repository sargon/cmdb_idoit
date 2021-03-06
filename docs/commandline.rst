.. _commandline:

Commandline Interface
=====================

The command line tool ``cmdb`` provides an easy access to various information
about the connected *i-doit* instance. To use it you HAVE TO configure the
connections details for your instance in the configuration file. See :ref:`configuration`.


::

  Usage: cmdb [OPTIONS] COMMAND [ARGS]...

  Options:
    --profile TEXT        Profile to use
    --debug / --no-debug
    --help                Show this message and exit.

  Commands:
    category
    object
    type

Via the option `--profile` you are able to select a configured profile. The default profile is named ``main``.
  

List Object Types
-----------------

Knowing the available object types is key to accessing and storing data through the api.

::

     $ cmdb type list
     Group    Title    Id    Const 
     Software    System service    1   C__OBJTYPE__SERVICE 
     ...


Object-Type definition
----------------------

When accessing types you also need to know about the structure of the type.

::

    $ cmdb type declaration C__OBJTYPE__SERVICE


Dialog value definition
-----------------------

The know the available values and constants for a dialog attibute, you can list them:

::

    $ cmdb category dialog C__CATG__GLOBAL cmdb_status
    Id	Constant		Title
    1	C__CMDB_STATUS__PLANNED		planned
    2	C__CMDB_STATUS__ORDERED		ordered
    3	C__CMDB_STATUS__DELIVERED		delivered
    4	C__CMDB_STATUS__ASSEMBLED		assembled
