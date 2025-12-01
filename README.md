# JobTech Search Application

This project was developed as a school project at Medieinstitutet. A client-side Job Search Application built with React and TypeScript. It allows users to browse job advertisements from Arbetsförmedlingen, view detailed information, and save interesting jobs.

The core objective of this assignment was to work with component libraries, specifically implementing Arbetsförmedlingen's official design system (`@digi/arbetsformedlingen`), with the ambition of creating a smoother and more intuitive user experience than the existing platform.

State regarding saved jobs and recent searches is persisted to localStorage, ensuring that user preferences survive page reloads. The main focus lies in state management, routing, and design system integration.

## 📋 Project overview

The app fetches job ad data from the external JobTech API and manages user preferences locally. It consists of:

- **Home Page** – Search interface with filtering options.
- **Jobs Page** – List of search results.
- **Job Details Page** – Detailed view of specific job advertisements.

Users can:

- **Search for jobs** using keywords.
- **Filter results** by Region, Municipality, and Occupation.
- **View detailed descriptions** and application info for each job.
- **Save jobs**: Bookmark ads for later viewing.
- **View recent searches**: Quickly access previous search terms.

## ✨ Features

- **API Integration**: Fetches job data from `https://jobsearch.api.jobtechdev.se/search`.
- **Local Persistence**:
  - Saves bookmarked jobs to localStorage (`savedJobs`).
  - Saves search history to localStorage (`recentSearches`).
- **Search & Filtering**:
  - Free text search.
  - Filter by Geographic location (Region/Municipality).
  - Filter by Occupation (Field/Group).
- **Visual Feedback**: Loading states and responsive layout.
- **Routing**: Uses React Router for navigation between search, list, and detail views.
- **Responsive UI**: Built with TailwindCSS for a mobile-friendly design.

## 🧰 Tech Stack

- React
- TypeScript
- TailwindCSS
- Vite
- @digi/arbetsformedlingen (Design System)
- NPM
- ESLint
- Prettier

## 🚀 Installation

### Prerequisites

- Node.js 18+
- npm, pnpm, or yarn

### Install dependencies

```bash
npm install
```

### Run the App

```bash
npm run dev
```
