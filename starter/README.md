<!-- PROJECT LOGO -->
<p align="center">
  <a href="https://github.com/calcom/cal.com">
   <img src="https://user-images.githubusercontent.com/8019099/210054112-5955e812-a76e-4160-9ddd-58f2c72f1cce.png" alt="Logo">
  </a>

  <h3 align="center">Cal.com Platform Starter Kit</h3>

  <p align="center">
    Build your pixel-perfect booking experience
    <br />
    <a href="https://experts.cal.dev"><strong>Demo</strong></a>
    <br />
    <a href="https://cal.com/docs/platform"><strong>Docs</strong></a>
    <br />
    <br />
    <a href="https://go.cal.com/discord">Discord</a>
    ·
    <a href="https://cal.com/platform">Website</a>
    ·
    <a href="https://github.com/calcom/cal.com/issues">Issues</a>
  </p>
</p>

# Platform Starter Kit Example

Cal.com Platform Starter Kit showcases the new Cal.com Platform API and Cal.com Atoms. It was built using the [T3 Stack](https://create.t3.gg/).

## Deploy your own

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fcalcom%2Fexamples%2Fblob%2Fmain%2Fstarter&env=TURSO_DATABASE_URL,TURSO_AUTH_TOKEN,AUTH_SECRET,AUTH_TRUST_HOST,NEXT_PUBLIC_CAL_OAUTH_CLIENT_ID,NEXT_PUBLIC_CAL_API_URL,NEXT_PUBLIC_REFRESH_URL,CAL_SECRET&envDescription=API%20Keys%20for%20the%20database%20(turso)%2C%20authentication%20(nextauth)%20and%20Cal.%20*Note*%3A%20You%20can%20copy%20%26%20paste%20the%20cal-specific%20env%20vars%20from%20our%20demo%20under%20the%20provided%20link&envLink=https%3A%2F%2Fgithub.com%2Fcalcom%2Fexamples%2Fblob%2Fmain%2Fstarter%2F.env.example%23L24-L35&project-name=cal-platform-starter&repository-name=cal-platform-starter&demo-title=Cal%20Platform%20Starter&demo-description=A%20marketplace%20to%20book%20experts.%20Scheduling%20is%20handled%20by%20%40calcom%2Fatoms.&demo-url=https%3A%2F%2Fstarter-4m7evv7ji-cal-staging.vercel.app%2F&demo-image=https%3A%2F%2Fcal.com%2Ffavicon.ico)

## How to use

**1. Clone the repository**

HTTPS:

 ```bash
 git clone https://github.com/calcom/examples.git
 ```

 GitHub CLI:

 ```bash
 gh repo clone calcom/examples
 ```

**2. Move into the Starter**

```bash
cd examples/starter
```

**3. Install dependencies**

PNPM:

```bash
pnpm install
```

NPM:

```bash
npm install
```

YARN:

```bash
yarn install
```

BUN:

```bash
bun install
```

**4. Set Environment Variables**

   We provide most environment variables out of the box (including  Cal-related variables).

   So get started by copying the `.env.example`:

   ```bash
   cp .env.example .env
   ```

   *4.1 Database*

   This project uses SQLite with Turso. You can create one for free at [turso.tech](https://turso.tech/).

   Then, get the URL and Access Token from the Turso dashboard and update the respective values in your `.env` file:

   ```.env
   # Prisma (Turso Database from https://turso.tech/app)
   # https://www.prisma.io/docs/orm/overview/databases/turso
   TURSO_DATABASE_URL="libsql://<your-database-name>.turso.io"
   TURSO_AUTH_TOKEN="eyJhbGc****"
   ```

   *4.2 Authentication*

   Generate a NextAuth secret and add it to your `.env.` file:

   ```bash
   openssl rand -hex 32
   ```

   ```.env
   # Next Auth
   # You can generate a new secret on the command line with
   # openssl rand -base64 32
   # <https://next-auth.js.org/configuration/options#secret>
   
   AUTH_SECRET="SQhGk****"
   ```

   *4.3 Cal*

   For **development**, you're all set! We've provided you with our sandbox keys that you can find the `.env.example` file.

   For **production**, keep in mind that you'll have to update the `NEXT_PUBLIC_REFRESH_URL` variable to make it point to your deployment, e.g.:

   ```.env
   # 3/ *REFRESH URL.* You have to expose an endpoint that will be used from calcom: https://cal.com/docs/platform/quick-start#4.-backend:-setting-up-refresh-token-endpoint

   NEXT_PUBLIC_REFRESH_URL="https://<your-project>.vercel.app/api/cal/refresh"
   ```

**5. Development Server**
   From here, you're all set. Just start the development server & get going.
   **PNPM**

```bash
pnpm dev
```

**NPM**

```bash
npm dev
```

**YARN**

```bash
yarn dev
```

**BUN**

```bash
bun dev
```

## What's next? How do I make an app with this?

We try to keep this project as simple as possible, so you can start with Cal.com Platform and the scaffolding we set up for you, and add additional things later when they become necessary.

If you are not familiar with the different technologies used in this project, please refer to the respective docs.

- [Cal.com Platform](https://cal.com/platform)
- [Next.js](https://nextjs.org)
- [NextAuth.js](https://next-auth.js.org)
- [Prisma](https://prisma.io)
- [Tailwind CSS](https://tailwindcss.com)
- [tRPC](https://trpc.io)

## Learn More about Cal.com Platform

Visit our documentation at [cal.com/docs/platform](https://cal.com/docs/platform) or join our [Discord](https://go.cal.com/discord).

Contact sales to purchase a commercial API key here: [cal.com/sales](https://cal.com/sales).

## Learn More about T3

To learn more about the [T3 Stack](https://create.t3.gg/), take a look at the following resources:

- [Documentation](https://create.t3.gg/)
- [Learn the T3 Stack](https://create.t3.gg/en/faq#what-learning-resources-are-currently-available) — Check out these awesome tutorials

You can check out the [create-t3-app GitHub repository](https://github.com/t3-oss/create-t3-app) — your feedback and contributions are welcome!