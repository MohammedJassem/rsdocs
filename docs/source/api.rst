API
===

The API of **Rakam Systems** is designed to handle the core functionalities of vector store management, content extraction, node processing, and retrieval-augmented generation (RAG) using large language models (LLMs).

Below are the key modules and classes available in this library.

.. autosummary::
   :toctree: generated

   rakam_systems.vector_store.VectorStores
   rakam_systems.core.Node
   rakam_systems.core.NodeMetadata
   rakam_systems.ingestion.content_extractors.PDFContentExtractor
   rakam_systems.ingestion.node_processors.CharacterSplitter
   rakam_systems.generation.agents.RAGGeneration
   rakam_systems.generation.agents.Agent
   rakam_systems.generation.agents.ClassifyQuery
