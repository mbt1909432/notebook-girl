<div align="center">
  <h1 align="center">Notebook Girl · AI Note Assistant</h1>
  <p align="center">
    <strong>A PPT-style slide generator experience built on the Acontext Agent Playground template</strong>
  </p>
  <p align="center">
    Powered by <a href="https://acontext.io"><strong>Acontext</strong></a>
  </p>
  
  <p align="center">
    <img src="https://img.shields.io/badge/Next.js-15+-000000?style=for-the-badge&logo=next.js&logoColor=white" alt="Next.js" />
    <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
    <img src="https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white" alt="Supabase" />
    <a href="https://acontext.io"><img src="https://assets.memodb.io/Acontext/badge-made-with-acontext.svg" alt="Made with Acontext" /></a>
  </p>
  
  <p align="center">
    <img src="./public/fonts/character1/ppt%20girl.png" alt="Notebook Girl - Homepage Character" width="300" />
    &nbsp;&nbsp;&nbsp;
    <img src="./public/fonts/character1/ppt_girl_chatbot.png" alt="Notebook Girl - Chatbot Avatar" width="200" />
  </p>
</div>

<br/>

## 📸 Gallery

<div align="center">
  <img src="./public/fonts/promotion/1.png" alt="Promotion 1" width="100%" />
  <br/><br/>
  <img src="./public/fonts/promotion/2.png" alt="Promotion 2" width="100%" />
  <br/><br/>
  <img src="./public/fonts/promotion/3.png" alt="Promotion 3" width="100%" />
  <br/><br/>
  <img src="./public/fonts/promotion/4.png" alt="Promotion 4" width="100%" />
  <br/><br/>
  <img src="./public/fonts/promotion/5.png" alt="Promotion 5" width="100%" />
  <br/><br/>
  <img src="./public/fonts/promotion/6.png" alt="Promotion 6" width="100%" />
</div>

<br/>

**Notebook Girl · AI Note Assistant** is an intelligent note generation system powered by [Acontext](https://acontext.io). Simply chat with **"Notebook Girl"** about your content, and she will automatically create beautiful, structured note pages ready for study or reference.

## 🎯 What It Does

Transform content into structured notes through natural conversation:

1. **Input**: Provide content (text, topics, or outlines)
2. **Planning**: Notebook Girl proposes a structured note outline
3. **Review**: Confirm the outline
4. **Generation**: Notebook Girl generates 16:9 note page images
5. **Delivery**: Notes are automatically stored and accessible via URLs

## ✨ Key Features

- **🎨 AI-Powered Generation**: Natural language conversation to create structured notes
- **🎨 Consistent Visual Style**: Unified aesthetic across all note pages
- **💾 Persistent Memory**: Remembers your previous notes and preferences across sessions
- **🔍 Semantic Search**: Automatically maintains style consistency
- **📦 Automatic Storage**: All notes stored in Acontext Disk with shareable URLs
- **🔄 Interactive Workflow**: Review outlines before generation, iterate on specific notes

## 🛠️ Tech Stack

- **Framework**: Next.js 15+ (App Router)
- **Authentication**: Supabase
- **AI Platform**: Acontext
- **LLM**: OpenAI (compatible API)
- **UI**: Tailwind CSS, shadcn/ui

## 📦 Getting Started

### Prerequisites

- Node.js 18+ and npm/yarn/pnpm
- A [Supabase account](https://database.new)
- An [Acontext account](https://acontext.io)
- An OpenAI API key

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/mbt1909432/notebook-girl.git
cd notebook-girl
```

2. **Install dependencies**

```bash
npm install
```

3. **Set up Supabase**

   - Create a new project at [Supabase Dashboard](https://database.new)
   - Note your `Project URL` and `Anon (publishable) key`

4. **Configure environment variables**

   Create a `.env.local` file:

```env
# Supabase (required)
NEXT_PUBLIC_SUPABASE_URL=your-supabase-project-url
NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY=your-supabase-publishable-or-anon-key

# Acontext (required)
ACONTEXT_API_KEY=your-acontext-api-key
ACONTEXT_BASE_URL=https://api.acontext.com/api/v1

# OpenAI LLM (required)
OPENAI_LLM_ENDPOINT=https://api.openai.com/v1
OPENAI_LLM_API_KEY=your-openai-api-key
OPENAI_LLM_MODEL=gpt-4o-mini
OPENAI_LLM_TEMPERATURE=0.7
OPENAI_LLM_MAX_TOKENS=2000

# Image Generation (optional, for slide generation)
IMAGE_GEN_API_KEY=your-image-gen-api-key
IMAGE_GEN_BASE_URL=https://api.openai-next.com
IMAGE_GEN_DEFAULT_MODEL=gemini-3-pro-image-preview

```

5. **Set up database schema**

   - Open your Supabase project → **SQL Editor**
   - Run SQL from `specs/001-chatbot-openai/schema.sql`
   - Run `specs/001-chatbot-openai/migration-acontext.sql`
   - Run `specs/001-chatbot-openai/migration-acontext-disk.sql`
   - Run `specs/001-chatbot-openai/migration-acontext-space-user.sql`

6. **Run the development server**

```bash
npm run dev
```

Visit `http://localhost:3000` to see your application.

## 🚢 Deployment

### Deploy to Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fmbt1909432%2Fnotebook-girl&ref=main&project-name=notebook-girl&repository-name=notebook-girl&demo-title=Acontext%20Notebook%20Girl%20AI%20Note%20Assistant&demo-description=AI-powered%20note%20assistant%20powered%20by%20Acontext%2C%20with%20chat-driven%20workflow%20and%20semantic%20memory.&demo-url=https%3A%2F%2Fnotebook-girl.vercel.app)

1. Click the "Deploy with Vercel" button above
2. Vercel will guide you through Supabase setup
3. Add remaining environment variables in Vercel dashboard (see `.env.local` above)
4. After deployment, run database migrations in Supabase SQL Editor

## 🔧 Available Tools

- **Acontext Disk Tools** - File system operations (`write_file`, `read_file`, `list_artifacts`, etc.)
- **Todo Management** (`todo`) - Create and manage todos within chat sessions
- **Image Generation** (`image_gen`) - Generate slide images

## 📚 Documentation

- Project docs: `public/fonts/skills/README.md`, `docs/`
- [Acontext Documentation](https://docs.acontext.io)
- [Next.js Documentation](https://nextjs.org/docs)
- [Supabase Documentation](https://supabase.com/docs)

## 🤝 Contributing

This is a starter template - feel free to fork and customize it for your needs!

## 📄 License

Check the LICENSE file in the repository.

## 🆘 Support

- **Acontext**: [Documentation](https://docs.acontext.io) | [Support](https://acontext.io)
- **Issues**: Open an issue in the repository

---

**Built with ❤️ using Acontext Platform**
