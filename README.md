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
Node.js (v18.18 or later)

npm or any other package manager

A Convex account (for database and backend)

A Clerk account (for authentication)

A Vapi account (for the voice assistant)

A Google AI Studio API key (for Gemini)
