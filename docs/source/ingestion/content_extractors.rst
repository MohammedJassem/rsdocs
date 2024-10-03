Content Extractor Module
========================

The `rakam_systems.ingestion.content_extractors` module provides various content extractors to extract data from different sources like PDFs, URLs, and JSON files.

Classes
-------

.. autosummary::
   :toctree: generated

   rakam_systems.ingestion.content_extractors.ContentExtractor
   rakam_systems.ingestion.content_extractors.SimplePDFParser
   rakam_systems.ingestion.content_extractors.LlamaPDFParser
   rakam_systems.ingestion.content_extractors.PDFContentExtractor
   rakam_systems.ingestion.content_extractors.URLContentExtractor
   rakam_systems.ingestion.content_extractors.JSONContentExtractor

SimplePDFParser
---------------

.. autoclass:: rakam_systems.ingestion.content_extractors.SimplePDFParser
   :members:
   :undoc-members:
   :show-inheritance:

   A simple PDF parser that extracts text from PDF files using PyMuPDF.

LlamaPDFParser
--------------

.. autoclass:: rakam_systems.ingestion.content_extractors.LlamaPDFParser
   :members:
   :undoc-members:
   :show-inheritance:

   A PDF parser that extracts text using the LlamaParse API.

PDFContentExtractor
-------------------

.. autoclass:: rakam_systems.ingestion.content_extractors.PDFContentExtractor
   :members:
   :undoc-members:
   :show-inheritance:

   Extracts content from PDF files using the specified parser (either `LlamaParse` or `SimplePDFParser`).

