# Lyrics Finder

A simple n8n workflow that allows users to find and save song lyrics through a chat interface.

## Overview

This project is an n8n workflow that:
1. Accepts user input through a chat interface
2. Extracts artist name and song title from the input
3. Fetches lyrics from the lyrics.ovh API
4. Creates a Google Doc with the formatted lyrics

## How It Works

1. **User Input**: When a chat message is received, the workflow is triggered
2. **Information Extraction**: The workflow uses an AI model (GPT-4o-mini) to extract the artist and song title from the user's message
3. **Conditional Logic**: The workflow checks if the user is asking for a list of tools or requesting lyrics
4. **Lyrics Retrieval**: If lyrics are requested, the workflow calls the lyrics.ovh API to fetch the lyrics
5. **Document Creation**: The lyrics are formatted and saved to a Google Doc with the song title and artist as the header

## Technologies Used

- **n8n**: Workflow automation platform
- **OpenAI API**: Used for natural language processing and information extraction
- **lyrics.ovh API**: Public API for retrieving song lyrics
- **MCP Client**: Model Context Protocol client for tool interactions
- **Google Docs**: For storing and formatting the retrieved lyrics

## Setup Requirements

To use this workflow, you'll need:

1. An n8n instance (cloud or self-hosted)
2. An OpenAI API key
3. Access to Google Docs (for saving lyrics)

## Usage

Simply send a message with the artist and song title to the chat interface. For example:
- "Get me lyrics for Bohemian Rhapsody by Queen"
- "I'd like to see the lyrics for Imagine by John Lennon"

The workflow will extract the information, fetch the lyrics, and save them to a Google Doc.

## Notes

- This workflow uses the free lyrics.ovh API which may have rate limits or service interruptions
- The information extraction works best with clear artist and song title mentions

## License

[Add your chosen license here]

## Author

[Your name/username]
