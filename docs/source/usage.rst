Usage
=====

.. _installation:

Installation
------------

To use **Rakam Systems**, you can install the pypi library using `pip`:

.. code-block:: console

   (.venv) $ pip install rakam-systems

This will install the library and its necessary dependencies such as `faiss`, `sentence-transformers`, and others listed in the **README**.

Creating Vector Stores
----------------------

To create and manage vector stores, you can use the ``VectorStores`` class from the `rakam_systems.vector_store` module.

Example:

.. code-block:: python

   from rakam_systems.vector_store import VectorStores
   from rakam_systems.core import VSFile, Node, NodeMetadata

   # Initialize a Vector Store
   vector_store = VectorStores(base_index_path="path/to/index", embedding_model="sentence-transformers/all-MiniLM-L6-v2")

   # Create vector store from nodes
   nodes = [
       Node(content="Text data 1", metadata=NodeMetadata(source_file_uuid="file1", position=1)),
       Node(content="Text data 2", metadata=NodeMetadata(source_file_uuid="file2", position=2))
   ]
   vector_store.create_from_nodes("store_name", nodes)

Retrieval-Augmented Generation (RAG)
------------------------------------

**RAG** enables the combination of vector store search with LLM-based prompt generation to produce context-enriched responses.

Example:

.. code-block:: python

   from rakam_systems.generation.agents import RAGGeneration, Agent
   from rakam_systems.vector_store import VectorStores

   # Initialize Vector Store and Agent
   vector_store = VectorStores(base_index_path="path/to/index", embedding_model="sentence-transformers/all-MiniLM-L6-v2")
   agent = Agent(model="gpt-3.5-turbo", api_key="your_openai_api_key")

   # Create RAG Action
   rag_action = RAGGeneration(agent, sys_prompt="System Prompt", prompt="User Prompt", vector_stores=vector_store)

   # Execute RAG Action
   query = "What is the capital of France?"
   result = rag_action.execute(query=query)
   print(result)

Content Extraction
------------------

This library provides several content extractors, such as extracting from PDFs or JSON files.

Example for extracting from a PDF:

.. code-block:: python

   from rakam_systems.ingestion.content_extractors import PDFContentExtractor

   # Initialize PDF Content Extractor
   pdf_extractor = PDFContentExtractor(parser_name="SimplePDFParser", output_format="markdown")

   # Extract content from a PDF file
   vs_files = pdf_extractor.extract_content(source="path/to/file.pdf")

Node Processing
---------------

To split content into smaller chunks (nodes), you can use the `NodeProcessor` classes.

Example for processing nodes:

.. code-block:: python

   from rakam_systems.ingestion.node_processors import CharacterSplitter

   # Initialize Node Processor
   splitter = CharacterSplitter(max_characters=512, overlap=50)

   # Process Nodes
   splitter.process(vs_file)

Classification with Vector Stores
----------------------------------

Use the vector store to classify queries based on predefined trigger queries.

Example:

.. code-block:: python

   from rakam_systems.generation.agents import ClassifyQuery
   import pandas as pd

   # Sample Data for Classification
   trigger_queries = pd.Series(["What is the capital of", "Tell me about"])
   class_names = pd.Series(["Geography", "General Info"])

   # Initialize Classification Action
   classifier = ClassifyQuery(agent=None, trigger_queries=trigger_queries, class_names=class_names)

   # Classify a new query
   result = classifier.execute("What is the capital of France?")
   print(result)

