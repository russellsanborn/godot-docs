:github_url: hide

.. DO NOT EDIT THIS FILE!!!
.. Generated automatically from Godot engine sources.
.. Generator: https://github.com/godotengine/godot/tree/master/doc/tools/make_rst.py.
.. XML source: https://github.com/godotengine/godot/tree/master/doc/classes/Resource.xml.

.. _class_Resource:

Resource
========

**Inherits:** :ref:`RefCounted<class_RefCounted>` **<** :ref:`Object<class_Object>`

**Inherited By:** :ref:`Animation<class_Animation>`, :ref:`AnimationLibrary<class_AnimationLibrary>`, :ref:`AnimationNode<class_AnimationNode>`, :ref:`AnimationNodeStateMachinePlayback<class_AnimationNodeStateMachinePlayback>`, :ref:`AnimationNodeStateMachineTransition<class_AnimationNodeStateMachineTransition>`, :ref:`AudioBusLayout<class_AudioBusLayout>`, :ref:`AudioEffect<class_AudioEffect>`, :ref:`AudioStream<class_AudioStream>`, :ref:`BitMap<class_BitMap>`, :ref:`BoneMap<class_BoneMap>`, :ref:`ButtonGroup<class_ButtonGroup>`, :ref:`CameraAttributes<class_CameraAttributes>`, :ref:`ColorPalette<class_ColorPalette>`, :ref:`Compositor<class_Compositor>`, :ref:`CompositorEffect<class_CompositorEffect>`, :ref:`CryptoKey<class_CryptoKey>`, :ref:`Curve<class_Curve>`, :ref:`Curve2D<class_Curve2D>`, :ref:`Curve3D<class_Curve3D>`, :ref:`EditorNode3DGizmoPlugin<class_EditorNode3DGizmoPlugin>`, :ref:`EditorSettings<class_EditorSettings>`, :ref:`Environment<class_Environment>`, :ref:`FoldableGroup<class_FoldableGroup>`, :ref:`Font<class_Font>`, :ref:`GDExtension<class_GDExtension>`, :ref:`GLTFAccessor<class_GLTFAccessor>`, :ref:`GLTFAnimation<class_GLTFAnimation>`, :ref:`GLTFBufferView<class_GLTFBufferView>`, :ref:`GLTFCamera<class_GLTFCamera>`, :ref:`GLTFDocument<class_GLTFDocument>`, :ref:`GLTFDocumentExtension<class_GLTFDocumentExtension>`, :ref:`GLTFLight<class_GLTFLight>`, :ref:`GLTFMesh<class_GLTFMesh>`, :ref:`GLTFNode<class_GLTFNode>`, :ref:`GLTFPhysicsBody<class_GLTFPhysicsBody>`, :ref:`GLTFPhysicsShape<class_GLTFPhysicsShape>`, :ref:`GLTFSkeleton<class_GLTFSkeleton>`, :ref:`GLTFSkin<class_GLTFSkin>`, :ref:`GLTFSpecGloss<class_GLTFSpecGloss>`, :ref:`GLTFState<class_GLTFState>`, :ref:`GLTFTexture<class_GLTFTexture>`, :ref:`GLTFTextureSampler<class_GLTFTextureSampler>`, :ref:`Gradient<class_Gradient>`, :ref:`Image<class_Image>`, :ref:`ImporterMesh<class_ImporterMesh>`, :ref:`InputEvent<class_InputEvent>`, :ref:`JSON<class_JSON>`, :ref:`LabelSettings<class_LabelSettings>`, :ref:`LightmapGIData<class_LightmapGIData>`, :ref:`Material<class_Material>`, :ref:`Mesh<class_Mesh>`, :ref:`MeshLibrary<class_MeshLibrary>`, :ref:`MissingResource<class_MissingResource>`, :ref:`MultiMesh<class_MultiMesh>`, :ref:`NavigationMesh<class_NavigationMesh>`, :ref:`NavigationMeshSourceGeometryData2D<class_NavigationMeshSourceGeometryData2D>`, :ref:`NavigationMeshSourceGeometryData3D<class_NavigationMeshSourceGeometryData3D>`, :ref:`NavigationPolygon<class_NavigationPolygon>`, :ref:`Noise<class_Noise>`, :ref:`Occluder3D<class_Occluder3D>`, :ref:`OccluderPolygon2D<class_OccluderPolygon2D>`, :ref:`OggPacketSequence<class_OggPacketSequence>`, :ref:`OpenXRAction<class_OpenXRAction>`, :ref:`OpenXRActionMap<class_OpenXRActionMap>`, :ref:`OpenXRActionSet<class_OpenXRActionSet>`, :ref:`OpenXRBindingModifier<class_OpenXRBindingModifier>`, :ref:`OpenXRHapticBase<class_OpenXRHapticBase>`, :ref:`OpenXRInteractionProfile<class_OpenXRInteractionProfile>`, :ref:`OpenXRIPBinding<class_OpenXRIPBinding>`, :ref:`PackedDataContainer<class_PackedDataContainer>`, :ref:`PackedScene<class_PackedScene>`, :ref:`PhysicsMaterial<class_PhysicsMaterial>`, :ref:`PolygonPathFinder<class_PolygonPathFinder>`, :ref:`RDShaderFile<class_RDShaderFile>`, :ref:`RDShaderSPIRV<class_RDShaderSPIRV>`, :ref:`RichTextEffect<class_RichTextEffect>`, :ref:`SceneReplicationConfig<class_SceneReplicationConfig>`, :ref:`Script<class_Script>`, :ref:`Shader<class_Shader>`, :ref:`ShaderInclude<class_ShaderInclude>`, :ref:`Shape2D<class_Shape2D>`, :ref:`Shape3D<class_Shape3D>`, :ref:`Shortcut<class_Shortcut>`, :ref:`SkeletonModification2D<class_SkeletonModification2D>`, :ref:`SkeletonModificationStack2D<class_SkeletonModificationStack2D>`, :ref:`SkeletonProfile<class_SkeletonProfile>`, :ref:`Skin<class_Skin>`, :ref:`Sky<class_Sky>`, :ref:`SpriteFrames<class_SpriteFrames>`, :ref:`StyleBox<class_StyleBox>`, :ref:`SyntaxHighlighter<class_SyntaxHighlighter>`, :ref:`Texture<class_Texture>`, :ref:`Theme<class_Theme>`, :ref:`TileMapPattern<class_TileMapPattern>`, :ref:`TileSet<class_TileSet>`, :ref:`TileSetSource<class_TileSetSource>`, :ref:`Translation<class_Translation>`, :ref:`VideoStream<class_VideoStream>`, :ref:`VideoStreamPlayback<class_VideoStreamPlayback>`, :ref:`VisualShaderNode<class_VisualShaderNode>`, :ref:`VoxelGIData<class_VoxelGIData>`, :ref:`World2D<class_World2D>`, :ref:`World3D<class_World3D>`, :ref:`X509Certificate<class_X509Certificate>`

