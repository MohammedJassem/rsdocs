Node Processor Module
=====================

The `rakam_systems.ingestion.node_processors` module provides classes for processing nodes, including splitting content based on characters and Markdown headers.

Classes
-------

.. autosummary::
   :toctree: generated

   rakam_systems.ingestion.node_processors.NodeProcessor
   rakam_systems.ingestion.node_processors.CharacterSplitter
   rakam_systems.ingestion.node_processors.MarkdownSplitter

NodeProcessor
-------------

.. autoclass:: rakam_systems.ingestion.node_processors.NodeProcessor
   :members:
   :undoc-members:
   :show-inheritance:

   Abstract base class for processing nodes in a `VSFile`.

CharacterSplitter
-----------------

.. autoclass:: rakam_systems.ingestion.node_processors.CharacterSplitter
   :members:
   :undoc-members:
   :show-inheritance:

   Splits the content of each node based on a specified number of characters and overlap.

MarkdownSplitter
----------------

.. autoclass:: rakam_systems.ingestion.node_processors.MarkdownSplitter
   :members:
   :undoc-members:
   :show-inheritance:

   Splits the content of each node in a `VSFile` based on Markdown headers.
