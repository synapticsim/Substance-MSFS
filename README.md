# Substance Painter for MSFS

This repository contains tools to aid with using Substance Painter for Microsoft Flight Simulator.

## Installing

### Material Templates

Move everything from `Material Templates/` to `Documents/Adobe/Adobe Substance 3D Painter/assets/templates/`.

### Export Templates

Move everything from `Export Templates/` to `Documents/Adobe/Adobe Substance 3D Painter/assets/export-presets/`.

## Generators

Drag the files into your shelf and import them as `generators`. You can choose to import them into your library or just into a project.

## Material Workflows

### Standard

The MSFS Standard material type is the material type that you're going to be using the most.
It is also the same as other engines' standard material, and so, is well supported in Substance Painter.

Simply create a texture set using the `MSFS Standard` material template and texture normally.

When you want to export, use the `MSFS Standard` export preset.

### Anisotropic

Microsoft Flight Simulator uses a different texture format for anisotropic highlights, compared to what Substance Painter uses.

Thus, you are going to have to use the `MSFS Anisotropy` generator to convert the formats.

1. Create a texture set using the `MSFS Anisotropic` material.
2. At the top of the layer stack, create an `Anchor Point`.
3. Above the anchor point, create a fill layer, and add the `MSFS Anisotropy` generator to it.
4. Remove all the layers from the generator output except `MSFS Anisotropy`.
5. Set up the `Anisotropy angle` and `Anisotropy level` inputs using the anchor point.

Ensure that the layer containg the `MSFS Anisotropy` generator and `Anchor Point` is always above the layers in which the anisotropy textures are edited.

To export, use the `MSFS Anisotropy` export preset.

### Clear Coat

Clear coat is also well supported by Substance Painter.

Use the `MSFS Clear Coat` template to create your texture set, and use the `MSFS Clear Coat` export preset to export.

### Windshield

The windshield material is an MSFS-specific material, and thus, requires custom layers to work. 
In the future, we may add a custom shader to render the windshield material properly.

Create the texture set using the `MSFS Windshield` template.

1. Use the `Scratches` channel to output windshield scratches.
2. Use the `Icing` channel to output the icing mask.
3. Use the `Fingerprints` channel to create fingerprints.
4. Use the `Icing Normal` channel to author normals for the icing.

Export using the `MSFS Windshield` export preset.
