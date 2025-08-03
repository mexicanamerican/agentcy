<div align="center">

<img width="100px" src="./misc/logo.png" />

# Agentcy 2.0

### Multi-Agent Creative Collaboration Platform

<p>
<img alt="GitHub Contributors" src="https://img.shields.io/github/contributors/amadad/agentcy" />
<img alt="GitHub Last Commit" src="https://img.shields.io/github/last-commit/amadad/agentcy" />
<img alt="" src="https://img.shields.io/github/repo-size/amadad/agentcy" />
<img alt="GitHub Stars" src="https://img.shields.io/github/stars/amadad/agentcy" />
<img alt="GitHub Forks" src="https://img.shields.io/github/forks/amadad/agentcy" />
<img alt="Github License" src="https://img.shields.io/badge/License-MIT-yellow.svg" />
<img alt="Twitter" src="https://img.shields.io/twitter/follow/amadad?style=social" />
</p>

</div>

-----

<p align="center">
  <a href="#-overview">Overview</a> •
  <a href="#-agents">Agents</a> •
  <a href="#-features">Features</a> •
  <a href="#-setup">Setup</a> • 
  <a href="#-usage">Usage</a> •
  <a href="#-roadmap">Roadmap</a> •
  <a href="#-license">License</a>
</p>

-----

A sophisticated multi-agent creative collaboration platform that transforms business challenges into comprehensive solutions through autonomous AI agents. Agentcy 2.0 combines advanced research, strategic planning, content creation, and visual design capabilities.

-----

## 📖 Overview