Base class for serializable objects.

.. rst-class:: classref-introduction-group

Description
-----------

Resource is the base class for all Godot-specific resource types, serving primarily as data containers. Since they inherit from :ref:`RefCounted<class_RefCounted>`, resources are reference-counted and freed when no longer in use. They can also be nested within other resources, and saved on disk. :ref:`PackedScene<class_PackedScene>`, one of the most common :ref:`Object<class_Object>`\ s in a Godot project, is also a resource, uniquely capable of storing and instantiating the :ref:`Node<class_Node>`\ s it contains as many times as desired.

In GDScript, resources can loaded from disk by their :ref:`resource_path<class_Resource_property_resource_path>` using :ref:`@GDScript.load()<class_@GDScript_method_load>` or :ref:`@GDScript.preload()<class_@GDScript_method_preload>`.

The engine keeps a global cache of all loaded resources, referenced by paths (see :ref:`ResourceLoader.has_cached()<class_ResourceLoader_method_has_cached>`). A resource will be cached when loaded for the first time and removed from cache once all references are released. When a resource is cached, subsequent loads using its path will return the cached reference.

\ **Note:** In C#, resources will not be freed instantly after they are no longer in use. Instead, garbage collection will run periodically and will free resources that are no longer in use. This means that unused resources will remain in memory for a while before being removed.

.. rst-class:: classref-introduction-group

Tutorials
---------

- :doc:`Resources <../tutorials/scripting/resources>`

- :doc:`When and how to avoid using nodes for everything <../tutorials/best_practices/node_alternatives>`

