
---- Minecraft Crash Report ----
// Uh... Did I do that?

Time: 2022-04-02 23:29:18 EDT
Description: Initializing game

java.lang.OutOfMemoryError: GC overhead limit exceeded
    at com.google.common.collect.Maps.newHashMap(Maps.java:275)
    at net.minecraftforge.client.model.ForgeBlockStateV1$Variant.<init>(ForgeBlockStateV1.java:296)
    at net.minecraftforge.client.model.ForgeBlockStateV1$Variant.mergeModelPartVariants(ForgeBlockStateV1.java:377)
    at net.minecraftforge.client.model.ForgeBlockStateV1$Variant.<init>(ForgeBlockStateV1.java:316)
    at net.minecraftforge.client.model.ForgeBlockStateV1$Variant.mergeModelPartVariants(ForgeBlockStateV1.java:377)
    at net.minecraftforge.client.model.ForgeBlockStateV1$Variant.<init>(ForgeBlockStateV1.java:316)
    at net.minecraftforge.client.model.ForgeBlockStateV1$Variant.mergeModelPartVariants(ForgeBlockStateV1.java:377)
    at net.minecraftforge.client.model.ForgeBlockStateV1$Variant.<init>(ForgeBlockStateV1.java:316)
    at net.minecraftforge.client.model.ForgeBlockStateV1$Variant.mergeModelPartVariants(ForgeBlockStateV1.java:377)
    at net.minecraftforge.client.model.ForgeBlockStateV1$Variant.<init>(ForgeBlockStateV1.java:316)
    at net.minecraftforge.client.model.ForgeBlockStateV1$Variant.mergeModelPartVariants(ForgeBlockStateV1.java:377)
    at net.minecraftforge.client.model.ForgeBlockStateV1$Variant.<init>(ForgeBlockStateV1.java:316)
    at net.minecraftforge.client.model.ForgeBlockStateV1$Variant.mergeModelPartVariants(ForgeBlockStateV1.java:377)
    at net.minecraftforge.client.model.ForgeBlockStateV1$Variant.sync(ForgeBlockStateV1.java:343)
    at net.minecraftforge.client.model.ForgeBlockStateV1$Deserializer.deserialize(ForgeBlockStateV1.java:167)
    at net.minecraftforge.client.model.ForgeBlockStateV1$Deserializer.deserialize(ForgeBlockStateV1.java:68)
    at com.google.gson.internal.bind.TreeTypeAdapter.read(TreeTypeAdapter.java:69)
    at com.google.gson.Gson.fromJson(Gson.java:887)
    at com.google.gson.Gson.fromJson(Gson.java:825)
    at net.minecraftforge.client.model.BlockStateLoader.load(BlockStateLoader.java:85)
    at net.minecraft.client.renderer.block.model.ModelBlockDefinition.parseFromReader(ModelBlockDefinition.java:42)
    at net.minecraft.client.renderer.block.model.ModelBakery.loadModelBlockDefinition(ModelBakery.java:242)
    at net.minecraft.client.renderer.block.model.ModelBakery.loadMultipartMBD(ModelBakery.java:223)
    at net.minecraft.client.renderer.block.model.ModelBakery.getModelBlockDefinition(ModelBakery.java:208)
    at net.minecraftforge.client.model.ModelLoader.getModelBlockDefinition(ModelLoader.java:265)
    at net.minecraft.client.renderer.block.model.ModelBakery.loadBlock(ModelBakery.java:121)
    at net.minecraftforge.client.model.ModelLoader.loadBlocks(ModelLoader.java:223)
    at net.minecraftforge.client.model.ModelLoader.setupModelRegistry(ModelLoader.java:150)
    at net.minecraft.client.renderer.block.model.ModelManager.onResourceManagerReload(ModelManager.java:28)
    at net.minecraft.client.resources.SimpleReloadableResourceManager.registerReloadListener(SimpleReloadableResourceManager.java:121)
    at net.minecraft.client.Minecraft.init(Minecraft.java:513)
    at net.minecraft.client.Minecraft.run(Minecraft.java:3931)


A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------