**Completely modernized and streamlined for 2024**, Agentcy 2.0 represents a complete evolution from experimental scripts to a production-ready creative agency platform. Built on [AG2](https://github.com/ag2ai/ag2) (the community-driven successor to AutoGen), it orchestrates specialized AI agents that collaborate like a real creative agency team.

### What's New in 2.0
- **🚀 AG2 Framework**: Modern, community-maintained multi-agent platform
- **🧠 Advanced Research**: Web search, intelligent scraping, and AI summarization
- **🎨 Visual Content**: AI image generation and critique workflows
- **📊 Professional Frameworks**: Marketing, copywriting, and media planning methodologies
- **🏗️ Production Ready**: Single consolidated file, robust error handling, organized outputs

## 🕵🏽 Agents

The enhanced agent team includes specialized roles for comprehensive creative solutions:

1. **Agency Manager**: Coordinates all project activities and ensures quality deliverables
2. **Agency Researcher**: Conducts advanced web research with intelligent scraping and summarization
3. **Agency Strategist**: Develops strategic frameworks using proven marketing methodologies
4. **Agency Copywriter**: Creates persuasive content using psychological principles and copywriting best practices
5. **Agency Visual Director**: Generates and critiques visual content using AI image generation
6. **Agency Marketer**: Designs comprehensive marketing campaigns and customer journeys
7. **Agency Media Planner**: Optimizes channel strategy using professional media planning frameworks
8. **Agency Director**: Provides creative leadership and ensures excellence across all outputs
9. **User Proxy**: Manages human interaction and oversees the collaborative process

## ✨ Features

### 🧠 Advanced Research Capabilities
- **Web Search**: Real-time search using Serper API
- **Intelligent Scraping**: Content extraction with Browserless and Selenium fallback
- **AI Summarization**: Direct OpenAI integration for content summarization (no LangChain dependency)
- **Research Reports**: Automatically generated and saved research documentation

### 🎨 Visual Content Creation
- **AI Image Generation**: Stability AI integration via Replicate
- **Image Critique**: LLaVA-powered image analysis and improvement suggestions
- **Visual Strategy**: Comprehensive visual direction and creative concepts

### 📊 Professional Frameworks
- **Marketing**: 4P's, STP, AIDA, Customer Journey, Marketing Funnel
- **Copywriting**: Reciprocity, Scarcity, Authority, Consistency, Social Proof, Liking
- **Media Planning**: RACE, POEM, OST, See-Think-Do-Care

### 🏗️ Production Features
- **Modern Dependencies**: AG2, OpenAI 1.98+, minimal focused dependencies
- **Organized Outputs**: Structured file organization with research/, content/, images/ folders
- **Error Handling**: Robust retry logic and graceful failure handling
- **Configuration Management**: Environment-based API key management 

<p align="center">
  <img src='./misc/flow.png' width=888>
</p>

## ⚙️ Setup & Configuration

### 1. Install Dependencies
```bash
# Using uv (recommended)
uv install

# Or using pip
pip install -e .
```

### 2. Set up API Keys
Copy the environment template and add your API keys:
```bash
cp .env.example .env
```

Edit `.env` with your API keys:
```bash
# Required
OPENAI_API_KEY=your_openai_api_key_here
SERPER_API_KEY=your_serper_api_key_here

# Optional (for enhanced features)
BROWSERLESS_API_KEY=your_browserless_api_key_here
REPLICATE_API_TOKEN=your_replicate_api_token_here
```

### 3. Configure AG2

**⚠️ SECURITY WARNING**: Never commit API keys to version control!

**Option A: Use .env only (Recommended)**
The system will automatically create AG2 config from your `.env` file. No additional setup needed.

**Option B: Create OAI_CONFIG_LIST file**
If you prefer separate AG2 configuration:
```json
[
    {
        "model": "gpt-4o",
        "api_key": "your_openai_api_key_here"
    }
]
```

**🔒 Security Best Practices:**
- Add `OAI_CONFIG_LIST` to your `.gitignore` 
- Never share or commit files containing API keys
- Revoke and regenerate keys if accidentally exposed

### 4. API Key Setup Guide
- **OpenAI**: Get your API key from [OpenAI Platform](https://platform.openai.com/api-keys)
- **Serper**: Sign up at [Serper.dev](https://serper.dev) for web search (free tier available)
- **Browserless** (Optional): Get API key from [Browserless.io](https://browserless.io) for enhanced scraping
- **Replicate** (Optional): Sign up at [Replicate.com](https://replicate.com) for AI image generation

## 🚀 Usage

### Quick Start
```bash
python agentcy.py
```

Follow the prompts to:
1. Enter your brand/company name
2. Describe your goal or problem statement
3. Watch the AI agents collaborate to create a comprehensive solution

### Example Session
```
📍 Enter the brand or company name: TechStartup
🎯 Enter your goal, brief, or problem statement: Launch a new mobile app for productivity
```

The system will generate:
- Market research and competitive analysis
- Strategic positioning and messaging
- Creative copy and content
- Visual concepts and imagery
- Marketing campaign strategy
- Media planning recommendations

### Output Structure
```
output/
├── research/          # Research reports and market analysis
├── content/           # Generated copy and content
├── images/            # AI-generated visual content
└── session_logs/      # Complete session transcripts
```

## 🛠️ Troubleshooting

### Common Issues

**"Configuration validation failed"**
- Ensure `OPENAI_API_KEY` and `SERPER_API_KEY` are set in `.env`
- Check that your OpenAI API key is valid and has sufficient credits

**"Module not found" errors**
- Run `uv install` or `pip install -e .` to install dependencies
- Optional features require additional packages (see error messages for specific install commands)

**Image generation not working**
- Install replicate: `pip install replicate`
- Set `REPLICATE_API_TOKEN` in your `.env` file
- Ensure you have credits in your Replicate account

**Research/scraping failures**
- Verify `SERPER_API_KEY` is correct
- For enhanced scraping, add `BROWSERLESS_API_KEY`
- Check your internet connection

### Testing Your Setup
Run the test suite to verify everything is working:
```bash
python test_agentcy.py
```

## 🔄 Migration from 1.0

If you're upgrading from Agentcy 1.0, here are the key changes:

### Breaking Changes
- **Framework**: Migrated from AutoGen to AG2
- **Dependencies**: Removed LangChain, updated to modern libraries
- **Structure**: Consolidated from multiple files to single `agentcy.py`
- **Configuration**: New environment-based configuration system

### New Capabilities
- AI image generation and critique
- Advanced web scraping with fallbacks
- Professional marketing frameworks
- Organized output structure
- Enhanced error handling

### Migration Steps
1. **Security First**: If you have an existing `OAI_CONFIG_LIST` with exposed API keys, revoke those keys immediately
2. Install new dependencies: `uv install`
3. Set up secure configuration using `.env` file (recommended)
4. Use `python agentcy.py` instead of `python main.py`

### Configuration Options
- **Recommended**: Use `.env` file for all API keys (more secure, easier to manage)
- **Alternative**: Keep existing `OAI_CONFIG_LIST` file (ensure it's in `.gitignore`)

## 📈 Roadmap

### Completed in 2.0 ✅
- [x] Modernize to AG2 framework
- [x] Remove LangChain dependency
- [x] Consolidate codebase into single file
- [x] Add visual content generation
- [x] Implement professional frameworks
- [x] Enhanced research capabilities
- [x] Organized output structure
- [x] Production-ready error handling

### Future Enhancements 🔮
- [ ] Local LLM support (Ollama integration)
- [ ] Web-based UI for project management
- [ ] Template system for different industries
- [ ] Integration with design tools (Figma, Adobe)
- [ ] Performance analytics and optimization
- [ ] Multi-language support
- [ ] Custom agent training workflows
- [ ] API endpoints for programmatic access

## 📝 License 

MIT License. See [LICENSE](https://opensource.org/license/mit/) for more information.