.. rst-class:: classref-reftable-group

Properties
----------

.. table::
   :widths: auto

   +-----------------------------+-----------------------------------------------------------------------------------+-----------+
   | :ref:`bool<class_bool>`     | :ref:`resource_local_to_scene<class_Resource_property_resource_local_to_scene>`   | ``false`` |
   +-----------------------------+-----------------------------------------------------------------------------------+-----------+
   | :ref:`String<class_String>` | :ref:`resource_name<class_Resource_property_resource_name>`                       | ``""``    |
   +-----------------------------+-----------------------------------------------------------------------------------+-----------+
   | :ref:`String<class_String>` | :ref:`resource_path<class_Resource_property_resource_path>`                       | ``""``    |
   +-----------------------------+-----------------------------------------------------------------------------------+-----------+
   | :ref:`String<class_String>` | :ref:`resource_scene_unique_id<class_Resource_property_resource_scene_unique_id>` |           |
   +-----------------------------+-----------------------------------------------------------------------------------+-----------+

.. rst-class:: classref-reftable-group

Methods
-------

.. table::
   :widths: auto

   +---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`RID<class_RID>`           | :ref:`_get_rid<class_Resource_private_method__get_rid>`\ (\ ) |virtual| |const|                                                                                   |
   +---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | |void|                          | :ref:`_reset_state<class_Resource_private_method__reset_state>`\ (\ ) |virtual|                                                                                   |
   +---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | |void|                          | :ref:`_set_path_cache<class_Resource_private_method__set_path_cache>`\ (\ path\: :ref:`String<class_String>`\ ) |virtual| |const|                                 |
   +---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | |void|                          | :ref:`_setup_local_to_scene<class_Resource_private_method__setup_local_to_scene>`\ (\ ) |virtual|                                                                 |
   +---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`Resource<class_Resource>` | :ref:`duplicate<class_Resource_method_duplicate>`\ (\ deep\: :ref:`bool<class_bool>` = false\ ) |const|                                                           |
   +---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`Resource<class_Resource>` | :ref:`duplicate_deep<class_Resource_method_duplicate_deep>`\ (\ deep_subresources_mode\: :ref:`DeepDuplicateMode<enum_Resource_DeepDuplicateMode>` = 1\ ) |const| |
   +---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | |void|                          | :ref:`emit_changed<class_Resource_method_emit_changed>`\ (\ )                                                                                                     |
   +---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`String<class_String>`     | :ref:`generate_scene_unique_id<class_Resource_method_generate_scene_unique_id>`\ (\ ) |static|                                                                    |
   +---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`String<class_String>`     | :ref:`get_id_for_path<class_Resource_method_get_id_for_path>`\ (\ path\: :ref:`String<class_String>`\ ) |const|                                                   |
   +---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`Node<class_Node>`         | :ref:`get_local_scene<class_Resource_method_get_local_scene>`\ (\ ) |const|                                                                                       |
   +---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`RID<class_RID>`           | :ref:`get_rid<class_Resource_method_get_rid>`\ (\ ) |const|                                                                                                       |
   +---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`bool<class_bool>`         | :ref:`is_built_in<class_Resource_method_is_built_in>`\ (\ ) |const|                                                                                               |
   +---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | |void|                          | :ref:`reset_state<class_Resource_method_reset_state>`\ (\ )                                                                                                       |
   +---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | |void|                          | :ref:`set_id_for_path<class_Resource_method_set_id_for_path>`\ (\ path\: :ref:`String<class_String>`, id\: :ref:`String<class_String>`\ )                         |
   +---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | |void|                          | :ref:`set_path_cache<class_Resource_method_set_path_cache>`\ (\ path\: :ref:`String<class_String>`\ )                                                             |
   +---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | |void|                          | :ref:`setup_local_to_scene<class_Resource_method_setup_local_to_scene>`\ (\ )                                                                                     |
   +---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | |void|                          | :ref:`take_over_path<class_Resource_method_take_over_path>`\ (\ path\: :ref:`String<class_String>`\ )                                                             |
   +---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

Signals
-------

.. _class_Resource_signal_changed:

.. rst-class:: classref-signal

**changed**\ (\ ) :ref:`🔗<class_Resource_signal_changed>`

Emitted when the resource changes, usually when one of its properties is modified. See also :ref:`emit_changed()<class_Resource_method_emit_changed>`.

