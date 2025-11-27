# Minecraft Bedrock Add-on Template

> [!IMPORTANT]
> This template is intended for development on Windows or Linux.
> If you are developing on mobile, please look elsewhere.

Feel free to use this template! No credit is required.

Key points:

- 📂 Both the behavior pack and the resource pack reside in the same "project folder"
- 🛡️ Your project folder can be located outside of the potentially dangerous `com.mojang` folder
- ⚡ One command to build (compile) the packs and copy them into the `com.mojang` folder
- ☑️ TypeScript is supported out of the box
- 📦 Easy integration of external packages through npm

Details are explained below.

## Prerequisites

Please install these tools on your system before proceeding:

- [Git](https://git-scm.com/install/)
- [Node.js](https://nodejs.org/) (v22 or later)
- [pnpm](https://pnpm.io/installation)

## Key concepts explained

### Project Folder

Most add-on developers store their packs directly in the `development_behavior_packs` (and/or
`development_resource_packs`) folder inside the `com.mojang` folder.

Packs that belongs to the same project, exist in separate locations and mixed with others.
Which can be quite inconvenient if:

- You hop between packs a lot - _have you ever opened two code editor windows for one project?_
- You want to use Git to manage both packs in a single repository

Plus, storing development data in such internal locations is not a very good idea.
Minecraft might (accidentally) delete your work during an update! 😱

**The "Project Folder" approach can solve this problem.**

The project folder is the single, top-level directory that acts as the centralized workspace for an
add-on, containing both packs and their source code, resources, and build configurations.

Main benefits:

- There's no longer a need to open two code editor windows (one for BP and one for RP)
- Git integration is finally possible
- Isolated from deep hidden locations like the `com.mojang` folder
