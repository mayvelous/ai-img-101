# Fullstack AI Image Generation

Image gallery site using MERN stack, OpenAI Apis (DALL-E model), Cloudinary and TailwindCSS.
Following this [tute](https://www.youtube.com/watch?v=EyIvuigqDoA).

# Setup

## Client

- Install Vite > React > JS variant
- Install TailwindCSS

```
npm create vite@latest ./
npm install

npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p

npm run dev
```

## Server

```
npm init -y
npm install cloudinary cors dotenv express mongoose nodemon openai

npm start
```

## .env

- Add .env file to `server` root
- Create mongodb database [here](https://www.mongodb.com/atlas/database) and add the connection url variable `MONGODB_URL`
- Grab OpenAi api key from [here](https://beta.openai.com/account/api-keys) and add as `OPENAI_API_KEY`
- Also add respective cloudinary variables

  - CLOUDINARY_CLOUD_NAME
  - CLOUDINARY_API_KEY
  - CLOUDINARY_API_SECRET

- Add `.env` and `.env.local` file to `client` root
- Add `VITE_SERVER_BASEURL="http://server:8080"` to .env.local file

### Note

To use `.env` vars in `Client Vite` app, prefix variables with `VITE_`, read more [here](https://vitejs.dev/guide/env-and-mode.html#env-files) and call it as `import.meta.env.VITE_SOME_VAR`
