TORNADO TEST MOD - FULL SOURCE PACK (Minecraft Java Edition 1.10.2 / Forge 1.10.2)

This pack contains a more complete experimental implementation than the earlier starter files.
It is a separate test mod with mod ID `tornadotest`, intended to be added to a Forge 1.10.2
MDK project that already has a compatible build.gradle and ForgeGradle setup.

CONTENTS
- EntTornado.class: fixed-direction tornado entity, 10-minute lifetime, cloud/funnel particles,
  limited ground-block pickup, controlled block orbit visuals, and player spiral movement.
- TornadoGun.class: creative Miscellaneous-tab item that summons the tornado.
- EntityTornadoBlock.class: full-size block visuals controlled by the tornado.
- TornadoTestMod.class: mod entry point and item/entity registration.
- TornadoTestClientProxy.class / TornadoTestCommonProxy.class: item model and entity renderers.
- resources: string item texture model, English name, and mcmod.info.

IMPORTANT LIMITATIONS
- The block and player behaviors are experimental approximations, not a verified recreation of the
  original Weather & Tornadoes mod. Fire and liquid pickup are represented by particles rather than
  full-size orbiting block entities. Blocks currently disappear at ground level at the end of their
  controlled spiral instead of being placed back into the world.
- The bubble is particle-based. It is not a solid collision shell.
- The test mod uses its own mod ID (`tornadotest`) to avoid colliding with a separate full mod whose
  ID is `weatherandtornadoes`. If you merge these into a project, keep the package path and resource
  folder names consistent.
- The existing build.gradle must be configured for Forge 1.10.2, Java 8, and compatible ForgeGradle.
  A successful source pack alone does not guarantee a buildable JAR.

Suggested Java source folder:
src/main/java/com/weatherandtornadoes/
Suggested resource folder:
src/main/resources/
