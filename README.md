# Generative AI Fitness Platform
A full-stack, voice-driven AI fitness coach that generates personalized workout and diet plans through a conversational interface.

## Overview
This project is a modern, full-stack web application that acts as a personal AI fitness and nutrition coach. Users can interact with a conversational voice assistant to describe their fitness goals, physical attributes, limitations, and dietary preferences. Leveraging the power of Google's Gemini AI, the platform processes this information to generate deeply personalized workout routines and meal plans in real-time.

The application is built with a serverless-first approach, featuring a responsive, futuristic UI and a secure, scalable backend architecture.

### Keyfeature

 **-Conversational Voice AI:** Engage in a natural conversation with a voice assistant powered by Vapi to provide your fitness requirements.

 **-Intelligent Plan Generation:** Utilizes Google Gemini to create tailored workout and diet plans based on user-specific data like age, weight, goals, and injuries.

 **Secure Authentication:** Full user authentication and management system handled by Clerk, including social sign-on and protected routes.

 **Real-time Database:** Built on Convex, a serverless platform providing a real-time database, server functions, and file storage.

 **User Profile & Plan Management:** Users can view their active and past fitness plans on a dedicated profile page.

 **Modern Tech Stack:** Built with Next.js 15, React, and TypeScript for a type-safe, performant, and scalable application.

 **Cyberpunk UI:** A sleek, responsive user interface styled with Tailwind CSS and Shadcn/ui, featuring custom animations and a futuristic aesthetic.

 **Serverless Functions & Webhooks:** Backend logic is handled through Convex functions, including a webhook endpoint to sync user data from Clerk.

## Tech Stack

  **FRONTEND      --**         Next.js, React, TypeScript
  **Backend       --**         Convex (Serverless Node.js Platform)
  **AI/LLM        --**         Google Gemini
  **Voice AI      --**         Vapi
  **AUthentication--**         Clerk
  **Styling       --**         Tailwind CSS, Shadcn/ui, Radix UI
  **Icons         --**         Lucide React
  
### Getting Started
Follow these steps to set up and run the project locally.

*Prerequisites*

--Node.js (v18.18 or later)

--npm or any other package manager

--A Convex account (for database and backend)

--A Clerk account (for authentication)

--A Vapi account (for the voice assistant)

--A Google AI Studio API key (for Gemini)

** Clone the Repository **
```
git clone [https://github.com/YOUR_USERNAME/Generative-AI-Fitness-Platform.git](https://github.com/YOUR_USERNAME/Generative-AI-Fitness-Platform.git)
cd Generative-AI-Fitness-Platform
```

**Install Dependencies**
```
  npm install
```
**Set Up Environment Variables**
--Create a .env.local file in the root of the project and add the following environment variables. Obtain these keys from their respective service dashboards.

```
# Clerk Authentication ([https://dashboard.clerk.com](https://dashboard.clerk.com))
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=
CLERK_WEBHOOK_SECRET=

# Vapi Voice AI ([https://dashboard.vapi.ai](https://dashboard.vapi.ai))
NEXT_PUBLIC_VAPI_API_KEY=

# Google Gemini AI ([https://aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey))
GEMINI_API_KEY=

# Convex Backend ([https://dashboard.convex.dev](https://dashboard.convex.dev))
NEXT_PUBLIC_CONVEX_URL=
CONVEX_DEPLOYMENT=
```
**Set Up Convex Backend**
--Initialize Convex and push the database schema. Follow the prompts after running the first command.
```
npx convex dev
```
--This command will watch for changes in your convex/ directory and automatically update your backend. It will also generate the necessary files in convex/_generated/.

** Run the Development Server**
```
npm run dev
```
--Open http://localhost:3000 in your browser to see the application running.

## Deployment

--This application is optimized for deployment on Vercel.

   Push your code to a GitHub repository.

   Connect your repository to a new Vercel project.
 
   Add the same environment variables from your .env.local file to the Vercel project settings.

   Deploy! Vercel will automatically build and deploy your application.

  ## Project Strucutre
```
Generative-AI-Fitness-Platform/
├── .git/
├── .gitignore
├── convex/
│   ├── _generated/
│   │   ├── api.d.ts
│   │   ├── api.js
│   │   ├── dataModel.d.ts
│   │   ├── server.d.ts
│   │   └── server.js
│   ├── auth.config.ts
│   ├── http.ts
│   ├── plans.ts
│   ├── schema.ts
│   └── users.ts
├── public/
│   ├── ai-avatar.png
│   ├── hero-ai.png
│   ├── hero-ai2.jpg
│   ├── hero-ai3.png
│   └── screenshot-for-readme.png
├── src/
│   ├── app/
│   │   ├── (auth)/
│   │   │   ├── sign-in/
│   │   │   │   └── [[...sign-in]]/
│   │   │   │       └── page.tsx
│   │   │   └── sign-up/
│   │   │       └── [[...sign-up]]/
│   │   │           └── page.tsx
│   │   ├── generate-program/
│   │   │   └── page.tsx
│   │   ├── profile/
│   │   │   └── page.tsx
│   │   ├── favicon.ico
│   │   ├── globals.css
│   │   ├── layout.tsx
│   │   └── page.tsx
│   ├── components/
│   │   ├── ui/
│   │   │   ├── accordion.tsx
│   │   │   ├── button.tsx
│   │   │   ├── card.tsx
│   │   │   └── tabs.tsx
│   │   ├── CornerElements.tsx
│   │   ├── Footer.tsx
│   │   ├── Navbar.tsx
│   │   ├── NoFitnessPlan.tsx
│   │   ├── ProfileHeader.tsx
│   │   ├── TerminalOverlay.tsx
│   │   └── UserPrograms.tsx
│   ├── constants/
│   │   └── index.ts
│   ├── lib/
│   │   ├── utils.ts
│   │   └── vapi.ts
│   ├── providers/
│   │   └── ConvexClerkProvider.tsx
│   └── middleware.ts
├── components.json
├── eslint.config.mjs
├── LICENSE
├── next.config.ts
├── package-lock.json
├── package.json
├── postcss.config.mjs
├── README.md
└── tsconfig.json

```

## Future Advancements
  ### Progress Tracking & Analytics:--### Implement features for users to log workout performance (sets, reps, weight) and daily meals. Visualize this data through charts and graphs to track strength gains, weight changes, and caloric intake over time.
  AI Feedback Loop: Enhance the AI to provide dynamic plan adjustments based on logged data. The assistant could proactively suggest increasing weight, modifying exercises, or altering diet based on user performance and feedback.
  Exercise Library with Demonstrations: Create a comprehensive library of exercises with video demonstrations to ensure users maintain proper form, maximizing effectiveness and minimizing injury risk.
  Wearable Device Integration: Integrate with health APIs from services like Apple HealthKit or Google Fit to automatically sync workout data, activity levels, and biometric information, providing the AI with a richer dataset for more accurate recommendations.
  Community & Social Sharing: Introduce features allowing users to share their fitness plans and progress with friends or the community, fostering motivation and accountability.

 
 

