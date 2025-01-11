This project is a modern web application template built with **Next.js**, **Tailwind CSS**, and a variety of utility libraries. It includes **Clerk** for authentication and a fully customizable developer experience.

## Prerequisites

Ensure you have the following installed on your system:

- **Node.js**: Version 16 or newer.
- **npm**: Comes with Node.js.

You can verify the versions by running:

```bash
node -v
npm -v
```

## Getting Started

Follow these steps to set up and run the project.

### 1. Clone the Repository

Clone this repository to your local machine:

```bash
git clone https://github.com/your-username/your-repo-name.git
```

Replace `your-username/your-repo-name` with the appropriate repository URL.

### 2. Navigate to the Project Directory

Navigate to the project folder:

```bash
cd your-repo-name
```

### 3. Install Dependencies

Install the required npm packages:

```bash
npm install
```

### 4. Set Up Environment Variables

Create a `.env.local` file in the root of the project and add the following variables:

```plaintext
NEXT_PUBLIC_CLERK_FRONTEND_API=your-clerk-frontend-api
CLERK_API_KEY=your-clerk-api-key
```

- Replace `your-clerk-frontend-api` with your Clerk frontend API key.
- Replace `your-clerk-api-key` with your Clerk secret API key.

For more details on how to obtain these keys, visit the [Clerk Documentation](https://clerk.dev/docs).

### 5. Run the Development Server

Start the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to see the application.

## Additional Scripts

### Build for Production

To create an optimized production build:

```bash
npm run build
```

### Start the Production Server

After building, you can start the production server:

```bash
npm run start
```

### Linting

To run linting checks using ESLint:

```bash
npm run lint
```

### Format Code

If Prettier is configured, format the codebase:

```bash
npm run format
```

### Clean `.next` Directory

If you encounter issues related to the `.next` folder, you can clean it manually or use a script:

#### Manually
For **Unix/Linux/macOS**:
```bash
rm -rf .next
```

For **Windows** (PowerShell):
```powershell
Remove-Item -Recurse -Force .next
```

#### Using Script
```bash
npm run predev
```

This script clears the `.next` folder automatically before starting the development server.

## Project Structure

- **`pages/`**: Contains all page components.
- **`components/`**: Reusable UI components.
- **`styles/`**: Global and Tailwind CSS files.
- **`public/`**: Static assets.
- **`env.local`**: Environment variables file (not included in the repo).

## Dependencies

### Key Dependencies
- **[Next.js](https://nextjs.org/)**: React framework for server-rendered apps.
- **[Tailwind CSS](https://tailwindcss.com/)**: Utility-first CSS framework.
- **[Clerk](https://clerk.dev/)**: Authentication and user management.
- **[Radix UI](https://www.radix-ui.com/)**: Accessible UI components.

### Dev Dependencies
- **ESLint**: Linting for consistent code.
- **Prettier**: Code formatter.
- **TypeScript**: Static typing.

## Troubleshooting

### Missing `.next/BUILD_ID` Error
This error occurs if the `.next` folder is missing or incomplete. Run the following commands to resolve it:

```bash
npm run predev
npm run build
```

### Missing Environment Variables
Ensure your `.env.local` file contains the required Clerk API keys. If the environment variables are missing, the app may not work as expected.