\ **Note:** This signal is not emitted automatically for properties of custom resources. If necessary, a setter needs to be created to emit the signal.

.. rst-class:: classref-item-separator

----

.. _class_Resource_signal_setup_local_to_scene_requested:

.. rst-class:: classref-signal

**setup_local_to_scene_requested**\ (\ ) :ref:`🔗<class_Resource_signal_setup_local_to_scene_requested>`

**Deprecated:** This signal is only emitted when the resource is created. Override :ref:`_setup_local_to_scene()<class_Resource_private_method__setup_local_to_scene>` instead.

Emitted by a newly duplicated resource with :ref:`resource_local_to_scene<class_Resource_property_resource_local_to_scene>` set to ``true``.

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

Enumerations
------------

.. _enum_Resource_DeepDuplicateMode:

.. rst-class:: classref-enumeration

enum **DeepDuplicateMode**: :ref:`🔗<enum_Resource_DeepDuplicateMode>`

.. _class_Resource_constant_DEEP_DUPLICATE_NONE:

.. rst-class:: classref-enumeration-constant

:ref:`DeepDuplicateMode<enum_Resource_DeepDuplicateMode>` **DEEP_DUPLICATE_NONE** = ``0``

No subresorces at all are duplicated. This is useful even in a deep duplication to have all the arrays and dictionaries duplicated but still pointing to the original resources.

.. _class_Resource_constant_DEEP_DUPLICATE_INTERNAL:

.. rst-class:: classref-enumeration-constant

:ref:`DeepDuplicateMode<enum_Resource_DeepDuplicateMode>` **DEEP_DUPLICATE_INTERNAL** = ``1``

Only subresources without a path or with a scene-local path will be duplicated.

.. _class_Resource_constant_DEEP_DUPLICATE_ALL:

.. rst-class:: classref-enumeration-constant

:ref:`DeepDuplicateMode<enum_Resource_DeepDuplicateMode>` **DEEP_DUPLICATE_ALL** = ``2``

Every subresource found will be duplicated, even if it has a non-local path. In other words, even potentially big resources stored separately will be duplicated.

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

Property Descriptions
---------------------

.. _class_Resource_property_resource_local_to_scene:

.. rst-class:: classref-property

:ref:`bool<class_bool>` **resource_local_to_scene** = ``false`` :ref:`🔗<class_Resource_property_resource_local_to_scene>`

.. rst-class:: classref-property-setget

- |void| **set_local_to_scene**\ (\ value\: :ref:`bool<class_bool>`\ )
- :ref:`bool<class_bool>` **is_local_to_scene**\ (\ )

If ``true``, the resource is duplicated for each instance of all scenes using it. At run-time, the resource can be modified in one scene without affecting other instances (see :ref:`PackedScene.instantiate()<class_PackedScene_method_instantiate>`).

\ **Note:** Changing this property at run-time has no effect on already created duplicate resources.

.. rst-class:: classref-item-separator

----

.. _class_Resource_property_resource_name:

.. rst-class:: classref-property

:ref:`String<class_String>` **resource_name** = ``""`` :ref:`🔗<class_Resource_property_resource_name>`

.. rst-class:: classref-property-setget

- |void| **set_name**\ (\ value\: :ref:`String<class_String>`\ )
- :ref:`String<class_String>` **get_name**\ (\ )

An optional name for this resource. When defined, its value is displayed to represent the resource in the Inspector dock. For built-in scripts, the name is displayed as part of the tab name in the script editor.

\ **Note:** Some resource formats do not support resource names. You can still set the name in the editor or via code, but it will be lost when the resource is reloaded. For example, only built-in scripts can have a resource name, while scripts stored in separate files cannot.

.. rst-class:: classref-item-separator

----

.. _class_Resource_property_resource_path:

.. rst-class:: classref-property

:ref:`String<class_String>` **resource_path** = ``""`` :ref:`🔗<class_Resource_property_resource_path>`

.. rst-class:: classref-property-setget

- |void| **set_path**\ (\ value\: :ref:`String<class_String>`\ )
- :ref:`String<class_String>` **get_path**\ (\ )

The unique path to this resource. If it has been saved to disk, the value will be its filepath. If the resource is exclusively contained within a scene, the value will be the :ref:`PackedScene<class_PackedScene>`'s filepath, followed by a unique identifier.

