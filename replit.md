# Qera's Smart Assistant - CV Builder

## Overview
Qera's Smart Assistant is a professional CV builder web application that helps candidates create polished, ATS-friendly CVs in minutes through a guided question-based approach.

## Project Architecture

### Tech Stack
- **Frontend**: React, TypeScript, Tailwind CSS, Shadcn UI
- **Backend**: Express.js, Node.js
- **Document Generation**: jsPDF (PDF), docx (DOCX)
- **Storage**: In-memory storage (MemStorage)
- **Routing**: Wouter
- **Forms**: React Hook Form with Zod validation
- **State Management**: TanStack Query

### Key Features
1. **Multi-step CV Builder**: Guided form with 6 steps (Personal Info, Experience, Education, Skills, Template Selection, Preview)
2. **5 Professional Templates**: Accountant, HR Generalist, Executive, Office Manager, Creative
3. **Document Export**: Download CVs in PDF or DOCX format
4. **Responsive Design**: Mobile-first approach with beautiful UI
5. **Dark Mode**: Full dark mode support with theme toggle
6. **Form Validation**: Client-side validation with clear error messages

### Project Structure
```
client/
  src/
    components/
      builder/           # CV builder step components
      ui/               # Shadcn UI components
      Header.tsx        # Global header with navigation
      Footer.tsx        # Global footer
      ProgressSteps.tsx # Multi-step progress indicator
      CVPreview.tsx     # CV preview component
    pages/
      Home.tsx          # Landing page
      CVBuilder.tsx     # Main CV builder page
      Templates.tsx     # Template gallery page
    data/
      templates.ts      # CV template definitions
server/
  utils/
    pdfGenerator.ts   # PDF generation logic
    docxGenerator.ts  # DOCX generation logic
  routes.ts           # API endpoints
  storage.ts          # Data storage interface
shared/
  schema.ts           # Shared TypeScript types and Zod schemas
```

### API Endpoints
- `POST /api/cvs` - Create/save CV data
- `GET /api/cvs/:id` - Get CV by ID
- `POST /api/cvs/generate-pdf` - Generate PDF document
- `POST /api/cvs/generate-docx` - Generate DOCX document

### Color Scheme
- **Primary**: Professional blue (217 91% 60%)
- **Success**: Green for completion states (142 76% 36%)
- **Background**: Pure white (light) / Dark gray (dark)
- **Text**: Near black (light) / Light gray (dark)

### Design Philosophy
- Professional and trustworthy appearance
- Clean, modern aesthetic inspired by Canva and Material Design
- Smooth animations and transitions
- Accessible and inclusive design
- Mobile-responsive with progressive enhancement

## Development

### Running the Application
```bash
npm run dev
```
This starts both the Express backend and Vite frontend on the same port.

### Building for Production
```bash
npm run build
```

## User Journey
1. **Landing Page**: User learns about the CV builder and clicks "Get Started"
2. **Personal Info**: Enter name, title, contact details, and summary
3. **Experience**: Add work history with job titles, companies, dates, and descriptions
4. **Education**: Add educational background with degrees, schools, and dates
5. **Skills**: Add skills, references, and activities
6. **Template Selection**: Choose from 5 professional templates
7. **Preview & Download**: Review CV and download as PDF or DOCX

## Recent Changes
- Initial implementation with complete MVP features
- All 6 steps of CV builder fully functional
- PDF and DOCX generation working
- Beautiful, responsive UI following design guidelines
- Dark mode support
- Form validation and error handling
