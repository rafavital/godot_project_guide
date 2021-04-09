# Godot Project Guide
A through convention for Godot Project's organization and naming conventions

# Folder Structure
By default godot creates the **res://** folder, inside of it create two folders **assets** and **src**

## assets
Inside of this folder put all of the project assets not directly related to the engine (e.g sprites, textures, models, audio files)

## src
Inside of this folder put all of the projects engine related files (e.g scenes, resources, scripts, shaders, etc)

# Naming Conventions

## Folder Hierarchy
In order to create easy to understand names make use of the folder hierachy for you advantage

## Inside of src
All files inside of src shall be named using snake_case naming convention with the exception of scripts, which shall be named with PascalCase naming convention to be easily distinguable

## Inside of assets
All files inside of assets shall be named using snake_case convention

## Naming assets
To improve asset naming and easy recognition use the following rule

> prefix_name_variant_sufix

where:
- prefix: defines the asset type (meshes, textures, scenes, scripts, etc)
- name: use simple and descriptive names (e.g. if an asset is related to a character named bob it's name should be "bob")
- variant: used to define variations of a given asset, can be used as plain text or numbers
  - for specific variations use descriptive names (e.g. for a variation of bob you can use bob_evil or bob_retro)
  - for unespecific variations you may use numbers (e.g rock_01, rock_02, rock_03)
- sufix: is used for further specification of a subtype of asset, such as textures, resources, etc

### Examples
#### Ladder
| Asset Type              | Asset Name        |
| ----------              | ----------        |
| Mesh                    | mesh_ladder       |
| Material                | mat_ladder        |
| Texture (Albedo)        | t_ladder_a        |
| Texture (Normal)        | t_ladder_n        |
| Texture (Retro Albedo)  | t_ladder_retro_a  |

#### Rocks
| Asset Type | Asset Name     |
| ---------- | ----------     |
| Mesh 01    | mesh_ladder_01 |
| Mesh 02    | mesh_ladder_02 |
| Mesh 03    | mesh_ladder_03 |

### Asset Names Modifiers

#### General

| Asset Type | Prefix | Suffix | Notes |
| ----       | ----   | ----   | ----  |
| Scene | tscn | \_? | You may use the suffix to include additional information such as \_level or \_character  |
| GDScript | gd |  |  |
| Animation | a | \_? | Check animations for more information |
| Bitmap Font | f\_ | \_bmp | |
| Dynamic Font | f\_ | \_dyn | |
| Material | mat\_ | \_? | Check [materials](Material) for more information |


#### Material
| Material Subyype | Suffix | Notes |
| ----       | ----   | ----  |
| Canvas Item Material | \_cim |  |
| Particle Material | \_part |  |
| Shader Material | \_shader |  |
| Spatial Material | \_spatial |  |

# References
https://github.com/Allar/ue4-style-guide#asset-name-modifiers
https://bebylon.dev/ue4guide/wip/assets-naming-convention/
https://www.gdquest.com/docs/guidelines/best-practices/godot-gdscript/