\ **Note:** Setting this property manually may fail if a resource with the same path has already been previously loaded. If necessary, use :ref:`take_over_path()<class_Resource_method_take_over_path>`.

.. rst-class:: classref-item-separator

----

.. _class_Resource_property_resource_scene_unique_id:

.. rst-class:: classref-property

:ref:`String<class_String>` **resource_scene_unique_id** :ref:`🔗<class_Resource_property_resource_scene_unique_id>`

.. rst-class:: classref-property-setget

- |void| **set_scene_unique_id**\ (\ value\: :ref:`String<class_String>`\ )
- :ref:`String<class_String>` **get_scene_unique_id**\ (\ )

A unique identifier relative to the this resource's scene. If left empty, the ID is automatically generated when this resource is saved inside a :ref:`PackedScene<class_PackedScene>`. If the resource is not inside a scene, this property is empty by default.

\ **Note:** When the :ref:`PackedScene<class_PackedScene>` is saved, if multiple resources in the same scene use the same ID, only the earliest resource in the scene hierarchy keeps the original ID. The other resources are assigned new IDs from :ref:`generate_scene_unique_id()<class_Resource_method_generate_scene_unique_id>`.

\ **Note:** Setting this property does not emit the :ref:`changed<class_Resource_signal_changed>` signal.

\ **Warning:** When setting, the ID must only consist of letters, numbers, and underscores. Otherwise, it will fail and default to a randomly generated ID.

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

Method Descriptions
-------------------

.. _class_Resource_private_method__get_rid:

.. rst-class:: classref-method

:ref:`RID<class_RID>` **_get_rid**\ (\ ) |virtual| |const| :ref:`🔗<class_Resource_private_method__get_rid>`

Override this method to return a custom :ref:`RID<class_RID>` when :ref:`get_rid()<class_Resource_method_get_rid>` is called.

.. rst-class:: classref-item-separator

----

.. _class_Resource_private_method__reset_state:

.. rst-class:: classref-method

|void| **_reset_state**\ (\ ) |virtual| :ref:`🔗<class_Resource_private_method__reset_state>`

For resources that use a variable number of properties, either via :ref:`Object._validate_property()<class_Object_private_method__validate_property>` or :ref:`Object._get_property_list()<class_Object_private_method__get_property_list>`, this method should be implemented to correctly clear the resource's state.

.. rst-class:: classref-item-separator

----

.. _class_Resource_private_method__set_path_cache:

.. rst-class:: classref-method

|void| **_set_path_cache**\ (\ path\: :ref:`String<class_String>`\ ) |virtual| |const| :ref:`🔗<class_Resource_private_method__set_path_cache>`

Sets the resource's path to ``path`` without involving the resource cache.

.. rst-class:: classref-item-separator

----

.. _class_Resource_private_method__setup_local_to_scene:

.. rst-class:: classref-method

|void| **_setup_local_to_scene**\ (\ ) |virtual| :ref:`🔗<class_Resource_private_method__setup_local_to_scene>`

Override this method to customize the newly duplicated resource created from :ref:`PackedScene.instantiate()<class_PackedScene_method_instantiate>`, if the original's :ref:`resource_local_to_scene<class_Resource_property_resource_local_to_scene>` is set to ``true``.

\ **Example:** Set a random ``damage`` value to every local resource from an instantiated scene:

::

    extends Resource

    var damage = 0

    func _setup_local_to_scene():
        damage = randi_range(10, 40)

.. rst-class:: classref-item-separator

----

.. _class_Resource_method_duplicate:

.. rst-class:: classref-method

:ref:`Resource<class_Resource>` **duplicate**\ (\ deep\: :ref:`bool<class_bool>` = false\ ) |const| :ref:`🔗<class_Resource_method_duplicate>`

Duplicates this resource, returning a new resource with its ``export``\ ed or :ref:`@GlobalScope.PROPERTY_USAGE_STORAGE<class_@GlobalScope_constant_PROPERTY_USAGE_STORAGE>` properties copied from the original.

If ``deep`` is ``false``, a **shallow** copy is returned: nested :ref:`Array<class_Array>`, :ref:`Dictionary<class_Dictionary>`, and **Resource** properties are not duplicated and are shared with the original resource.

