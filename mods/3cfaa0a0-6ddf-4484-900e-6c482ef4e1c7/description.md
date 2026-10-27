# Physaria (Kinetic Gore)

A ragdoll and body physics engine for Terraria, purely cosmetic: enemy deaths
become physics-driven ragdolls, with dismemberment, particle blood and
wobbling heads. Works with any mod.

## Ragdolls

- **Physics bodies**: enemies collapse into ragdolls that obey gravity,
  friction and bounce, rolling down slopes. Flying enemies crash and splatter
  on impact.
- **Persistent corpses**: bodies stay on the ground and fade out after the
  chosen time.
- **Ragdoll collision**: ragdolls collide with each other and pile up.
- **Buoyancy**: in water they float, slowly.

## Dismemberment and blood

- On death, humanoids may lose their **head**, which rolls away with physics
  while the **neck bleeds**.
- Striking a body on the ground launches it and can knock off the head or the
  **legs**.
- **Sticky blood**: drops stop when they hit the ground, form pools and slowly
  fade.
- **Gibs**: small chunks fly out of enemies on every hit.

## Living physics

- **Head bob**: humanoids (town NPCs too) wobble their heads while walking,
  like a car dashboard bobblehead.
- **Head flinching**: heads snap back and wobble when hit.
- **Head banging**: near someone playing an instrument, humanoids bob their
  heads and face the musician (off by default).
- **Slime jiggle**: slimes stretch and squash as they jump and land.
- **Arrow sticking**: arrows stay stuck in enemies and bodies for a while (off
  by default).

## Options

Nearly everything is adjustable: corpse duration, dismemberment chance, blood
amount, size and speed, gibs, gravity, bounce, friction, knockback force, neck
and slime stiffness and damping, and more.

## On mobile

- Each device creates and simulates its own bodies: nothing goes over the
  network, and in multiplayer each player sees their own.
- **Max corpses** (new option): past the limit, the oldest body disappears, to
  keep the phone running smoothly.
- Times are in seconds.
- There is no Sword (And Spear) Swing compatibility (that mod does not exist
  on mobile).

## Credits

Original mod by **LevitatingGT** for tModLoader, ported to Bunny Loader by
**Animatak_**.
