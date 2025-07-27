# Shap-E 3D Asset Generation from Text Prompts

This project demonstrates generating 3D assets from text prompts using the **Shap-E** machine learning model by OpenAI. The assets are generated as 3D meshes in **OBJ** format, suitable for game development, 3D visualization, or further editing in 3D software.

---

## Project Overview

- **Goal:** Generate and visualize 3D assets from natural language descriptions using AI.
- **Model Used:** [Shap-E](https://github.com/openai/shap-e), an open-source text-to-3D generation model by OpenAI.
- **Platform:** Google Colab (easy GPU access, no local install required).
- **Outputs:** Four 3D models exported in OBJ format.
- **Use Case:** Useful for game developers, 3D artists, and ML enthusiasts to explore AI-assisted 3D creation.

---

## Repository Structure


```
ShapE-3D-Generation/
├── ShapE_3D_Generation.ipynb     # Main Colab notebook with code and instructions
├── output_assets/                # Folder containing generated 3D assets in OBJ format
│   ├── example_mesh_0.obj
│   ├── example_mesh_1.obj
│   ├── example_mesh_2.obj
│   └── example_mesh_3.obj
└── README.md                     # This documentation file
```

---

## How to Use

### 1. Open and Run the Notebook

- Open [ShapE_3D_Generation.ipynb](./ShapE_3D_Generation.ipynb) in Google Colab or locally via Jupyter.
- The notebook contains step-by-step code to:
  - Clone and install Shap-E.
  - Load the model and diffusion pipeline.
  - Define text prompts to generate assets.
  - Generate and visualize multiple 3D assets.
  - Export generated meshes to OBJ files.

### 2. Modify Prompts

- Edit the `prompts` list in the notebook to generate custom 3D assets from your own descriptions, e.g.:
prompts = [
"a robot",
"a futuristic car",
"a medieval sword",
"a flying drone"
]


### 3. View Outputs

- The notebook renders rotating GIF previews of the generated 3D objects.
- The `.obj` files in the `output_assets` folder can be imported into:
- **3D software:** Blender, Maya, 3DS Max, etc.
- **Game engines:** Unity, Unreal Engine.
- **Online viewers:** e.g., https://mynameisjimmy.github.io/obj-viewer/

---

## Requirements

- Python 3.x
- PyTorch with CUDA (GPU recommended but CPU also supported)
- Google Colab (recommended for ease of use and free GPU access)
- Dependencies listed in the notebook are installed automatically.

---

## Notes and Tips

- Shap-E requires decent GPU memory (~12GB+ recommended). If running on CPU or low memory, generation may be slow or less accurate.
- The exported OBJ models contain geometry but may not have complex materials or textures.
- For advanced usage, refer to [Shap-E GitHub repo](https://github.com/openai/shap-e).

---

## Example Generated Assets

The `output_assets` folder contains four sample 3D assets generated from the default prompts:

| File                 | Description           |
|----------------------|-----------------------|
| `example_mesh_0.obj` | "a robot"             |
| `example_mesh_1.obj` | "a futuristic car"    |
| `example_mesh_2.obj` | "a medieval sword"    |
| `example_mesh_3.obj` | "a flying drone"      |

You can preview these files in any OBJ-supporting application.

---

## How It Works (Summary)

1. Clone Shap-E repo and install dependencies.
2. Load pre-trained Shap-E text-to-3D model.
3. Define a batch of text prompts.
4. Use the diffusion model to sample 3D latent representations for each prompt.
5. Decode latents into 3D meshes using the transmitter model.
6. Render preview images and export the meshes as OBJ files.

---

## License & Acknowledgments

- This project uses OpenAI’s Shap-E under the license specified in their [GitHub](https://github.com/openai/shap-e).
- Thanks to the OpenAI team for providing open-source 3D generation tools.
- This repository is for educational and demonstration purposes.

---
