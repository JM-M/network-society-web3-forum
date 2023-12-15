# Attestation-Gated Forum Template

A template for setting up attestation-gated decentralized forums built with Ceramic (using ComposeDB), Orbis SDK, and Hololym. 

## Getting Started (to be updated)

1. Duplicate the existing .env.example file and rename it `.env`

2. Install your dependencies:

```bash
npm install
```

3. Create your author key (this will be your server's static seed phrase to write attestations to your ComposeDB instance). Copy-paste the resulting string into your `AUTHOR_KEY` field in your .env file:

```bash
npm run author
```

4. Generate your Ceramic admin seed, DID, and ComposeDB configuration file. Copy-paste the resulting string found in your admin_seed.txt file into your `SEED` field in your .env file:

```bash
npm run generate
```

5. Create your Orbis project and context from the command line (follow the prompts in your terminal):

```bash
npm run generateOrbis
```

After you've completed the series of prompts, you will see a log note that says "This is your parent context: ". Copy the value starting with a "k" and paste it into your `ORBCONTEXT` field in your .env file. Finally, locate your file found at /pages/_app.js and paste the same value for the corresponding constants: 

`global.orbis_context`
`global.orbis_chat_context`

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Styles

Most of the colors can be updated in the `styles/global.css` file which contains CSS variables applied to the main `html` property.