If ``deep`` is ``true``, a **deep** copy is returned: all nested arrays, dictionaries, and packed arrays are also duplicated (recursively). Any **Resource** found inside will only be duplicated if it's local, like :ref:`DEEP_DUPLICATE_INTERNAL<class_Resource_constant_DEEP_DUPLICATE_INTERNAL>` used with :ref:`duplicate_deep()<class_Resource_method_duplicate_deep>`.

The following exceptions apply:

- Subresource properties with the :ref:`@GlobalScope.PROPERTY_USAGE_ALWAYS_DUPLICATE<class_@GlobalScope_constant_PROPERTY_USAGE_ALWAYS_DUPLICATE>` flag are always duplicated (recursively or not, depending on ``deep``).

- Subresource properties with the :ref:`@GlobalScope.PROPERTY_USAGE_NEVER_DUPLICATE<class_@GlobalScope_constant_PROPERTY_USAGE_NEVER_DUPLICATE>` flag are never duplicated.

\ **Note:** For custom resources, this method will fail if :ref:`Object._init()<class_Object_private_method__init>` has been defined with required parameters.

\ **Note:** When duplicating with ``deep`` set to ``true``, each resource found, including the one on which this method is called, will be only duplicated once and referenced as many times as needed in the duplicate. For instance, if you are duplicating resource A that happens to have resource B referenced twice, you'll get a new resource A' referencing a new resource B' twice.

.. rst-class:: classref-item-separator

----

.. _class_Resource_method_duplicate_deep:

.. rst-class:: classref-method

:ref:`Resource<class_Resource>` **duplicate_deep**\ (\ deep_subresources_mode\: :ref:`DeepDuplicateMode<enum_Resource_DeepDuplicateMode>` = 1\ ) |const| :ref:`🔗<class_Resource_method_duplicate_deep>`

Duplicates this resource, deeply, like :ref:`duplicate()<class_Resource_method_duplicate>`\ ``(true)``, with extra control over how subresources are handled.

\ ``deep_subresources_mode`` must be one of the values from :ref:`DeepDuplicateMode<enum_Resource_DeepDuplicateMode>`.

.. rst-class:: classref-item-separator

----

.. _class_Resource_method_emit_changed:

.. rst-class:: classref-method

|void| **emit_changed**\ (\ ) :ref:`🔗<class_Resource_method_emit_changed>`

Emits the :ref:`changed<class_Resource_signal_changed>` signal. This method is called automatically for some built-in resources.

\ **Note:** For custom resources, it's recommended to call this method whenever a meaningful change occurs, such as a modified property. This ensures that custom :ref:`Object<class_Object>`\ s depending on the resource are properly updated.

::

    var damage:
        set(new_value):
            if damage != new_value:
                damage = new_value
                emit_changed()

.. rst-class:: classref-item-separator

----

.. _class_Resource_method_generate_scene_unique_id:

.. rst-class:: classref-method

:ref:`String<class_String>` **generate_scene_unique_id**\ (\ ) |static| :ref:`🔗<class_Resource_method_generate_scene_unique_id>`

Generates a unique identifier for a resource to be contained inside a :ref:`PackedScene<class_PackedScene>`, based on the current date, time, and a random value. The returned string is only composed of letters (``a`` to ``y``) and numbers (``0`` to ``8``). See also :ref:`resource_scene_unique_id<class_Resource_property_resource_scene_unique_id>`.

.. rst-class:: classref-item-separator

----

.. _class_Resource_method_get_id_for_path:

.. rst-class:: classref-method

:ref:`String<class_String>` **get_id_for_path**\ (\ path\: :ref:`String<class_String>`\ ) |const| :ref:`🔗<class_Resource_method_get_id_for_path>`

Returns the unique identifier for the resource with the given ``path`` from the resource cache. If the resource is not loaded and cached, an empty string is returned.

\ **Note:** This method is only implemented when running in an editor context. At runtime, it returns an empty string.

.. rst-class:: classref-item-separator

----

.. _class_Resource_method_get_local_scene:

.. rst-class:: classref-method

:ref:`Node<class_Node>` **get_local_scene**\ (\ ) |const| :ref:`🔗<class_Resource_method_get_local_scene>`

