=========================
 RabbitMQ Munin Plug-Ins
=========================

Screenshots
===========

.. image:: http://cloud.github.com/downloads/ask/rabbitmq-munin/rabbitmq-munin-connections.png

.. image:: http://cloud.github.com/downloads/ask/rabbitmq-munin/rabbitmq-munin-consumers.png

.. image:: http://cloud.github.com/downloads/ask/rabbitmq-munin/rabbitmq-munin-list_queues.png

.. image:: http://cloud.github.com/downloads/ask/rabbitmq-munin/rabbitmq-munin-queue-memory.png

.. image:: http://cloud.github.com/downloads/ask/rabbitmq-munin/rabbitmq-munin-unacknowledged.png

Installation
============

Copy the plug-ins to the munin plugin directory, e.g ``/etc/munin/plugins/``.

Granting Permissions
====================

To use these plug-ins you have to tell munin-node to execute them as
root by changing the plug-in configuration file (on debian that is
``/etc/munin/plugin-conf.d``)::

    [rabbitmq-consumers]
    user root

    [rabbitmq-messages]
    user root

    [rabbitmq-messages_unacknowledged]
    user root

    [rabbitmq-messages_uncommitted]
    user root

    [rabbitmq-queue_memory]
    user root


Using a Custom Virtual Host
============================

You can set the name of virtual host by changing the plug-in configuration
file (on debian that is ``/etc/munin/plugin-conf.d``)::

    [rabbitmq-consumers]
    env.vhost vhostname

    [rabbitmq-messages]
    env.vhost vhostname

    [rabbitmq-messages_unacknowledged]
    env.vhost vhostname

    [rabbitmq-messages_uncommitted]
    env.vhost vhostname

    [rabbitmq-queue_memory]
    env.vhost vhostname

Author
======

Ask Solem <askh@opera.com>
