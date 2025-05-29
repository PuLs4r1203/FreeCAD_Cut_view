# FreeCAD Macro: Create Cutviews for Assemblies and Parts

This FreeCAD macro automates the creation, management, and deletion of "cut views" for assemblies and parts.  
It is designed for advanced workflows, supporting both single parts and complex assemblies (including links and nested structures).  
**Compatible with both the Part and PartDesign workbenches.**

---

> 🇩🇪 [German version](README.de.md)

---

## Features

- **Automatic creation of cut views** for single bodies or entire assemblies
- **Qt-based user dialog** for easy interaction (choose section letter and rectangle size)
- **Delete existing cut-view groups** using a dedicated dialog
- Works with both simple parts and nested assemblies (with Links)
- Supports both **Part** and **PartDesign** objects

---

## How to Use

### 1. Preparation

- Open your desired FreeCAD document.
- Select either:
  - a body or assembly **and** a cutting plane to create a new cut view, or
  - an existing cutview group to delete it.

> **MARKER_IMAGE1**  
> *(Insert screenshot of initial selection here)*

---

### 2. Creating a New Cut View

1. **Select object and plane:**  
   In the model tree, select a body/assembly and an existing plane (DatumPlane/Plane).
2. **Run the macro:**  
   A dialog will appear. Choose a letter for the section label and the rectangle size (for the cut cube).
3. **Confirm your choices:**  
   The macro will automatically generate sub-links and the corresponding cut cubes, and perform the cutting operation.

> **MARKER_IMAGE2**  
> *(Insert screenshot of the dialog here)*

---

### 3. Deleting an Existing Cutview

- Select a group in the model tree whose name starts with `Cut_` (e.g., `Cut_A`).
- Run the macro again.  
  A dialog will open, giving you the option to delete the entire group.

> **MARKER_IMAGE3**  
> *(Insert screenshot of delete dialog here)*

---

## Notes & Tips

- Coplanar faces at the cut will be **highlighted in dark red** to improve visibility.
- Objects are automatically grouped under main and subgroups for clarity.
- Works with both individual parts and complex assemblies with nested structures and links.

> **MARKER_IMAGE4**  
> *(Insert screenshot of a finished cut view here)*

---

## Installation

1. Copy `ZZZZ_Create_Cutviews_ASM.FCMacro` into your FreeCAD macros folder.
2. Start FreeCAD and execute the macro via the Macro Manager.

---

## Requirements

- FreeCAD (latest version recommended)
- Part and/or PartDesign workbenches enabled
- For assemblies: an assembly workbench (A2plus, Assembly3, etc.) if required

---

## License

This macro is provided under the MIT license.

---

## Support / Questions

For issues or suggestions, please open an issue in the [GitHub repository](https://github.com/PuLs4r1203/FreeCAD_Cut_view).
