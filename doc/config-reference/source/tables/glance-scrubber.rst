..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _glance-scrubber:

.. list-table:: Description of scrubber configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[DEFAULT]**
     -
   * - ``wakeup_time`` = ``300``
     - (Integer) Time interval, in seconds, between scrubber runs in daemon mode.

       Scrubber can be run either as a cron job or daemon. When run as a daemon, this configuration time specifies the time period between two runs. When the scrubber wakes up, it fetches and scrubs all ``pending_delete`` images that are available for scrubbing after taking ``scrub_time`` into consideration.

       If the wakeup time is set to a large number, there may be a large number of images to be scrubbed for each run. Also, this impacts how quickly the backend storage is reclaimed.

       Possible values:

       * Any non-negative integer

       Related options:

       * ``daemon``

       * ``delayed_delete``
