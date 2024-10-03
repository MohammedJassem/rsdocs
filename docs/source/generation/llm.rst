LLM Module
==========

The `rakam_systems.generation.llm` module provides the `LLM` class for interacting with large language models (LLMs) such as OpenAI's GPT models.

Classes
-------

.. autosummary::
   :toctree: generated

   rakam_systems.generation.llm.LLM

LLM
---

.. autoclass:: rakam_systems.generation.llm.LLM
   :members:
   :undoc-members:
   :show-inheritance:

   The `LLM` class handles interactions with OpenAI models and provides methods for generating responses in both streaming and non-streaming modes.

Methods:

- **call_llm**: Calls the LLM in non-streaming mode and returns the result.
- **call_llm_stream**: Calls the LLM in streaming mode and yields response chunks.