-- System Details --
  Minecraft Version: 1.12.2
  Operating System: Windows 10 (amd64) version 10.0
  Java Version: 1.8.0_51, Oracle Corporation
  Java VM Version: Java HotSpot(TM) 64-Bit Server VM (mixed mode), Oracle Corporation
  Memory: 486045472 bytes (463 MB) / 3817865216 bytes (3641 MB) up to 3817865216 bytes (3641 MB)
  JVM Flags: 3 total; -XX:HeapDumpPath=MojangTricksIntelDriversForPerformance_javaw.exe_minecraft.exe.heapdump -Xmx4096m -Xms256m
  IntCache: cache: 0, tcache: 0, allocated: 0, tallocated: 0
  FML: MCP 9.42 Powered by Forge 14.23.5.2854 377 mods loaded, 375 mods active
       States: 'U' = Unloaded 'L' = Loaded 'C' = Constructed 'H' = Pre-initialized 'I' = Initialized 'J' = Post-initialized 'A' = Available 'D' = Disabled 'E' = Errored
       
       | State | ID                                | Version                  | Source                                            | Signature                                |
       |:----- |:--------------------------------- |:------------------------ |:------------------------------------------------- |:---------------------------------------- |
       | LCH   | minecraft                         | 1.12.2                   | minecraft.jar                                     | None                                     |
       | LCH   | mcp                               | 9.42                     | minecraft.jar                                     | None                                     |
       | LCH   | FML                               | 8.0.99.99                | forge-1.12.2-14.23.5.2854.jar                     | e3c3d50c7c986df74c645c0ac54639741c90a557 |
       | LCH   | forge                             | 14.23.5.2854             | forge-1.12.2-14.23.5.2854.jar                     | e3c3d50c7c986df74c645c0ac54639741c90a557 |
       | LCH   | advancedrocketrycore              | 1                        | minecraft.jar                                     | None                                     |
       | LCH   | ColorUtility                      | 1.0.4                    | minecraft.jar                                     | None                                     |
       | LCH   | creativecoredummy                 | 1.0.0                    | minecraft.jar                                     | None                                     |
       | LCH   | ivtoolkit                         | 1.3.3-1.12               | minecraft.jar                                     | None                                     |
       | LCH   | littletilescore                   | 1.0.0                    | minecraft.jar                                     | None                                     |
       | LCH   | openmodscore                      | 0.12.2                   | minecraft.jar                                     | None                                     |
       | LCH   | obfuscate                         | 0.4.2                    | minecraft.jar                                     | None                                     |
       | LCH   | opencomputers|core                | 1.7.5.192                | minecraft.jar                                     | None                                     |
       | LCH   | randompatches                     | 1.12.2-1.22.1.10         | randompatches-1.12.2-1.22.1.10.jar                | None                                     |
       | LCH   | tweakersconstruct                 | 1.12.2-1.6.0             | tweakersconstruct-1.12.2-1.6.0.jar                | None                                     |
       | LCH   | fastbench                         | 1.7.3                    | FastWorkbench-1.12.2-1.7.3.jar                    | None                                     |
       | LCH   | actuallyadditions                 | 1.12.2-r152              | ActuallyAdditions-1.12.2-r152.jar                 | None                                     |
       | LCH   | forgeendertech                    | 1.12.2-4.5.5.0           | ForgeEndertech-1.12.2-4.5.5.0-build.0561.jar      | None                                     |
       | LCH   | adhooks                           | 1.12.2-3.3.0.0           | AdHooks-1.12.2-3.3.0.0-build.0528.jar             | None                                     |
       | LCH   | adlods                            | 1.12.2-1.0.8.0           | AdLods-1.12.2-1.0.8.0-build.0504.jar              | None                                     |
       | LCH   | redstoneflux                      | 2.1.1                    | RedstoneFlux-1.12-2.1.1.1-universal.jar           | None                                     |
       | LCH   | cofhcore                          | 4.6.6                    | CoFHCore-1.12.2-4.6.6.1-universal.jar             | None                                     |
       | LCH   | libvulpes                         | 0.4.2.-75                | LibVulpes-1.12.2-0.4.2-75-universal.jar           | None                                     |
       | LCH   | advancedrocketry                  | 1.7.0.-232               | AdvancedRocketry-1.12.2-1.7.0-232-universal.jar   | None                                     |
       | LCH   | ctm                               | MC1.12.2-1.0.2.31        | CTM-MC1.12.2-1.0.2.31.jar                         | None                                     |
       | LCH   | appliedenergistics2               | rv6-stable-7             | appliedenergistics2-rv6-stable-7.jar              | dfa4d3ac143316c6f32aa1a1beda1e34d42132e5 |
       | LCH   | bdlib                             | 1.14.3.12                | bdlib-1.14.3.12-mc1.12.2.jar                      | None                                     |
       | LCH   | ae2stuff                          | 0.7.0.4                  | ae2stuff-0.7.0.4-mc1.12.2.jar                     | None                                     |
       | LCH   | baubles                           | 1.5.2                    | Baubles-1.12-1.5.2.jar                            | None                                     |
       | LCH   | roots                             | 1.12.2-3.0.33            | Roots-1.12.2-3.0.33.jar                           | None                                     |
       | LCH   | mysticalworld                     | 1.12.2-1.9.8             | mysticalworld-1.12.2-1.9.8.jar                    | None                                     |
       | LCH   | endercore                         | 1.12.2-0.5.76            | EnderCore-1.12.2-0.5.76.jar                       | None                                     |
       | LCH   | crafttweaker                      | 4.1.20                   | CraftTweaker2-1.12-4.1.20.618.jar                 | None                                     |
       | LCH   | mtlib                             | 3.0.6                    | MTLib-3.0.6.jar                                   | None                                     |
       | LCH   | modtweaker                        | 4.0.18                   | modtweaker-4.0.18.jar                             | None                                     |
       | LCH   | jei                               | 4.16.1.301               | jei_1.12.2-4.16.1.301.jar                         | None                                     |
       | LCH   | thaumcraft                        | 6.1.BETA26               | Thaumcraft-1.12.2-6.1.BETA26.jar                  | None                                     |
       | LCH   | codechickenlib                    | 3.2.3.358                | CodeChickenLib-1.12.2-3.2.3.358-universal.jar     | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
       | LCH   | cofhworld                         | 1.4.0                    | CoFHWorld-1.12.2-1.4.0.1-universal.jar            | None                                     |
       | LCH   | thermalfoundation                 | 2.6.7                    | ThermalFoundation-1.12.2-2.6.7.1-universal.jar    | None                                     |
       | LCH   | thermalexpansion                  | 5.5.7                    | ThermalExpansion-1.12.2-5.5.7.1-universal.jar     | None                                     |
       | LCH   | enderio                           | 5.3.70                   | EnderIO-1.12.2-5.3.70.jar                         | None                                     |
       | LCH   | mantle                            | 1.12-1.3.3.55            | Mantle-1.12-1.3.3.55.jar                          | None                                     |
       | LCH   | chisel                            | MC1.12.2-1.0.2.45        | Chisel-MC1.12.2-1.0.2.45.jar                      | None                                     |
       | LCH   | enderiointegrationtic             | 5.3.70                   | EnderIO-1.12.2-5.3.70.jar                         | None                                     |
       | LCH   | tombstone                         | 4.1.2                    | tombstone-4.1.2-1.12.2.jar                        | None                                     |
       | LCH   | quark                             | r1.6-179                 | Quark-r1.6-179.jar                                | None                                     |
       | LCH   | twilightforest                    | 3.11.1021                | twilightforest-1.12.2-3.11.1021-universal.jar     | None                                     |
       | LCH   | tconstruct                        | 1.12.2-2.13.0.183        | TConstruct-1.12.2-2.13.0.183.jar                  | None                                     |
       | LCH   | p455w0rdslib                      | 2.3.161                  | p455w0rdslib-1.12.2-2.3.161.jar                   | 186bc454cd122c9c2f1aa4f95611254bcc543363 |
       | LCH   | ae2wtlib                          | 1.0.34                   | AE2WTLib-1.12.2-1.0.34.jar                        | 186bc454cd122c9c2f1aa4f95611254bcc543363 |
       | LCH   | infinitylib                       | 1.12.2-1.12.0            | infinitylib-1.12.0.jar                            | None                                     |
       | LCH   | agricraft                         | 2.12.0-1.12.0-a6         | AgriCraft-2.12.0-1.12.0-a6.jar                    | None                                     |
       | LCH   | aiimprovements                    | 0.0.1.3                  | AIImprovements-1.12-0.0.1b3.jar                   | None                                     |
       | LCH   | akashictome                       | 1.2-12                   | AkashicTome-1.2-12.jar                            | None                                     |
       | LCH   | creativecore                      | 1.10.0                   | CreativeCore_v1.10.47_mc1.12.2.jar                | None                                     |
       | LCH   | ambientsounds                     | 3.0                      | AmbientSounds_v3.1.5_mc1.12.2.jar                 | None                                     |
       | LCH   | ebwizardry                        | 4.3.4                    | ElectroblobsWizardry-4.3.4-MC1.12.2.jar           | None                                     |
       | LCH   | ancientspellcraft                 | 1.1.3                    | ancientspellcraft-1.1.3.jar                       | None                                     |
       | LCH   | ancientwarfare                    | 1.12.2-2.7.0.1032        | ancientwarfare-1.12.2-2.7.0.1032.jar              | None                                     |
       | LCH   | buildcraftlib                     | 7.99.24.8                | buildcraft-all-7.99.24.8.jar                      | None                                     |
       | LCH   | buildcraftcore                    | 7.99.24.8                | buildcraft-all-7.99.24.8.jar                      | None                                     |
       | LCH   | ancientwarfareautomation          | 1.12.2-2.7.0.1032        | ancientwarfare-1.12.2-2.7.0.1032.jar              | None                                     |
       | LCH   | ancientwarfarenpc                 | 1.12.2-2.7.0.1032        | ancientwarfare-1.12.2-2.7.0.1032.jar              | None                                     |
       | LCH   | ancientwarfarestructure           | 1.12.2-2.7.0.1032        | ancientwarfare-1.12.2-2.7.0.1032.jar              | None                                     |
       | LCH   | ancientwarfarevehicle             | 1.12.2-2.7.0.1032        | ancientwarfare-1.12.2-2.7.0.1032.jar              | None                                     |
       | LCH   | applecore                         | 3.4.0                    | AppleCore-mc1.12.2-3.4.0.jar                      | None                                     |
       | LCH   | appleskin                         | 1.0.14                   | AppleSkin-mc1.12-1.0.14.jar                       | None                                     |
       | LCH   | architecturecraft                 | @VERSION@                | architecturecraft-1.12-3.98.jar                   | None                                     |
       | LCH   | conarm                            | 1.2.5.10                 | conarm-1.12.2-1.2.5.10.jar                        | b33d2c8df492beff56d1bbbc92da49b8ab7345a1 |
       | LCH   | armoryexpansion                   | 1.4.2                    | armoryexpansion-1.4.2.jar                         | None                                     |
       | LCH   | armoryexpansion-custommaterials   | 1.4.2                    | armoryexpansion-1.4.2.jar                         | None                                     |
       | LCH   | hammercore                        | 2.0.6.26                 | HammerLib-1.12.2-2.0.6.26.jar                     | 9f5e2a811a8332a842b34f6967b7db0ac4f24856 |
       | LCH   | thaumadditions                    | 12.6.6                   | ThaumicAdditions-1.12.2-12.6.6.jar                | 9f5e2a811a8332a842b34f6967b7db0ac4f24856 |
       | LCH   | llibrary                          | 1.7.20                   | llibrary-1.7.20-1.12.2.jar                        | b9f30a813bee3b9dd5652c460310cfcd54f6b7ec |
       | LCH   | iceandfire                        | 1.9.1                    | iceandfire-1.9.1-1.12.2.jar                       | None                                     |
       | LCH   | armoryexpansion-iceandfire        | 1.4.2                    | armoryexpansion-1.4.2.jar                         | None                                     |
       | LCH   | armoryexpansion-matteroverdrive   | 1.4.2                    | armoryexpansion-1.4.2.jar                         | None                                     |
       | LCH   | aroma1997core                     | 2.0.0.2.b167             | Aroma1997Core-1.12.2-2.0.0.2.b167.jar             | dfbfe4c473253d8c5652417689848f650b2cbe32 |
       | LCH   | aromabackup                       | 3.0.0.0.b135             | AromaBackup-1.12.2-3.0.0.0.b135.jar               | dfbfe4c473253d8c5652417689848f650b2cbe32 |
       | LCH   | aromabackuprecovery               | 3.0.0.0.b135             | AromaBackup-1.12.2-3.0.0.0.b135.jar               | dfbfe4c473253d8c5652417689848f650b2cbe32 |
       | LCH   | artifacts                         | 1.12.2-1.2.3             | Artifacts-1.12.2-1.2.3.jar                        | None                                     |
       | LCH   | astralsorcery                     | 1.10.27                  | astralsorcery-1.12.2-1.10.27.jar                  | a0f0b759d895c15ceb3e3bcb5f3c2db7c582edf0 |
       | LCH   | attributefix                      | 1.0.4                    | AttributeFix-1.12.2-1.0.4.jar                     | d476d1b22b218a10d845928d1665d45fce301b27 |
       | LCH   | atum                              | 2.0.20                   | Atum-1.12.2-2.0.20.jar                            | None                                     |
       | LCH   | mdecore                           | 1.12-1.1                 | mdecore-1.12-1.1.jar                              | None                                     |
       | LCH   | autooredictconv                   | 1.12-1.0.1               | autooredictconv-1.12-1.0.1.jar                    | None                                     |
       | LCH   | autoreglib                        | 1.3-32                   | AutoRegLib-1.3-32.jar                             | None                                     |
       | LCH   | badwithernocookiereloaded         | 1.12.2-3.4.18            | badwithernocookiereloaded-1.12.2-3.4.18.jar       | None                                     |
       | LCH   | battletowers                      | 1.6.5                    | BattleTowers-1.12.2.jar                           | None                                     |
       | LCH   | betterbuilderswands               | 0.13.2                   | BetterBuildersWands-1.12.2-0.13.2.271+5997513.jar | None                                     |
       | LCH   | bettercaves                       | 1.12.2                   | bettercaves-1.12.2-2.0.4.jar                      | None                                     |
       | LCH   | botania                           | r1.10-363                | Botania r1.10-363.jar                             | None                                     |
       | LCH   | mowziesmobs                       | 1.5.8                    | mowziesmobs-1.5.8.jar                             | None                                     |
       | LCH   | patchouli                         | 1.0-23.6                 | Patchouli-1.0-23.6.jar                            | None                                     |
       | LCH   | bewitchment                       | 0.22.63                  | bewitchment-1.12.2-0.0.22.64.jar                  | None                                     |
       | LCH   | bibliocraft                       | 2.4.5                    | BiblioCraft[v2.4.5][MC1.12.2].jar                 | None                                     |
       | LCH   | biomeinfo                         | v1.2.5                   | biomeinfo-1.12.2-v1.2.5.jar                       | None                                     |
       | LCH   | biomesoplenty                     | 7.0.1.2441               | BiomesOPlenty-1.12.2-7.0.1.2441-universal.jar     | None                                     |
       | LCH   | biomestaff                        | 1.0.0                    | BiomeStaff-1.12.2-1.0.0.jar                       | None                                     |
       | LCH   | blockdrops                        | 1.4.0                    | blockdrops-1.12.2-1.4.0.jar                       | None                                     |
       | LCH   | cyclicmagic                       | 1.20.8                   | Cyclic-1.12.2-1.20.8.jar                          | 0e5cb559be7d03f3fc18b8cba547d663e25f28af |
       | LCH   | guideapi                          | 1.12-2.1.8-63            | Guide-API-1.12-2.1.8-63.jar                       | None                                     |
       | LCH   | bloodmagic                        | 1.12.2-2.4.3-105         | BloodMagic-1.12.2-2.4.3-105.jar                   | None                                     |
       | LCH   | bookshelf                         | 2.3.590                  | Bookshelf-1.12.2-2.3.590.jar                      | d476d1b22b218a10d845928d1665d45fce301b27 |
       | LCH   | bountifulbaubles                  | 0.0.1                    | Bountiful Baubles-1.12.2-0.1.6.jar                | None                                     |
       | LCH   | forgelin                          | 1.8.4                    | Forgelin-1.8.4.jar                                | None                                     |
       | LCH   | bountiful                         | 2.2.2                    | Bountiful-2.2.2.jar                               | None                                     |
       | LCH   | brokenwings                       | 2.0.0                    | brokenwings-3.0.0.jar                             | None                                     |
       | LCH   | buildcraftbuilders                | 7.99.24.8                | buildcraft-all-7.99.24.8.jar                      | None                                     |
       | LCH   | buildcrafttransport               | 7.99.24.8                | buildcraft-all-7.99.24.8.jar                      | None                                     |
       | LCH   | buildcraftsilicon                 | 7.99.24.8                | buildcraft-all-7.99.24.8.jar                      | None                                     |
       | LCH   | buildcraftenergy                  | 7.99.24.8                | buildcraft-all-7.99.24.8.jar                      | None                                     |
       | LCH   | reborncore                        | 3.19.5                   | RebornCore-FORK-1.12.2-3.19.5-universal.jar       | None                                     |
       | LCH   | techreborn                        | 2.27.3.1084              | TechReborn-1.12.2-2.27.3.1084-universal.jar       | 8727a3141c8ec7f173b87aa78b9b9807867c4e6b |
       | LCH   | forestry                          | 5.8.2.422                | forestry_1.12.2-5.8.2.422.jar                     | None                                     |
       | LCH   | buildcraftcompat                  | 7.99.24.8                | buildcraft-all-7.99.24.8.jar                      | None                                     |
       | LCH   | buildcraftfactory                 | 7.99.24.8                | buildcraft-all-7.99.24.8.jar                      | None                                     |
       | LCH   | buildcraftrobotics                | 7.99.24.8                | buildcraft-all-7.99.24.8.jar                      | None                                     |
       | LCH   | buildinggadgets                   | 2.8.4                    | BuildingGadgets-2.8.4.jar                         | None                                     |
       | LCH   | capsule                           | 1.12.2-3.3.11            | Capsule-1.12.2-3.3.11.jar                         | None                                     |
       | LCH   | careerbees                        | 1.0                      | careerbees-0.4.0.jar                              | None                                     |
       | LCH   | chameleon                         | 1.12-4.1.3               | Chameleon-1.12-4.1.3.jar                          | None                                     |
       | LCH   | champions                         | 1.12.2-1.0.11.10         | champions-1.12.2-1.0.11.10.jar                    | b33d2c8df492beff56d1bbbc92da49b8ab7345a1 |
       | LCH   | chancecubes                       | 1.12.2-5.0.2.385         | ChanceCubes-1.12.2-5.0.2.385.jar                  | None                                     |
       | LCH   | charm                             | 1.4                      | Charm-1.12.2-1.4.1.jar                            | None                                     |
       | LCH   | cherishedworlds                   | 1.12.2-1.0.1             | cherishedworlds-1.12.2-1.0.1.jar                  | 2484ef4d131fdc0dca0647aa21b7b944ddb935a1 |
       | LCH   | chiselsandbits                    | 14.33                    | chiselsandbits-14.33.jar                          | None                                     |
       | LCH   | chunkpregenerator                 | 2.5.0                    | Chunk Pregenerator-V1.12-2.5.0.jar                | None                                     |
       | LCH   | clumps                            | 3.1.2                    | Clumps-3.1.2.jar                                  | None                                     |
       | LCH   | collective                        | 2.25                     | collective-1.12.2-2.25.jar                        | None                                     |
       | LCH   | cyclopscore                       | 1.6.7                    | CyclopsCore-1.12.2-1.6.7.jar                      | bd0353b3e8a2810d60dd584e256e364bc3bedd44 |
       | LCH   | commoncapabilities                | 2.4.8                    | CommonCapabilities-1.12.2-2.4.8.jar               | bd0353b3e8a2810d60dd584e256e364bc3bedd44 |
       | LCH   | compactmachines3                  | 3.0.18                   | compactmachines3-1.12.2-3.0.18-b278.jar           | None                                     |
       | LCH   | controlling                       | 3.0.10                   | Controlling-3.0.10.jar                            | None                                     |
       | LCH   | cookingforblockheads              | 6.5.0                    | CookingForBlockheads_1.12.2-6.5.0.jar             | None                                     |
       | LCH   | cosmeticarmorreworked             | 1.12.2-v5a               | CosmeticArmorReworked-1.12.2-v5a.jar              | aaaf83332a11df02406e9f266b1b65c1306f0f76 |
       | LCH   | craftingtweaks                    | 8.1.9                    | CraftingTweaks_1.12.2-8.1.9.jar                   | None                                     |
       | LCH   | ctgui                             | 1.0.0                    | CraftTweaker2-1.12-4.1.20.618.jar                 | None                                     |
       | LCH   | crafttweakerjei                   | 2.0.3                    | CraftTweaker2-1.12-4.1.20.618.jar                 | None                                     |
       | LCH   | crimsonwarfare                    | 1.5                      | crimsonwarfare-1.5.jar                            | None                                     |
       | LCH   | cucumber                          | 1.1.3                    | Cucumber-1.12.2-1.1.3.jar                         | None                                     |
       | LCH   | culinaryconstruct                 | 1.3.4                    | culinaryconstruct-1.3.4.jar                       | 2484ef4d131fdc0dca0647aa21b7b944ddb935a1 |
       | LCH   | customizeddungeonloot             | 1.0.3                    | Customized-Dungeon-Loot-1.12 -(v.1.0.3).jar       | None                                     |
       | LCH   | custommainmenu                    | 2.0.9.1                  | CustomMainMenu-MC1.12.2-2.0.9.1.jar               | None                                     |
       | LCH   | waila                             | 1.8.26                   | Hwyla-1.8.26-B41_1.12.2.jar                       | None                                     |
       | LCH   | stg                               | 1.12.2-1.2.3             | stg-1.12.2-1.2.3.jar                              | None                                     |
       | LCH   | mousetweaks                       | 2.10                     | MouseTweaks-2.10-mc1.12.2.jar                     | None                                     |
       | LCH   | danknull                          | 1.7.101                  | DankNull-1.12.2-1.7.101.jar                       | 644f38521a349310a5dae0239577dc7beebefaec |
       | LCH   | darknesslib                       | 1.1.0                    | DarknessLib-1.12.2-1.1.0.jar                      | 220f10d3a93b3ff5fbaa7434cc629d863d6751b9 |
       | LCH   | dimdoors                          | 1.12.2-3.1.2+UNOFFICIAL  | DimensionalDoors-1.12.2-3.1.2-UNOFFICIAL.jar      | None                                     |
       | LCH   | ding                              | 1.0.2                    | Ding-1.12.2-1.0.2.jar                             | 4db5c2bd1b556f252a5b8b54b256d381b2a0a6b8 |
       | LCH   | discordcraft                      | 1.0                      | DiscordCraft-2.0.jar                              | None                                     |
       | LCH   | doggytalents                      | 1.15.1.6                 | DoggyTalents-1.12.2-1.15.1.6.jar                  | None                                     |
       | LCH   | dungeonsmod                       | 1.12.2-1.0.6             | DungeonsMod-1.12.2-1.0.6.jar                      | None                                     |
       | LCH   | dungeontactics                    | DT-0.16.9                | DungeonTactics-1.12.2-0.16.9.jar                  | None                                     |
       | LCH   | eerieentities                     | 1.0.7                    | EerieEntities-1.12.2-1.0.7.jar                    | d476d1b22b218a10d845928d1665d45fce301b27 |
       | LCH   | elenaidodge2                      | 1.0.8b                   | ElenaiDodge2-1.12.2-1.0.8b.jar                    | None                                     |
       | LCH   | enchdesc                          | 1.1.15                   | EnchantmentDescriptions-1.12.2-1.1.15.jar         | d476d1b22b218a10d845928d1665d45fce301b27 |
       | LCH   | enderiobase                       | 5.3.70                   | EnderIO-1.12.2-5.3.70.jar                         | None                                     |
       | LCH   | enderioconduits                   | 5.3.70                   | EnderIO-1.12.2-5.3.70.jar                         | None                                     |
       | LCH   | enderioconduitsappliedenergistics | 5.3.70                   | EnderIO-1.12.2-5.3.70.jar                         | None                                     |
       | LCH   | opencomputers                     | 1.7.5.192                | OpenComputers-MC1.12.2-1.7.5.192.jar              | None                                     |
       | LCH   | enderioconduitsopencomputers      | 5.3.70                   | EnderIO-1.12.2-5.3.70.jar                         | None                                     |
       | LCH   | enderioconduitsrefinedstorage     | 5.3.70                   | EnderIO-1.12.2-5.3.70.jar                         | None                                     |
       | LCH   | enderiointegrationforestry        | 5.3.70                   | EnderIO-1.12.2-5.3.70.jar                         | None                                     |
       | LCH   | enderiointegrationticlate         | 5.3.70                   | EnderIO-1.12.2-5.3.70.jar                         | None                                     |
       | LCH   | enderioinvpanel                   | 5.3.70                   | EnderIO-1.12.2-5.3.70.jar                         | None                                     |
       | LCH   | ftblib                            | 5.4.7.2                  | FTBLib-5.4.7.2.jar                                | None                                     |
       | LCH   | enderiomachines                   | 5.3.70                   | EnderIO-1.12.2-5.3.70.jar                         | None                                     |
       | LCH   | enderiopowertools                 | 5.3.70                   | EnderIO-1.12.2-5.3.70.jar                         | None                                     |
       | LCH   | mcmultipart                       | 2.5.3                    | MCMultiPart-2.5.3.jar                             | None                                     |
       | LCH   | mekanism                          | 1.12.2-9.8.3.390         | Mekanism-1.12.2-9.8.3.390.jar                     | None                                     |
       | LCH   | gasconduits                       | 5.3.70                   | EnderIO-conduits-mekanism-1.12.2-5.3.70.jar       | None                                     |
       | LCH   | enderstorage                      | 2.4.6.137                | EnderStorage-1.12.2-2.4.6.137-universal.jar       | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
       | LCH   | energyconverters                  | 1.3.7.30                 | energyconverters_1.12.2-1.3.7.30.jar              | None                                     |
       | LCH   | erebus                            | 1.0.32                   | Erebus-1.0.32.jar                                 | None                                     |
       | LCH   | erebusfix                         | 1.12.2-0.0.0.1           | erebusfix-1.12.2-0.0.0.1.jar                      | None                                     |
       | LCH   | extrabitmanipulation              | 1.12.2-3.4.1             | ExtraBitManipulation-1.12.2-3.4.1.jar             | None                                     |
       | LCH   | extracells                        | 2.6.5                    | ExtraCells-1.12.2-2.6.5.jar                       | None                                     |
       | LCH   | extrautils2                       | 1.0                      | extrautils2-1.12-1.9.9.jar                        | None                                     |
       | LCH   | fairylights                       | 2.1.10                   | fairylights-2.2.0-1.12.2.jar                      | None                                     |
       | LCH   | farmingforblockheads              | 3.1.28                   | FarmingForBlockheads_1.12.2-3.1.28.jar            | None                                     |
       | LCH   | farseek                           | 2.5.1                    | Farseek-1.12-2.5.1.jar                            | None                                     |
       | LCH   | mod_lavacow                       | 1.2.4                    | Fish's Undead Rising-1.2.4a.jar                   | None                                     |
       | LCH   | sonarcore                         | 5.0.19                   | sonarcore-1.12.2-5.0.19-20.jar                    | None                                     |
       | LCH   | fluxnetworks                      | 4.1.0                    | FluxNetworks-1.12.2-4.1.1.34.jar                  | None                                     |
       | LCH   | forgemultipartcbe                 | 2.6.2.83                 | ForgeMultipart-1.12.2-2.6.2.83-universal.jar      | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
       | LCH   | microblockcbe                     | 2.6.2.83                 | ForgeMultipart-1.12.2-2.6.2.83-universal.jar      | None                                     |
       | LCH   | minecraftmultipartcbe             | 2.6.2.83                 | ForgeMultipart-1.12.2-2.6.2.83-universal.jar      | None                                     |
       | LCH   | fossil                            | 8.0.5                    | fossilsarcheology-8.0.5.jar                       | None                                     |
       | LCH   | from_the_depths                   | @VERSION@                | from_the_depths-1.2.1.0.jar                       | None                                     |
       | LCH   | iceologer                         | 1.5                      | Frozen-Fiend-1.5.jar                              | None                                     |
       | LCH   | ftbutilities                      | 5.4.1.131                | FTBUtilities-5.4.1.131.jar                        | None                                     |
       | LCH   | itemfilters                       | 1.0.4.2                  | ItemFilters-1.0.4.2.jar                           | None                                     |
       | LCH   | reskillable                       | 1.12.2-1.13.0            | Reskillable-1.12.2-1.13.0.jar                     | None                                     |
       | LCH   | ftbquests                         | 1202.9.0.15              | FTBQuests-1202.9.0.15.jar                         | None                                     |
       | LCH   | ftbmoney                          | 1.2.0.47                 | FTBMoney-1.2.0.47.jar                             | None                                     |
       | LCH   | futuremc                          | 0.2.6                    | future-mc-1.12.2-0.2.6.1.jar                      | None                                     |
       | LCH   | gendustry                         | 1.6.5.8                  | gendustry-1.6.5.8-mc1.12.2.jar                    | None                                     |
       | LCH   | ghostsexplosives                  | 2.3.0 - MC 1.12.2        | Ghost's Explosives 2.3.0 - MC1.12.2.jar           | None                                     |
       | LCH   | gottschcore                       | 1.14.0                   | GottschCore-mc1.12.2-f14.23.5.2854-v1.14.0.jar    | None                                     |
       | LCH   | grue                              | 1.8.0                    | Grue-1.12.2-1.8.0.jar                             | 220f10d3a93b3ff5fbaa7434cc629d863d6751b9 |
       | LCH   | guardillagers                     | 1.0.1                    | guardillagers-1.12.2-1.0.1.jar                    | None                                     |
       | LCH   | gunpowderlib                      | 1.12.2-1.1               | GunpowderLib-1.12.2-1.1.jar                       | 4ffa87db52cf086d00ecc4853a929367b1c39b5c |
       | LCH   | hardcoredarkness                  | 2.0                      | HardcoreDarkness-MC1.12.2-2.0.jar                 | d72e0dd57935b3e9476212aea0c0df352dd76291 |
       | LCH   | ichunutil                         | 7.2.2                    | iChunUtil-1.12.2-7.2.2.jar                        | 4db5c2bd1b556f252a5b8b54b256d381b2a0a6b8 |
       | LCH   | hats                              | 7.1.1                    | Hats-1.12.2-7.1.1.jar                             | 4db5c2bd1b556f252a5b8b54b256d381b2a0a6b8 |
       | LCH   | hole_filler_mod                   | 1.0                      | hole_filler_mod-1.2.4.jar                         | None                                     |
       | LCH   | hunterillager                     | 1.2                      | hunterillager-1.12.2-1.2.jar                      | None                                     |
       | LCH   | icbmclassic                       | 1.12.2-4.0.1.75          | ICBM-classic-1.12.2-4.0.1b75.jar                  | None                                     |
       | LCH   | illagers_plus                     | 1.1                      | IllagersPlus-1.12.2-1.1.3.jar                     | None                                     |
       | LCH   | immersiveengineering              | 0.12-98                  | ImmersiveEngineering-0.12-98.jar                  | None                                     |
       | LCH   | immersivecables                   | 1.3.2                    | ImmersiveCables-1.12.2-1.3.2.jar                  | None                                     |
       | LCH   | immersiveintelligence             | 0.1.1                    | immersiveintelligence-1.12.2-0.1.1.jar            | None                                     |
       | LCH   | immersivepetroleum                | 1.1.9                    | immersivepetroleum-1.12.2-1.1.9.jar               | None                                     |
       | LCH   | immersiveposts                    | 0.2.1                    | ImmersivePosts-0.2.1.jar                          | 0ba8738eadcf158e7fe1452255a73a022fb15feb |
       | LCH   | improvedbackpacks                 | 1.12.2-1.5.0.0           | ImprovedBackpacks-1.12.2-1.5.0.0.jar              | None                                     |
       | LCH   | incontrol                         | 3.9.18                   | incontrol-1.12-3.9.18.jar                         | None                                     |
       | LCH   | teslacorelib                      | 1.0.17                   | tesla-core-lib-1.12.2-1.0.17.jar                  | d476d1b22b218a10d845928d1665d45fce301b27 |
       | LCH   | industrialforegoing               | 1.12.2-1.12.2            | industrialforegoing-1.12.2-1.12.13-237.jar        | None                                     |
       | LCH   | instantunify                      | 1.1.2                    | instantunify-1.12.2-1.1.2.jar                     | None                                     |
       | LCH   | instrumentalmobs                  | 1.2                      | Instrumental-Mobs-1.2.1.jar                       | None                                     |
       | LCH   | integrateddynamics                | 1.1.11                   | IntegratedDynamics-1.12.2-1.1.11.jar              | bd0353b3e8a2810d60dd584e256e364bc3bedd44 |
       | LCH   | integrateddynamicscompat          | 1.0.0                    | IntegratedDynamics-1.12.2-1.1.11.jar              | None                                     |
       | LCH   | integratedtunnels                 | 1.6.14                   | IntegratedTunnels-1.12.2-1.6.14.jar               | bd0353b3e8a2810d60dd584e256e364bc3bedd44 |
       | LCH   | integratedtunnelscompat           | 1.0.0                    | IntegratedTunnels-1.12.2-1.6.14.jar               | None                                     |
       | LCH   | mysticalagriculture               | 1.7.5                    | MysticalAgriculture-1.12.2-1.7.5.jar              | None                                     |
       | LCH   | mysticalagradditions              | 1.3.2                    | MysticalAgradditions-1.12.2-1.3.2.jar             | None                                     |
       | LCH   | nuclearcraft                      | 2.18y                    | NuclearCraft-2.18y-1.12.2.jar                     | None                                     |
       | LCH   | harvestcraft                      | 1.12.2zb                 | Pam's HarvestCraft 1.12.2zg.jar                   | None                                     |
       | LCH   | randomthings                      | 4.2.7.4                  | RandomThings-MC1.12.2-4.2.7.4.jar                 | d72e0dd57935b3e9476212aea0c0df352dd76291 |
       | LCH   | mcjtylib_ng                       | 3.5.4                    | mcjtylib-1.12-3.5.4.jar                           | None                                     |
       | LCH   | rftools                           | 7.73                     | rftools-1.12-7.73.jar                             | None                                     |
       | LCH   | integrationforegoing              | 1.12.2-1.11              | IntegrationForegoing-1.12.2-1.11.jar              | 4ffa87db52cf086d00ecc4853a929367b1c39b5c |
       | LCH   | inventorypets                     | 2.0.12                   | inventorypets-1.12-2.0.12.jar                     | None                                     |
       | LCH   | inventorytweaks                   | 1.63+release.109.220f184 | InventoryTweaks-1.63.jar                          | 55d2cd4f5f0961410bf7b91ef6c6bf00a766dcbe |
       | LCH   | ironchest                         | 1.12.2-7.0.67.844        | ironchest-1.12.2-7.0.72.847.jar                   | None                                     |
       | LCH   | itlt                              | 1.0.3                    | itlt-1.12.2-1.0.3.jar                             | None                                     |
       | LCH   | jaopca                            | 1.12.2-2.2.8.103         | JAOPCA-1.12.2-2.2.8.103.jar                       | None                                     |
       | LCH   | oredictinit                       | 1.12.2-2.2.1.71          | JAOPCA-1.12.2-2.2.8.103.jar                       | None                                     |
       | LCH   | jeibees                           | 0.9.0.5                  | jeibees-0.9.0.5-mc1.12.2.jar                      | None                                     |
       | LCH   | journeymap                        | 1.12.2-5.7.1             | journeymap-1.12.2-5.7.1.jar                       | None                                     |
       | LCH   | jehc                              | 1.7.2                    | just-enough-harvestcraft-1.12.2-1.7.2.jar         | None                                     |
       | LCH   | jecalculation                     | 1.12.2-3.2.5             | JustEnoughCalculation-1.12.2-3.2.5.jar            | None                                     |
       | LCH   | jee                               | 1.0.8                    | JustEnoughEnergistics-1.12.2-1.0.8.jar            | None                                     |
       | LCH   | jeresources                       | 0.9.2.60                 | JustEnoughResources-1.12.2-0.9.2.60.jar           | None                                     |
       | LCH   | laggoggles                        | FAT-1.12.2-4.11-92       | LagGoggles-FAT-1.12.2-4.11-92.jar                 | None                                     |
       | LCH   | letsencryptcraft                  | @VERSION@                | letsencryptcraft-1.10.2-1.2.0.jar                 | None                                     |
       | LCH   | levelup2                          | ${version}               | levelup2-1.5.8.jar                                | None                                     |
       | LCH   | littletiles                       | 1.5.0                    | LittleTiles_v1.5.0-pre327_mc1.12.2.jar            | None                                     |
       | LCH   | lodsofemone                       | 0.1                      | LodsOfEmone-0.1.jar                               | None                                     |
       | LCH   | login_shield                      | 1.12.2-6-g5654706        | Login_Shield-1.12.2-6-g5654706.jar                | None                                     |
       | LCH   | lootcapacitortooltips             | 1.3                      | lootcapacitortooltips-1.3.jar                     | None                                     |
       | LCH   | timecore                          | 1.0.1.1                  | TimeCore-1.12.2-1.0.1.1.jar                       | None                                     |
       | LCH   | lootgames                         | 1.0.3.1                  | LootGames-1.12.2-1.0.3.1.jar                      | None                                     |
       | LCH   | lostmagic                         | 1.0                      | lostmagic-1.0.2.jar                               | None                                     |
       | LCH   | magicbees                         | 1.0                      | MagicBees-1.12.2-3.1.10.jar                       | None                                     |
       | LCH   | malisiscore                       | 1.12.2-6.5.1-SNAPSHOT    | malisiscore-1.12.2-6.5.1.jar                      | None                                     |
       | LCH   | malisisdoors                      | 1.12.2-7.3.0             | malisisdoors-1.12.2-7.3.0.jar                     | None                                     |
       | LCH   | maxpotidext                       | 1.0.3                    | maxpotidext-1.0.3.jar                             | b851b8b7c7f4d8d0e910ff27618150ba80c026ec |
       | LCH   | immersivetech                     | 1.8.94                   | MCTImmersiveTechnology-1.12.2-1.8.94.jar          | None                                     |
       | LCH   | mcwroofs                          | 1.0.2                    | mcw-roofs-1.0.2-mc1.12.2.jar                      | None                                     |
       | LCH   | mekanismgenerators                | 1.12.2-9.8.3.390         | MekanismGenerators-1.12.2-9.8.3.390.jar           | None                                     |
       | LCH   | mekanismtools                     | 1.12.2-9.8.3.390         | MekanismTools-1.12.2-9.8.3.390.jar                | None                                     |
       | LCH   | menumobs                          | 1.21                     | MenuMobs-1.12.2-1.21.jar                          | None                                     |
       | LCH   | moartinkers                       | 0.6.0                    | moartinkers-0.6.0.jar                             | None                                     |
       | LCH   | mob_grinding_utils                | 0.3.13                   | MobGrindingUtils-0.3.13.jar                       | None                                     |
       | LCH   | numina                            | 1.12.2-1.0.38            | Numina-1.12.2-1.0.38.jar                          | None                                     |
       | LCH   | powersuits                        | 1.12.2-1.0.46            | ModularPowersuits-1.12.2-1.0.46.jar               | None                                     |
       | LCH   | moreoverlays                      | 1.15.1                   | moreoverlays-1.15.1-mc1.12.2.jar                  | None                                     |
       | LCH   | guilib                            | $version                 | morepaintings-paintings-1.12.2-5.0.1.2.jar        | None                                     |
       | LCH   | paintingselgui                    | $version                 | morepaintings-paintings-1.12.2-5.0.1.2.jar        | None                                     |
       | LCH   | morepaintings                     | $version                 | morepaintings-paintings-1.12.2-5.0.1.2.jar        | None                                     |
       | LCH   | morpheus                          | 1.12.2-3.5.106           | Morpheus-1.12.2-3.5.106.jar                       | None                                     |
       | LCH   | mputils                           | 1.5.6                    | MPUtils-1.12.2-1.5.7.jar                          | None                                     |
       | LCH   | multimob                          | 1.0.5                    | multimob-1.0.5.jar                                | None                                     |
       | LCH   | naturesaura                       | 18.1                     | NaturesAura-18.1.jar                              | None                                     |
       | LCH   | naturescompass                    | 1.8.5                    | NaturesCompass-1.12.2-1.8.5.jar                   | None                                     |
       | LCH   | netherportalfix                   | 5.3.17                   | NetherPortalFix_1.12.1-5.3.17.jar                 | None                                     |
       | LCH   | netherportalspread                | 5.1                      | netherportalspread_1.12.2-5.1.jar                 | None                                     |
       | LCH   | recipehandler                     | 0.13                     | NoMoreRecipeConflict-0.13(1.12.2).jar             | None                                     |
       | LCH   | norecipebook                      | 1.2.1                    | noRecipeBook_v1.2.2formc1.12.2.jar                | None                                     |
       | LCH   | neid                              | 1.5.4.4                  | NotEnoughIDs-1.5.4.4.jar                          | None                                     |
       | LCH   | oldjava                           | 1.1.11                   | OldJavaWarning-1.12.2-1.1.11.jar                  | d476d1b22b218a10d845928d1665d45fce301b27 |
       | LCH   | omlib                             | 3.1.4-249                | omlib-1.12.2-3.1.4-249.jar                        | None                                     |
       | LCH   | openmods                          | 0.12.2                   | OpenModsLib-1.12.2-0.12.2.jar                     | d2a9a8e8440196e26a268d1f3ddc01b2e9c572a5 |
       | LCH   | openblocks                        | 1.8.1                    | OpenBlocks-1.12.2-1.8.1.jar                       | d2a9a8e8440196e26a268d1f3ddc01b2e9c572a5 |
       | LCH   | openmodularturrets                | 3.1.12-378               | openmodularturrets-1.12.2-3.1.12-378.jar          | None                                     |
       | LCH   | oreexcavation                     | 1.4.150                  | OreExcavation-1.4.150.jar                         | None                                     |
       | LCH   | packmode                          | 1.2.0                    | packmode-1.12.2-1.2.0.jar                         | None                                     |
       | LCH   | packmodemenu                      | 1.0.4                    | PackModeMenu-1.0.4.jar                            | None                                     |
       | LCH   | pamscookables                     | 1.1                      | pamscookables-1.1.jar                             | None                                     |
       | LCH   | pigstep                           | 1.12                     | pigstep-1.12.jar                                  | None                                     |
       | LCH   | placebo                           | 1.6.0                    | Placebo-1.12.2-1.6.0.jar                          | None                                     |
       | LCH   | thermaldynamics                   | 2.5.6                    | ThermalDynamics-1.12.2-2.5.6.1-universal.jar      | None                                     |
       | LCH   | simplyjetpacks                    | 2.2.14.67                | SimplyJetpacks2-1.12.2-2.2.14.67.jar              | None                                     |
       | LCH   | plustic                           | 8.0.1.0                  | plustic-8.0.1.0.jar                               | None                                     |
       | LCH   | portalgun                         | 7.1.0                    | PortalGun-1.12.2-7.1.0.jar                        | 4db5c2bd1b556f252a5b8b54b256d381b2a0a6b8 |
       | LCH   | potioncore                        | 1.9_for_1.12.2           | PotionCore-1.9_for_1.12.2.jar                     | None                                     |
       | LCH   | practicallogistics2               | 3.0.8                    | practicallogistics2-1.12.2-3.0.8-11.jar           | None                                     |
       | LCH   | primitivemobs                     | 1.2.3a                   | primitivemobs-1.2.3a.jar                          | None                                     |
       | LCH   | progressivebosses                 | 1.5.4                    | ProgressiveBosses-1.5.4-mc1.12.x.jar              | None                                     |
       | LCH   | quarkoddities                     | 1                        | QuarkOddities-1.12.2.jar                          | None                                     |
       | LCH   | rats                              | 3.2.14                   | rats-3.2.14-1.12.2.jar                            | None                                     |
       | LCH   | reccomplex                        | 1.4.8.2                  | RecurrentComplex-1.4.8.2.jar                      | None                                     |
       | LCH   | xreliquary                        | 1.12.2-1.3.4.796         | Reliquary-1.12.2-1.3.4.796.jar                    | None                                     |
       | LCH   | resourceloader                    | 1.5.3                    | ResourceLoader-MC1.12.1-1.5.3.jar                 | d72e0dd57935b3e9476212aea0c0df352dd76291 |
       | LCH   | rftoolsdim                        | 5.71                     | rftoolsdim-1.12-5.71.jar                          | None                                     |
       | LCH   | roguelike                         | 2.3.2                    | RoguelikeDungeonsFnarEdition-1.12.2-2.3.2.jar     | None                                     |
       | LCH   | savemystronghold                  | 1.12.2-1.0.0             | savemystronghold-1.12.2-1.0.0.jar                 | None                                     |
       | LCH   | scannable                         | 1.6.3.26                 | Scannable-MC1.12.2-1.6.3.26.jar                   | None                                     |
       | LCH   | signpost                          | 1.08.3                   | signpost-1.12.2-1.08.3.jar                        | None                                     |
       | LCH   | storagenetwork                    | 1.8.1                    | SimpleStorageNetwork-1.12.2-1.8.1.jar             | 0e5cb559be7d03f3fc18b8cba547d663e25f28af |
       | LCH   | simplycats                        | 1.12.2-0.0.3.1           | simplycats-1.12.2-0.0.3.1.jar                     | None                                     |
       | LCH   | stevescarts                       | 2.4.32.137               | StevesCarts-1.12.2-2.4.32.137.jar                 | None                                     |
       | LCH   | storagedrawers                    | 5.2.2                    | StorageDrawers-1.12.2-5.4.2.jar                   | None                                     |
       | LCH   | storagedrawersextra               | @VERSION@                | StorageDrawersExtras-1.12-3.1.0.jar               | None                                     |
       | LCH   | streams                           | 0.4.9                    | Streams-1.12-0.4.9.jar                            | None                                     |
       | LCH   | stupidthings                      | 1.1.6                    | Stupid Things-1.12.2-1.1.6.jar                    | None                                     |
       | LCH   | stygian                           | 1.0.4                    | stygian-1.0.4.jar                                 | None                                     |
       | LCH   | taiga                             | 1.12.2-1.3.3             | taiga-1.12.2-1.3.4.jar                            | None                                     |
       | LCH   | tfspellpack                       | 1.1.0                    | TFSpellPack-1.1.0-MC1.12.2.jar                    | None                                     |
       | LCH   | thaumicaugmentation               | 1.12.2-2.0.13            | ThaumicAugmentation-1.12.2-2.0.13.jar             | 8f678591ba6f78d579e553a8aa94b4c4766cb13d |
       | LCH   | thaumicjei                        | 1.6.0                    | ThaumicJEI-1.12.2-1.6.0-27.jar                    | None                                     |
       | LCH   | thaumicperiphery                  | 0.3.1                    | thaumicperiphery-0.3.1.jar                        | None                                     |
       | LCH   | beneath                           | 1.7.0                    | The Beneath-1.12.2-1.7.0.jar                      | 220f10d3a93b3ff5fbaa7434cc629d863d6751b9 |
       | LCH   | theaurorian                       | 1.12.2-Release           | theaurorian-1.12.2-release-mar2321.jar            | None                                     |
       | LCH   | thermalcultivation                | 0.3.6                    | ThermalCultivation-1.12.2-0.3.6.1-universal.jar   | None                                     |
       | LCH   | thermalinnovation                 | 0.3.6                    | ThermalInnovation-1.12.2-0.3.6.1-universal.jar    | None                                     |
       | LCH   | thesummoner                       | 1.0.1-beta               | thesummoner-1.0.1.jar                             | None                                     |
       | LCH   | tinkersjei                        | 1.2                      | tinkersjei-1.2.jar                                | None                                     |
       | LCH   | tinkertoolleveling                | 1.12.2-1.1.0.DEV.b23e769 | TinkerToolLeveling-1.12.2-1.1.0.jar               | None                                     |
       | LCH   | tips                              | 1.0.9                    | Tips-1.12.2-1.0.9.jar                             | d476d1b22b218a10d845928d1665d45fce301b27 |
       | LCH   | totemic                           | 1.12.2-0.11.6            | Totemic-1.12.2-0.11.6.jar                         | 21d11d7bf4d97b465382a1f95428029aac6daaea |
       | LCH   | treasure2                         | 1.16.0                   | Treasure2-mc1.12.2-f14.23.5.2854-v1.16.0.jar      | None                                     |
       | LCH   | treechop                          | 0.14.4                   | TreeChop-1.12.2-0.14.4.jar                        | None                                     |
       | LCH   | vampiresneedumbrellas             | 1.4                      | VampiresNeedUmbrellas-1.12.2-1.5.jar              | None                                     |
       | LCH   | vampirism                         | 1.6.2                    | Vampirism-1.12.2-1.6.2.jar                        | None                                     |
       | LCH   | teamlapen-lib                     | 1.6.2                    | Vampirism-1.12.2-1.6.2.jar                        | None                                     |
       | LCH   | vampirism_integrations            | vampirism_integrations   | VampirismIntegrations-1.12.2-1.3.0.jar            | None                                     |
       | LCH   | vanillafix                        | 1.0.10-150               | VanillaFix-1.0.10-150.jar                         | None                                     |
       | LCH   | villagenames                      | 4.1.5                    | VillageNames-1.12.2-4.1.5.jar                     | None                                     |
       | LCH   | gvc                               | 1.2.5                    | Voice Chat Reloaded-1.2.5.jar                     | None                                     |
       | LCH   | wailaharvestability               | 1.1.12                   | WailaHarvestability-mc1.12-1.1.12.jar             | None                                     |
       | LCH   | wanionlib                         | 1.12.2-2.5               | WanionLib-1.12.2-2.5.jar                          | None                                     |
       | LCH   | waystones                         | 4.1.0                    | Waystones_1.12.2-4.1.0.jar                        | None                                     |
       | LCH   | wings                             | 1.1.6                    | wings-1.1.6-1.12.2.jar                            | None                                     |
       | LCH   | mowzies_wings                     | 1.0.0                    | wings-1.1.6-1.12.2.jar                            | None                                     |
       | LCH   | bauble_wings                      | 1.0.0                    | wings-1.1.6-1.12.2.jar                            | None                                     |
       | LCH   | wct                               | 3.12.97                  | WirelessCraftingTerminal-1.12.2-3.12.97.jar       | 186bc454cd122c9c2f1aa4f95611254bcc543363 |
       | LCH   | witherskelefix                    | 2.6.3                    | WitherSkeletonTweaks-1.12.2-2.6.3.jar             | None                                     |
       | LCH   | wgblockreplacer                   | 2.2.0                    | WorldgenBlockReplacer-1.12.2-2.2.0.jar            | None                                     |
       | LCH   | wrcbe                             | 2.3.2                    | WR-CBE-1.12.2-2.3.2.33-universal.jar              | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
       | LCH   | xnet                              | 1.8.2                    | xnet-1.12-1.8.2.jar                               | None                                     |
       | LCH   | yabba                             | 1.1.2.54                 | YABBA-1.1.2.54.jar                                | None                                     |
       | LCH   | ynot                              | 0.2.4                    | YNot-0.2.4.jar                                    | None                                     |
       | LCH   | yoyos                             | 1.12.2-1.3.3.25          | yoyos_1.12.2-1.3.3.25.jar                         | None                                     |
       | LCH   | zerocore                          | 1.12.2-0.1.2.9           | zerocore-1.12.2-0.1.2.9.jar                       | None                                     |
       | LCH   | lemonlib                          | 1.3.0                    | lemonlib-1.12.2-1.3.0.jar                         | None                                     |
       | LCH   | arcaneworld                       | 0.0.11                   | arcaneworld-1.12.2-0.0.11.jar                     | None                                     |
       | LCH   | rf-capability-adapter             | 1.1.1                    | capabilityadapter-1.1.1.jar                       | None                                     |
       | LCH   | structurize                       | 1.12.2-0.10.277-RELEASE  | structurize-1.12.2-0.10.277-RELEASE.jar           | None                                     |
       | LCH   | minecolonies                      | 1.12.2-0.11.811-BETA     | minecolonies-1.12.2-0.11.811-BETA-universal.jar   | None                                     |
       | LCH   | phosphor-lighting                 | 1.12.2-0.2.6             | phosphor-1.12.2-0.2.6+build50-universal.jar       | f0387d288626cc2d937daa504e74af570c52a2f1 |
       | LCH   | reauth                            | 3.6.0                    | reauth-3.6.0.jar                                  | daba0ec4df71b6da841768c49fb873def208a1e3 |
       | LCH   | solcarrot                         | 1.8.4                    | solcarrot-1.12.2-1.8.4.jar                        | None                                     |
       | LCH   | techreborn_compat                 | 1.0.0                    | TechReborn-ModCompatibility-1.12.2-1.4.0.76.jar   | 8727a3141c8ec7f173b87aa78b9b9807867c4e6b |
       | LCH   | thebetweenlands                   | 3.7.3                    | TheBetweenlands-3.7.3-universal.jar               | 38067d6878811efb38b6a045521cfd80b9b60b38 |
       | LCH   | midnight                          | 0.3.5                    | themidnight-0.3.5.jar                             | None                                     |
       | LCH   | armoryexpansion-conarm            | 1.4.2                    | armoryexpansion-1.4.2.jar                         | None                                     |
       | LCH   | mysticallib                       | 1.12.2-1.10.0            | mysticallib-1.12.2-1.10.0.jar                     | None                                     |
       | LCH   | teslacorelib_registries           | 1.0.17                   | tesla-core-lib-1.12.2-1.0.17.jar                  | None                                     |
       | LCH   | tweakersconstructpostload         | 1.12.2-1.6.0             | tweakersconstruct-1.12.2-1.6.0.jar                | None                                     |
       | LCH   | unidict                           | 1.12.2-3.0.7             | UniDict-1.12.2-3.0.7.jar                          | None                                     |
       | LCH   | wrapup                            | 1.12-1.1.3               | WrapUp-1.12-1.1.3.jar                             | None                                     |
       | UD    | mdecore-core                      | 1.0                      | minecraft.jar                                     | None                                     |
       | UD    | mobends_wings                     | 1.0.0                    | wings-1.1.6-1.12.2.jar                            | None                                     |
  Loaded coremods (and transformers): wings (wings-1.1.6-1.12.2.jar)
                                        me.paulf.wings.server.asm.WingsRuntimePatcher
                                        me.paulf.wings.server.asm.mobends.WingsMoBendsRuntimePatcher
                                      IELoadingPlugin (ImmersiveEngineering-core-0.12-98.jar)
                                        blusunrize.immersiveengineering.common.asm.IEClassTransformer
                                      TransformerLoader (OpenComputers-MC1.12.2-1.7.5.192.jar)
                                        li.cil.oc.common.asm.ClassTransformer
                                      Thaumic Augmentation Core Plugin (ThaumicAugmentation-1.12.2-2.0.13.jar)
                                        thecodex6824.thaumicaugmentation.core.TATransformer
                                      MekanismCoremod (Mekanism-1.12.2-9.8.3.390.jar)
                                        mekanism.coremod.KeybindingMigrationHelper
                                      LittlePatchingLoader (LittleTiles_v1.5.0-pre327_mc1.12.2.jar)
                                        com.creativemd.littletiles.LittleTilesTransformer
                                      BewitchmentFMLLoadingPlugin (bewitchment-1.12.2-0.0.22.64.jar)
                                        
                                      Quark Plugin (Quark-r1.6-179.jar)
                                        vazkii.quark.base.asm.ClassTransformer
                                      AppleCore (AppleCore-mc1.12.2-3.4.0.jar)
                                        squeek.applecore.asm.TransformerModuleHandler
                                      ObfuscatePlugin (obfuscate-0.4.2-1.12.2.jar)
                                        com.mrcrayfish.obfuscate.asm.ObfuscateTransformer
                                      iceandfire (iceandfire-1.9.1-1.12.2.jar)
                                        com.github.alexthe666.iceandfire.patcher.IceAndFireRuntimePatcher
                                      Inventory Tweaks Coremod (InventoryTweaks-1.63.jar)
                                        invtweaks.forge.asm.ContainerTransformer
                                      EnderCorePlugin (EnderCore-1.12.2-0.5.76-core.jar)
                                        com.enderio.core.common.transform.EnderCoreTransformer
                                        com.enderio.core.common.transform.SimpleMixinPatcher
                                      PhosphorFMLLoadingPlugin (phosphor-1.12.2-0.2.6+build50-universal.jar)
                                        
                                      ratscore (rats-3.2.14-1.12.2.jar)
                                        com.github.alexthe666.rats.server.misc.RatsRuntimePatcher
                                      LevelUpCore (levelup2-1.5.8.jar)
                                        
                                      LoadingPlugin (ResourceLoader-MC1.12.1-1.5.3.jar)
                                        lumien.resourceloader.asm.ClassTransformer
                                      MalisisCorePlugin (malisiscore-1.12.2-6.5.1.jar)
                                        
                                      CoreMod (Aroma1997Core-1.12.2-2.0.0.2.b167.jar)
                                        
                                      LoadingPlugin (HardcoreDarkness-MC1.12.2-2.0.jar)
                                        lumien.hardcoredarkness.asm.ClassTransformer
                                      CreativePatchingLoader (CreativeCore_v1.10.47_mc1.12.2.jar)
                                        
                                      IvToolkit (IvToolkit-1.3.3-1.12.jar)
                                        
                                      LoadingPlugin (Reskillable-1.12.2-1.13.0.jar)
                                        codersafterdark.reskillable.base.asm.ClassTransformer
                                      ColorUtilityCorePlugin (ColorUtility-universal-1.0.4.jar)
                                        com.Axeryok.ColorUtility.ColorUtilityTransformer
                                      FutureMC (future-mc-1.12.2-0.2.6.1.jar)
                                        thedarkcolour.futuremc.asm.CoreTransformer
                                      HCASM (HammerLib-1.12.2-2.0.6.26.jar)
                                        com.zeitheron.hammercore.asm.HammerCoreTransformer
                                      LoadingPlugin (RandomThings-MC1.12.2-4.2.7.4.jar)
                                        lumien.randomthings.asm.ClassTransformer
                                      ErebusFix Mixin Loading Plugin (erebusfix-1.12.2-0.0.0.1.jar)
                                        
                                      RandomPatches (randompatches-1.12.2-1.22.1.10.jar)
                                        com.therandomlabs.randompatches.core.RPTransformer
                                      ForgelinPlugin (Forgelin-1.8.4.jar)
                                        
                                      midnight (themidnight-0.3.5.jar)
                                        com.mushroom.midnight.core.transformer.MidnightClassTransformer
                                      OpenModsCorePlugin (OpenModsLib-1.12.2-0.12.2.jar)
                                        openmods.core.OpenModsClassTransformer
                                      CorePlugin (ForgeEndertech-1.12.2-4.5.5.0-build.0561.jar)
                                        
                                      CTMCorePlugin (CTM-MC1.12.2-1.0.2.31.jar)
                                        team.chisel.ctm.client.asm.CTMTransformer
                                      FarseekCoreMod (Farseek-1.12-2.5.1.jar)
                                        farseek.core.FarseekClassTransformer
                                      TheBetweenlandsLoadingPlugin (TheBetweenlands-3.7.3-SNAPSHOT-20210322.082210-core.jar)
                                        thebetweenlands.core.TheBetweenlandsClassTransformer
                                      AdvancedRocketryPlugin (AdvancedRocketry-1.12.2-1.7.0-232-universal.jar)
                                        zmaster587.advancedRocketry.asm.ClassTransformer
                                      CharmLoadingPlugin (Charm-1.12.2-1.4.1.jar)
                                        svenhjol.charm.base.CharmClassTransformer
                                      Plugin (NotEnoughIDs-1.5.4.4.jar)
                                        ru.fewizz.neid.asm.Transformer
                                      llibrary (llibrary-core-1.0.11-1.12.2.jar)
                                        net.ilexiconn.llibrary.server.core.plugin.LLibraryTransformer
                                        net.ilexiconn.llibrary.server.core.patcher.LLibraryRuntimePatcher
                                      AstralCore (astralsorcery-1.12.2-1.10.27.jar)
                                        
                                      MDECore-Core (mdecore-1.12-1.1.jar)
                                        com.mattdahepic.mdecore.asm.TickrateTransformer
                                      VanillaFixLoadingPlugin (VanillaFix-1.0.10-150.jar)
                                        
                                      Max Potion ID Extender (maxpotidext-1.0.3.jar)
                                        zabi.minecraft.maxpotidext.MPIDTransformer
  GL info: ' Vendor: 'NVIDIA Corporation' Version: '4.6.0 NVIDIA 471.68' Renderer: 'NVIDIA GeForce RTX 2060/PCIe/SSE2'
  OpenModsLib class transformers: [llama_null_fix:FINISHED],[horse_base_null_fix:FINISHED],[pre_world_render_hook:FINISHED],[player_render_hook:FINISHED],[horse_null_fix:FINISHED]
  AE2 Version: stable rv6-stable-7 for Forge 14.23.5.2768
  Ender IO: No known problems detected.
            Authlib is : /C:/Users/Jeremy/curseforge/minecraft/Install/libraries/com/mojang/authlib/1.5.25/authlib-1.5.25.jar
            
            !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
            !!!You are looking at the diagnostics information, not at the crash.       !!!
            !!!Scroll up until you see the line with '---- Minecraft Crash Report ----'!!!
            !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
  Pulsar/tconstruct loaded Pulses: - TinkerCommons (Enabled/Forced)
                                   - TinkerWorld (Enabled/Not Forced)
                                   - TinkerTools (Enabled/Not Forced)
                                   - TinkerHarvestTools (Enabled/Forced)
                                   - TinkerMeleeWeapons (Enabled/Forced)
                                   - TinkerRangedWeapons (Enabled/Forced)
                                   - TinkerModifiers (Enabled/Forced)
                                   - TinkerSmeltery (Enabled/Not Forced)
                                   - TinkerGadgets (Enabled/Not Forced)
                                   - TinkerOredict (Enabled/Forced)
                                   - TinkerIntegration (Enabled/Forced)
                                   - TinkerFluids (Enabled/Forced)
                                   - TinkerMaterials (Enabled/Forced)
                                   - TinkerModelRegister (Enabled/Forced)
                                   - chiselIntegration (Enabled/Not Forced)
                                   - chiselsandbitsIntegration (Enabled/Not Forced)
                                   - craftingtweaksIntegration (Enabled/Not Forced)
                                   - wailaIntegration (Enabled/Not Forced)
                                   - quarkIntegration (Enabled/Not Forced)
  HammerCore Debug Information: Dependent Mods:
                                -Thaumic Additions: Reconstructed (thaumadditions) @ 12.6.6
  List of loaded APIs: * actuallyadditionsapi (34) from ActuallyAdditions-1.12.2-r152.jar
                       * ae2wtlib|API (1.0.34) from AE2WTLib-1.12.2-1.0.34.jar
                       * AgriCraftAPI (1.0) from AgriCraft-2.12.0-1.12.0-a6.jar
                       * AppleCoreAPI (3.4.0) from AppleCore-mc1.12.2-3.4.0.jar
                       * appliedenergistics2|API (rv6) from appliedenergistics2-rv6-stable-7.jar
                       * AtumAPI (0.0.2) from Atum-1.12.2-2.0.20.jar
                       * Baubles|API (1.4.0.2) from Baubles-1.12-1.5.2.jar
                       * BetterWithModsAPI (Beta 0.6) from AppleSkin-mc1.12-1.0.14.jar
                       * BetweenlandsAPI (1.13.1) from TheBetweenlands-3.7.3-universal.jar
                       * bloodmagic-api (2.0.0) from BloodMagic-1.12.2-2.4.3-105.jar
                       * BotaniaAPI (93) from Botania r1.10-363.jar
                       * buildcraftapi_blocks (1.0) from buildcraft-all-7.99.24.8.jar
                       * buildcraftapi_boards (2.0) from buildcraft-all-7.99.24.8.jar
                       * buildcraftapi_core (2.2) from buildcraft-all-7.99.24.8.jar
                       * buildcraftapi_crops (1.1) from buildcraft-all-7.99.24.8.jar
                       * buildcraftapi_enums (1.0) from buildcraft-all-7.99.24.8.jar
                       * buildcraftapi_events (2.0) from buildcraft-all-7.99.24.8.jar
                       * buildcraftapi_facades (1.1) from buildcraft-all-7.99.24.8.jar
                       * buildcraftapi_filler (5.0) from buildcraft-all-7.99.24.8.jar
                       * buildcraftapi_fuels (2.0) from buildcraft-all-7.99.24.8.jar
                       * buildcraftapi_gates (4.1) from buildcraft-all-7.99.24.8.jar
                       * buildcraftapi_items (1.1) from buildcraft-all-7.99.24.8.jar
                       * buildcraftapi_library (2.0) from buildcraft-all-7.99.24.8.jar
                       * buildcraftapi_lists (1.0) from buildcraft-all-7.99.24.8.jar
                       * buildcraftapi_power (1.3) from buildcraft-all-7.99.24.8.jar
                       * buildcraftapi_recipes (3.0) from buildcraft-all-7.99.24.8.jar
                       * buildcraftapi_robotics (3.0) from buildcraft-all-7.99.24.8.jar
                       * buildcraftapi_statements (1.1) from buildcraft-all-7.99.24.8.jar
                       * buildcraftapi_tiles (1.2) from buildcraft-all-7.99.24.8.jar
                       * buildcraftapi_tools (1.0) from buildcraft-all-7.99.24.8.jar
                       * buildcraftapi_transport (5.0) from buildcraft-all-7.99.24.8.jar
                       * Chisel-API (0.0.1) from Chisel-MC1.12.2-1.0.2.45.jar
                       * ChiselAPI|Carving (0.0.1) from Chisel-MC1.12.2-1.0.2.45.jar
                       * ChiselsAndBitsAPI (14.25.0) from chiselsandbits-14.33.jar
                       * cofhapi (2.5.0) from CoFHCore-1.12.2-4.6.6.1-universal.jar
                       * commoncapabilities|api (0.0.1) from CommonCapabilities-1.12.2-2.4.8.jar
                       * cosmeticarmorreworked|api (1.0.0) from CosmeticArmorReworked-1.12.2-v5a.jar
                       * CraftingTweaks|API (4.1) from CraftingTweaks_1.12.2-8.1.9.jar
                       * ctm-api (0.1.0) from CTM-MC1.12.2-1.0.2.31.jar
                       * ctm-api-events (0.1.0) from CTM-MC1.12.2-1.0.2.31.jar
                       * ctm-api-models (0.1.0) from CTM-MC1.12.2-1.0.2.31.jar
                       * ctm-api-textures (0.1.0) from CTM-MC1.12.2-1.0.2.31.jar
                       * ctm-api-utils (0.1.0) from CTM-MC1.12.2-1.0.2.31.jar
                       * Culinary Construct API (1) from culinaryconstruct-1.3.4.jar
                       * DarknessLibAPI (1.1.0) from DarknessLib-1.12.2-1.1.0.jar
                       * DarknessLibAPI|Cap (1.1.0) from DarknessLib-1.12.2-1.1.0.jar
                       * DarknessLibAPI|Internal (1.1.0) from DarknessLib-1.12.2-1.1.0.jar
                       * enderioapi (4.0.0) from EnderIO-1.12.2-5.3.70.jar
                       * enderioapi|addon (4.0.0) from EnderIO-1.12.2-5.3.70.jar
                       * enderioapi|capacitor (4.0.0) from EnderIO-1.12.2-5.3.70.jar
                       * enderioapi|conduits (4.0.0) from EnderIO-1.12.2-5.3.70.jar
                       * enderioapi|farm (4.0.0) from EnderIO-1.12.2-5.3.70.jar
                       * enderioapi|redstone (4.0.0) from EnderIO-1.12.2-5.3.70.jar
                       * enderioapi|teleport (4.0.0) from EnderIO-1.12.2-5.3.70.jar
                       * enderioapi|tools (4.0.0) from EnderIO-1.12.2-5.3.70.jar
                       * enderioapi|upgrades (4.0.0) from EnderIO-1.12.2-5.3.70.jar
                       * farmingforblockheads|api (1.0) from FarmingForBlockheads_1.12.2-3.1.28.jar
                       * ForestryAPI|apiculture (5.0.0) from forestry_1.12.2-5.8.2.422.jar
                       * ForestryAPI|arboriculture (4.3.0) from forestry_1.12.2-5.8.2.422.jar
                       * ForestryAPI|book (5.8.1) from forestry_1.12.2-5.8.2.422.jar
                       * ForestryAPI|circuits (3.1.0) from forestry_1.12.2-5.8.2.422.jar
                       * ForestryAPI|climate (5.0.0) from forestry_1.12.2-5.8.2.422.jar
                       * ForestryAPI|core (5.7.0) from forestry_1.12.2-5.8.2.422.jar
                       * ForestryAPI|farming (5.8.0) from forestry_1.12.2-5.8.2.422.jar
                       * ForestryAPI|food (1.1.0) from forestry_1.12.2-5.8.2.422.jar
                       * ForestryAPI|fuels (3.0.0) from forestry_1.12.2-5.8.2.422.jar
                       * ForestryAPI|genetics (5.7.0) from forestry_1.12.2-5.8.2.422.jar
                       * ForestryAPI|gui (5.8.0) from forestry_1.12.2-5.8.2.422.jar
                       * ForestryAPI|hives (4.1.0) from forestry_1.12.2-5.8.2.422.jar
                       * ForestryAPI|lepidopterology (1.4.0) from forestry_1.12.2-5.8.2.422.jar
                       * ForestryAPI|mail (3.1.0) from forestry_1.12.2-5.8.2.422.jar
                       * ForestryAPI|modules (5.7.0) from forestry_1.12.2-5.8.2.422.jar
                       * ForestryAPI|multiblock (3.0.0) from forestry_1.12.2-5.8.2.422.jar
                       * ForestryAPI|recipes (5.4.0) from forestry_1.12.2-5.8.2.422.jar
                       * ForestryAPI|storage (5.0.0) from forestry_1.12.2-5.8.2.422.jar
                       * ForestryAPI|world (2.1.0) from forestry_1.12.2-5.8.2.422.jar
                       * ForgeEndertechAPI (1.0) from ForgeEndertech-1.12.2-4.5.5.0-build.0561.jar
                       * gendustryAPI (2.3.0) from gendustry-1.6.5.8-mc1.12.2.jar
                       * Guide-API|API (2.0.0) from Guide-API-1.12-2.1.8-63.jar
                       * iChunUtil API (1.2.0) from iChunUtil-1.12.2-7.2.2.jar
                       * ImmersiveEngineering|API (1.0) from ImmersiveEngineering-0.12-98.jar
                       * ImmersiveEngineering|ImmersiveFluxAPI (1.0) from ImmersiveEngineering-0.12-98.jar
                       * ImprovedBackpacks|API (1.2.0.3) from ImprovedBackpacks-1.12.2-1.5.0.0.jar
                       * industrialforegoingapi (5) from industrialforegoing-1.12.2-1.12.13-237.jar
                       * integrateddynamics|api (0.2.0) from IntegratedDynamics-1.12.2-1.1.11.jar
                       * jeresources|API (0.9.2.60) from JustEnoughResources-1.12.2-0.9.2.60.jar
                       * journeymap|client-api (1.4) from journeymap-1.12.2-5.7.1.jar
                       * journeymap|client-api-display (1.4) from journeymap-1.12.2-5.7.1.jar
                       * journeymap|client-api-event (1.4) from journeymap-1.12.2-5.7.1.jar
                       * journeymap|client-api-model (1.4) from journeymap-1.12.2-5.7.1.jar
                       * journeymap|client-api-util (1.4) from journeymap-1.12.2-5.7.1.jar
                       * JustEnoughItemsAPI (4.13.0) from jei_1.12.2-4.16.1.301.jar
                       * MekanismAPI|core (9.8.1) from Mekanism-1.12.2-9.8.3.390.jar
                       * MekanismAPI|energy (9.8.1) from Mekanism-1.12.2-9.8.3.390.jar
                       * MekanismAPI|gas (9.8.1) from Mekanism-1.12.2-9.8.3.390.jar
                       * MekanismAPI|infuse (9.8.1) from Mekanism-1.12.2-9.8.3.390.jar
                       * MekanismAPI|laser (9.8.1) from Mekanism-1.12.2-9.8.3.390.jar
                       * MekanismAPI|transmitter (9.8.1) from Mekanism-1.12.2-9.8.3.390.jar
                       * MekanismAPI|util (9.0.0) from Mekanism-1.12.2-9.8.3.390.jar
                       * minecolonies-api (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|achievements (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|blocks (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|blocks|decorative (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|blocks|huts (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|blocks|interfaces (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|blocks|types (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|client (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|client|render (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|client|render|modeltype (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|client|render|modeltype|registry (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|buildings (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|buildings|registry (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|buildings|views (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|buildings|workerbuildings (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|guardtype (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|guardtype|registry (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|jobs (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|jobs|registry (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|managers (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|managers|interfaces (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|permissions (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|requestsystem (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|requestsystem|data (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|requestsystem|factory (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|requestsystem|factory|standard (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|requestsystem|location (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|requestsystem|manager (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|requestsystem|request (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|requestsystem|requestable (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|requestsystem|requestable|crafting (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|requestsystem|requester (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|requestsystem|resolver (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|requestsystem|resolver|player (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|requestsystem|resolver|retrying (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|requestsystem|token (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|colony|workorders (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|compatibility (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|compatibility|candb (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|compatibility|dynamictrees (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|compatibility|gbook (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|compatibility|tinkers (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|configuration (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|crafting (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|creativetab (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|entity (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|entity|ai (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|entity|ai|citizen (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|entity|ai|citizen|builder (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|entity|ai|citizen|guards (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|entity|ai|pathfinding (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|entity|ai|registry (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|entity|ai|statemachine (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|entity|ai|statemachine|basestatemachine (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|entity|ai|statemachine|states (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|entity|ai|statemachine|tickratestatemachine (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|entity|ai|statemachine|transition (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|entity|citizen (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|entity|citizen|citizenhandlers (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|entity|mobs (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|entity|mobs|barbarians (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|entity|mobs|pirates (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|entity|mobs|util (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|entity|pathfinding (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|entity|pathfinding|registry (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|inventory (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|inventory|api (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|items (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|network (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|sounds (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|tileentities (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|util (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-api|util|constants (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-blockout (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-blockout|controls (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * minecolonies-blockout|views (1.12.2-0.11.811-BETA) from minecolonies-1.12.2-0.11.811-BETA-universal.jar
                       * MouseTweaks|API (1.0) from MouseTweaks-2.10-mc1.12.2.jar
                       * naturesauraapi (9) from NaturesAura-18.1.jar
                       * openblocks|api (1.2) from OpenBlocks-1.12.2-1.8.1.jar
                       * opencomputersapi|component (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.5.192.jar
                       * opencomputersapi|core (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.5.192.jar
                       * opencomputersapi|driver (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.5.192.jar
                       * opencomputersapi|driver|item (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.5.192.jar
                       * opencomputersapi|event (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.5.192.jar
                       * opencomputersapi|filesystem (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.5.192.jar
                       * opencomputersapi|internal (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.5.192.jar
                       * opencomputersapi|machine (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.5.192.jar
                       * opencomputersapi|manual (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.5.192.jar
                       * opencomputersapi|network (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.5.192.jar
                       * opencomputersapi|prefab (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.5.192.jar
                       * PatchouliAPI (6) from Patchouli-1.0-23.6.jar
                       * practicallogistics2-api (3.1) from practicallogistics2-1.12.2-3.0.8-11.jar
                       * QuarkAPI (2) from Bountiful Baubles-1.12.2-0.1.6.jar
                       * reborncoreAPI (3.19.5) from RebornCore-FORK-1.12.2-3.19.5-universal.jar
                       * reborncoreAPI|Power (3.19.5) from RebornCore-FORK-1.12.2-3.19.5-universal.jar
                       * reborncoreAPI|Recipe (3.19.5) from RebornCore-FORK-1.12.2-3.19.5-universal.jar
                       * reborncoreAPI|Tile (3.19.5) from RebornCore-FORK-1.12.2-3.19.5-universal.jar
                       * redstonefluxapi (2.1.1) from RedstoneFlux-1.12-2.1.1.1-universal.jar
                       * sonarapi (1.0.1) from sonarcore-1.12.2-5.0.19-20.jar
                       * stevescartsAPI (${version}) from StevesCarts-1.12.2-2.4.32.137.jar
                       * stevescartsAPI|FARMS (${version}) from StevesCarts-1.12.2-2.4.32.137.jar
                       * StorageDrawersAPI (2.1.0) from StorageDrawers-1.12.2-5.4.2.jar
                       * StorageDrawersAPI|event (2.1.0) from StorageDrawers-1.12.2-5.4.2.jar
                       * StorageDrawersAPI|registry (2.1.0) from StorageDrawers-1.12.2-5.4.2.jar
                       * StorageDrawersAPI|render (2.1.0) from StorageDrawers-1.12.2-5.4.2.jar
                       * StorageDrawersAPI|storage (2.1.0) from StorageDrawers-1.12.2-5.4.2.jar
                       * StorageDrawersAPI|storage-attribute (2.1.0) from StorageDrawers-1.12.2-5.4.2.jar
                       * team_reborn|Praescriptum (3.19.5) from RebornCore-FORK-1.12.2-3.19.5-universal.jar
                       * techrebornAPI (2.27.3.1084) from TechReborn-1.12.2-2.27.3.1084-universal.jar
                       * Thaumcraft|API (6.0.2) from Thaumcraft-1.12.2-6.1.BETA26.jar
                       * thaumicaugmentationapi (2.0.13) from ThaumicAugmentation-1.12.2-2.0.13.jar
                       * tombstone-api (1.0.8) from tombstone-4.1.2-1.12.2.jar
                       * tombstone-api-capability (1.0.8) from tombstone-4.1.2-1.12.2.jar
                       * tombstone-api-event (1.0.8) from tombstone-4.1.2-1.12.2.jar
                       * tombstone-api-magic (1.0.8) from tombstone-4.1.2-1.12.2.jar
                       * tombstone-api-recipe (1.0.8) from tombstone-4.1.2-1.12.2.jar
                       * totemic|API (1.12.2-7.1.0) from Totemic-1.12.2-0.11.6.jar
                       * VampirismAPI (1.4) from Vampirism-1.12.2-1.6.2.jar
                       * WailaAPI (1.3) from Hwyla-1.8.26-B41_1.12.2.jar
                       * wct|api (1.1) from WirelessCraftingTerminal-1.12.2-3.12.97.jar
                       * zerocore|API|multiblock (1.10.2-0.0.2) from zerocore-1.12.2-0.1.2.9.jar
                       * zerocore|API|multiblock|rectangular (1.10.2-0.0.2) from zerocore-1.12.2-0.1.2.9.jar
                       * zerocore|API|multiblock|tier (1.10.2-0.0.2) from zerocore-1.12.2-0.1.2.9.jar
                       * zerocore|API|multiblock|validation (1.10.2-0.0.2) from zerocore-1.12.2-0.1.2.9.jar
  Patchouli open book context: n/a
  RebornCore: Plugin Engine: 0
              RebornCore Version: 3.19.5
              Runtime Debofucsation 1
              Invalid fingerprint detected for RebornCore!
              RenderEngine: 0
  Suspected Mods: Unknown
  Launched Version: forge-14.23.5.2854
  LWJGL: 2.9.4
  OpenGL: NVIDIA GeForce RTX 2060/PCIe/SSE2 GL version 4.6.0 NVIDIA 471.68, NVIDIA Corporation
  GL Caps: Using GL 1.3 multitexturing.
           Using GL 1.3 texture combiners.
           Using framebuffer objects because OpenGL 3.0 is supported and separate blending is supported.
           Shaders are available because OpenGL 2.1 is supported.
           VBOs are available because OpenGL 1.5 is supported.
  Using VBOs: Yes
  Is Modded: Definitely; Client brand changed to 'fml,forge'
  Type: Client (map_client.txt)
  Resource Packs: 
  Current Language: English (US)
  Profiler Position: N/A (disabled)
  CPU: 16x AMD Ryzen 7 3800X 8-Core Processor
