# Shelf.nu — MAD BIRD STUDIOS

<p align="center">
  <img width="100%" src="./apps/webapp/public/static/images/readme-cover.jpg" alt="Shelf.nu Asset Management Platform" />
</p>

<h3 align="center">Open-source asset management infrastructure for everyone.</h3>

<p align="center">
  Developed by <strong>MAD BIRD STUDIOS</strong>
</p>

Shelf.nu is an asset management platform for tracking physical assets, including equipment, devices, tools, vehicles, props, and inventory. It helps teams manage assets across locations, track bookings, assign custody, and organize inventory with role-based access controls.

## Features

- **QR Asset Tags** — Generate and print QR codes to identify and access asset information.
- **Bookings and Reservations** — Schedule equipment usage and manage checkout and return dates.
- **Custody Tracking** — Assign assets to team members and track responsibility.
- **Location Management** — Organize assets by buildings, floors, rooms, and storage locations.
- **Team Roles** — Manage organization access using role-based permissions.
- **Custom Fields** — Store metadata such as serial numbers, purchase dates, and warranty information.
- **Categories and Tags** — Organize and classify assets.
- **Kits** — Group related assets and manage them together.
- **Search and Filtering** — Find assets using search and advanced filters.
- **CSV Import and Export** — Import asset data in bulk and export reports.
- **Asset Reminders** — Schedule reminders for maintenance and warranty dates.
- **Audit Trail** — Track asset activities, notes, and changes.
- **Multi-workspace Support** — Manage inventory across organizations and departments.
- **QR and Barcode Scanner** — Scan assets and perform supported inventory actions.

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | React Router 7, React 19 |
| Language | TypeScript |
| Database | PostgreSQL via Supabase |
| ORM | Prisma |
| Styling | Tailwind CSS |
| Components | Radix UI |
| Authentication | Supabase Auth |
| Job Queue | pg-boss |
| Payments | Stripe |
| Email | Nodemailer |
| Build Tools | Vite, Turborepo |
| Testing | Vitest, Playwright |

Refer to the relevant configuration files in this repository to confirm the exact installed versions.

## Getting Started

### Prerequisites

- Node.js version required by the repository
- pnpm version required by the repository
- A configured Supabase project
- Git

Check the project's `package.json`, `packageManager` field, and documentation for the required tool versions.

### Installation

Clone this repository:

```bash
git clone https://github.com/imhari63/shelf.nu.git
cd shelf.nu
```

Install dependencies:

```bash
pnpm install
```

Create your local environment file using the provided template, if available:

```bash
cp .env.example .env
```

On Windows PowerShell, you can use:

```powershell
Copy-Item .env.example .env
```

Configure the required environment variables using the project's documentation. Never commit real API keys, database passwords, or other secrets.

### Database Setup

After configuring Supabase and the required environment variables, run the repository's setup command:

```bash
pnpm webapp:setup
```

### Start Development

```bash
pnpm webapp:dev
```

Check the terminal output for the local application URL and any required HTTPS certificate setup.

**Note:** These commands are based on the existing project documentation. Successful startup depends on your environment configuration and the current repository state.

## Project Structure

```text
shelf.nu/
├── apps/
│   ├── webapp/       # Main web application
│   ├── companion/    # Companion mobile application
│   └── docs/         # Documentation site
├── packages/
│   └── database/     # Database schema and migrations
├── tooling/          # Shared development configuration
├── package.json
├── pnpm-workspace.yaml
└── turbo.json
```

The project uses pnpm workspaces and Turborepo to manage its monorepo structure.

## Development Commands

| Command | Description |
|---|---|
| `pnpm webapp:dev` | Start the web application |
| `pnpm webapp:build` | Build the web application |
| `pnpm webapp:test` | Run web application tests |
| `pnpm webapp:validate` | Run project validation |
| `pnpm webapp:setup` | Set up the database client and migrations |
| `pnpm typecheck` | Run TypeScript checks |
| `pnpm lint` | Run ESLint |
| `pnpm docs:dev` | Start the documentation site |

Run commands from the repository root. Verify available scripts in `package.json` before relying on them.

## Deployment

Deployment depends on the required database, authentication, environment variables, and hosting configuration.

Before deploying:

1. Configure production environment variables.
2. Set up the database and apply the required migrations.
3. Run the available validation and build scripts.
4. Configure your hosting platform.
5. Verify authentication, storage, and application functionality.

Do not assume the original project's deployment pipeline is configured for this repository.

## Documentation

- [Shelf.nu Documentation](https://docs.shelf.nu/)
- [Local Development Guide](https://docs.shelf.nu/local-development)
- [Supabase Setup](https://docs.shelf.nu/supabase-setup)
- [Deployment Guide](https://docs.shelf.nu/deployment)
- [Docker Guide](https://docs.shelf.nu/docker)
- [Contributing Guide](./CONTRIBUTING.md)

Some documentation links describe the upstream project and may need to be adapted to this customized repository.

## License and Attribution

This repository is based on the Shelf.nu project.

The upstream project identifies its main application as licensed under **GNU Affero General Public License v3.0 (AGPL-3.0)**, with a separate license for the companion mobile application in `apps/companion/`.

- Preserve the original copyright notices and required license files.
- Review the root `LICENSE` and `apps/companion/LICENSE` before modifying or redistributing the project.
- Follow all applicable license conditions when publishing modified source code or offering the application as a network service.
- Do not replace the original copyright ownership with MAD BIRD STUDIOS or imply that MAD BIRD STUDIOS created the original upstream software.

MAD BIRD STUDIOS branding and modifications do not change the upstream license obligations.

For the binding terms, refer to the license files included in this repository.

## Maintained By

**MAD BIRD STUDIOS**

A digital creative studio working across design, web development, branding, video editing, and SEO.

- GitHub: [@imhari63](https://github.com/imhari63)
- Repository: [shelf.nu](https://github.com/imhari63/shelf.nu)

---

<p align="center">
  Customized and maintained by MAD BIRD STUDIOS.
</p>
