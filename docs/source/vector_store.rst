Vector Store Module
===================

The `rakam_systems.vector_store` module defines the `VectorStores` class, which is responsible for managing vector stores, storing data, and handling embeddings using FAISS and SentenceTransformers.

Classes
-------

.. autosummary::
   :toctree: generated

   rakam_systems.vector_store.VectorStores

VectorStores
------------

.. autoclass:: rakam_systems.vector_store.VectorStores
   :members:
   :undoc-members:
   :show-inheritance:

   A class for managing vector stores with FAISS and SentenceTransformers.

Methods:

- **__init__**: Initializes the vector store with a base path and embedding model.
- **load_all_stores**: Loads all vector stores from a directory.
- **load_store**: Loads a specific vector store from a directory.
- **predict_embeddings**: Generates embeddings for a given query.
- **search**: Searches for the closest embeddings in the specified store.
- **get_embeddings**: Generates embeddings for a list of sentences.
- **create_from_files**: Creates a FAISS index from files.
- **create_from_nodes**: Creates a FAISS index from nodes.
- **add_nodes**: Adds nodes to an existing store and updates the index.
- **delete_nodes**: Deletes nodes from an existing store.
- **add_files**: Adds files and their nodes to a vector store.
- **delete_files**: Deletes files and their nodes from a vector store.
