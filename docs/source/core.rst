Core Module
===========

The `rakam_systems.core` module defines the core structures and classes such as `VSFile`, `Node`, and `NodeMetadata` that are essential for managing and processing data in **Rakam Systems**.

Classes
-------

.. autosummary::
   :toctree: generated

   rakam_systems.core.VSFile
   rakam_systems.core.Node
   rakam_systems.core.NodeMetadata

VSFile
------

.. autoclass:: rakam_systems.core.VSFile
   :members:
   :undoc-members:
   :show-inheritance:

   Represents a file in the vector store, containing metadata and nodes extracted from the content of the file.

Node
----

.. autoclass:: rakam_systems.core.Node
   :members:
   :undoc-members:
   :show-inheritance:

   Represents a node with content and associated metadata, which is stored in the vector store.

NodeMetadata
------------

.. autoclass:: rakam_systems.core.NodeMetadata
   :members:
   :undoc-members:
   :show-inheritance:

   Holds metadata for a node, including the file's UUID, position within the file, and any custom information.
