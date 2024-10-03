Agents Module
=============

The `rakam_systems.generation.agents` module provides classes for executing various actions such as query classification, prompt generation, and retrieval-augmented generation (RAG).

Classes
-------

.. autosummary::
   :toctree: generated

   rakam_systems.generation.agents.Agent
   rakam_systems.generation.agents.Action
   rakam_systems.generation.agents.ClassifyQuery
   rakam_systems.generation.agents.PromptGeneration
   rakam_systems.generation.agents.RAGGeneration

Agent
-----

.. autoclass:: rakam_systems.generation.agents.Agent
   :members:
   :undoc-members:
   :show-inheritance:

   Represents the agent that can perform different actions based on input and state.

Action
------

.. autoclass:: rakam_systems.generation.agents.Action
   :members:
   :undoc-members:
   :show-inheritance:

   Abstract base class for actions that agents can perform.

ClassifyQuery
-------------

.. autoclass:: rakam_systems.generation.agents.ClassifyQuery
   :members:
   :undoc-members:
   :show-inheritance:

   Classifies a query by finding the closest match in a vector store using FAISS and SentenceTransformers.

PromptGeneration
----------------

.. autoclass:: rakam_systems.generation.agents.PromptGeneration
   :members:
   :undoc-members:
   :show-inheritance:

   Generates a prompt using a provided system prompt and user input. Supports streaming and non-streaming modes.

RAGGeneration
-------------

.. autoclass:: rakam_systems.generation.agents.RAGGeneration
   :members:
   :undoc-members:
   :show-inheritance:

   Performs Retrieval-Augmented Generation (RAG) by combining vector store search results with LLM generation.