If :ref:`resource_local_to_scene<class_Resource_property_resource_local_to_scene>` is set to ``true`` and the resource has been loaded from a :ref:`PackedScene<class_PackedScene>` instantiation, returns the root :ref:`Node<class_Node>` of the scene where this resource is used. Otherwise, returns ``null``.

.. rst-class:: classref-item-separator

----

.. _class_Resource_method_get_rid:

.. rst-class:: classref-method

:ref:`RID<class_RID>` **get_rid**\ (\ ) |const| :ref:`🔗<class_Resource_method_get_rid>`

Returns the :ref:`RID<class_RID>` of this resource (or an empty RID). Many resources (such as :ref:`Texture2D<class_Texture2D>`, :ref:`Mesh<class_Mesh>`, and so on) are high-level abstractions of resources stored in a specialized server (:ref:`DisplayServer<class_DisplayServer>`, :ref:`RenderingServer<class_RenderingServer>`, etc.), so this function will return the original :ref:`RID<class_RID>`.

.. rst-class:: classref-item-separator

----

.. _class_Resource_method_is_built_in:

.. rst-class:: classref-method

:ref:`bool<class_bool>` **is_built_in**\ (\ ) |const| :ref:`🔗<class_Resource_method_is_built_in>`

Returns ``true`` if the resource is built-in (from the engine) or ``false`` if it is user-defined.

.. rst-class:: classref-item-separator

----

.. _class_Resource_method_reset_state:

.. rst-class:: classref-method

|void| **reset_state**\ (\ ) :ref:`🔗<class_Resource_method_reset_state>`

For resources that use a variable number of properties, either via :ref:`Object._validate_property()<class_Object_private_method__validate_property>` or :ref:`Object._get_property_list()<class_Object_private_method__get_property_list>`, override :ref:`_reset_state()<class_Resource_private_method__reset_state>` to correctly clear the resource's state.

.. rst-class:: classref-item-separator

----

.. _class_Resource_method_set_id_for_path:

.. rst-class:: classref-method

|void| **set_id_for_path**\ (\ path\: :ref:`String<class_String>`, id\: :ref:`String<class_String>`\ ) :ref:`🔗<class_Resource_method_set_id_for_path>`

Sets the unique identifier to ``id`` for the resource with the given ``path`` in the resource cache. If the unique identifier is empty, the cache entry using ``path`` is removed if it exists.

\ **Note:** This method is only implemented when running in an editor context.

.. rst-class:: classref-item-separator

----

.. _class_Resource_method_set_path_cache:

.. rst-class:: classref-method

|void| **set_path_cache**\ (\ path\: :ref:`String<class_String>`\ ) :ref:`🔗<class_Resource_method_set_path_cache>`

Sets the resource's path to ``path`` without involving the resource cache.

.. rst-class:: classref-item-separator

----

.. _class_Resource_method_setup_local_to_scene:

.. rst-class:: classref-method

|void| **setup_local_to_scene**\ (\ ) :ref:`🔗<class_Resource_method_setup_local_to_scene>`

**Deprecated:** This method should only be called internally.

Calls :ref:`_setup_local_to_scene()<class_Resource_private_method__setup_local_to_scene>`. If :ref:`resource_local_to_scene<class_Resource_property_resource_local_to_scene>` is set to ``true``, this method is automatically called from :ref:`PackedScene.instantiate()<class_PackedScene_method_instantiate>` by the newly duplicated resource within the scene instance.

.. rst-class:: classref-item-separator

----

.. _class_Resource_method_take_over_path:

.. rst-class:: classref-method

|void| **take_over_path**\ (\ path\: :ref:`String<class_String>`\ ) :ref:`🔗<class_Resource_method_take_over_path>`

Sets the :ref:`resource_path<class_Resource_property_resource_path>` to ``path``, potentially overriding an existing cache entry for this path. Further attempts to load an overridden resource by path will instead return this resource.

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |required| replace:: :abbr:`required (This method is required to be overridden when extending its base class.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
.. |constructor| replace:: :abbr:`constructor (This method is used to construct a type.)`
.. |static| replace:: :abbr:`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
.. |operator| replace:: :abbr:`operator (This method describes a valid operator to use with this type as left-hand operand.)`
.. |bitfield| replace:: :abbr:`BitField (This value is an integer composed as a bitmask of the following flags.)`
.. |void| replace:: :abbr:`void (No return value.)`
