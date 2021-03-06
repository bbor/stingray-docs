# ShaderFX shader graphs

The standard material that you can create and assign in Stingray uses a physically based shader graph, built with ShaderFX nodes, that respects the laws of physics and energy conservation. The Stingray PBS (physically based shader) lets you balance diffusion/reflection and microsurface detail/reflectivity using roughness, normal, and metallic maps. For more information about the shader nodes supplied with Stingray, see [Stingray Shader Node Reference](../../../shaders_ref/index.html).

The Stingray PBS is also available in Maya 2016, Maya LT 2016, and 3ds Max 2016. This means you can create a Stingray PBS node in these design tools, build its shader graph using ShaderFX nodes, then import the scene into Stingray. The model will look exactly the same, and the imported graph will be the same, including all input connections and nodes. See also ~{ Interop with Maya, Maya LT, or 3ds Max }~.

> **Note:** If the shader uses a custom preset, the preset shader graph is also exported.

Refer to the DCC product documentation for information on creating physically based shaders in ShaderFX:

- [Maya LT 2017 Help](http://help.autodesk.com/view/MAYALT/2017/ENU/)
- [Maya 2017 Help](http://help.autodesk.com/view/MAYAUL/2017/ENU/)
- [3ds Max 2017 Help](http://help.autodesk.com/view/3DSMAX/2017/ENU/)

For example, in Maya and Maya LT, look for the following topics:

- *About ShaderFX*
- *ShaderFX introductory sample workflow*
- *Create a Stingray Physically Based Shader*
- *Export a Stingray Physically Based Shader*

In Stingray, you'll use the ~{ Shader Graph Editor }~ to create and edit shader graphs. See ~{ Create or edit shader graphs }~.

---
Related topics:
- ~{ Create a parent material }~
- ~{ Interop with Maya, Maya LT, or 3ds Max }~

Tags:
- physically-based shader
---
