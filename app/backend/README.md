# Backend Application Documentation

This document provides an overview and documentation for the source files located in the `/app/backend` folder of the project.

## Overview

The backend application is designed to support the operations of a chat application, with functionalities that include document processing, user authentication, and communication with frontend services. It is built using [Quart](https://quart.palletsprojects.com/), a Python framework for asynchronous web applications.

## Source Files

### `prepdocs.py`

- **Description**: This script is responsible for preparing and processing documents to be used by the chat application. It includes functions for parsing documents, extracting relevant information, and formatting the data for use within the application.
- **Key Functions**:
  - `parse_document`: Parses the input document and extracts sections based on predefined markers.
  - `format_data`: Formats the extracted data for easier consumption by the chat application.
- **Usage**: This script can be executed directly or imported as a module in other parts of the backend application for document processing tasks.

## Customizing the Backend

The backend application can be customized to suit different requirements. Here are some areas where customization can be applied:

- **Data Processing**: The `prepdocs.py` script can be modified to change the way documents are processed, such as adding new parsing rules or changing the data extraction logic.
- **Authentication**: Implement or modify authentication mechanisms to secure access to the backend services.
- **Communication Protocol**: Adjust the AI Chat HTTP Protocol implementation as needed to improve the communication between the frontend and backend services.

For more detailed customization options, refer to the [Customizing the Backend](docs/customization.md#customizing-the-backend) section in the project documentation.

## Further Reading

- [Quart Documentation](https://quart.palletsprojects.com/)
- [AI Chat HTTP Protocol](https://aka.ms/chatprotocol)

Please refer to the individual source files for more detailed documentation on specific functionalities and implementation details.

## Dependencies

Here's a summary of the key dependencies and their purposes:

aiofiles (23.2.1): Asynchronous file operations, used via Quart.
aiohttp (3.9.5): Asynchronous HTTP client/server framework.
aiosignal (1.3.1): Required by aiohttp for signal handling.
annotated-types (0.7.0): Used by Pydantic for annotated types.
anyio (4.4.0): Provides asynchronous networking and concurrency support, used by HTTPx and OpenAI.
asgiref (3.8.1): ASGI (Asynchronous Server Gateway Interface) utilities, used by OpenTelemetry instrumentation for ASGI.
attrs (23.2.0): Provides classes without boilerplate, used by aiohttp.
azure-ai-documentintelligence (1.0.0b3) and azure-cognitiveservices-speech (1.38.0): Azure services for document intelligence and speech recognition.
azure-common (1.1.28): Shared Azure service client library components, used by Azure Search Documents.
azure-core (1.30.2): Core library for Azure Python SDKs, used by multiple Azure services including document intelligence, tracing, and identity.