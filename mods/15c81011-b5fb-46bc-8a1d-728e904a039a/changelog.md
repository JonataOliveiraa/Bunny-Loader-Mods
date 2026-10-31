# Changelog

## 0.2.1-beta
- Adicionados `description.md` e `license.md` com descrição do projeto, aviso de beta e licença de uso restrito.
- Atualizados os metadados do mod para identificar o estado beta.

## 0.2.2-beta
- Hostile creatures scale by +10% maximum life and damage per unique main-progression boss defeated.
- Optional bosses do not increase the scaling count; The Twins count as one progression stage.

## 0.3.0-beta
- Added classes: Guerreiro, Atirador, Mago, Invocador, Necromante and Combatente (icons reuse the attribute icons), each with its own passive.
- Class selection screen opens the first time the menu is opened without a class (list of classes, then a detail screen with Back / Confirm). The chosen class is saved with the character.
- `/exp class <name|reset>` for testing. "Reset all" also clears the class.
- Fixed the attributes page not drawing (the back button used a palette before it was declared).
- Attribute description (name and text) is larger; the boxes keep their original size.
- Skill tree removed for now: its menu entry shows "Work In Progress".
- Defeating a progression boss for the first time shows "The creatures have grown stronger!" (several variations) with the new life/damage bonus.
- Eater of Worlds and The Destroyer now count when their last segment dies; The Twins count only after both are dead.
- Chat messages, the exp bar and the character menu are fully translated (pt-BR / en-US).

## 1.0.0
- First stable release: the mod is no longer in beta. Version, summary and description were updated for publishing.
- New level-up feedback: instead of a chat message, green particles burst out of the character and keep rising for a moment, together with a "Level up! Lv N" combat text and a sound. Falls back to the chat line only if the effect fails.
- `/exp add` now plays the same level-up effect, so it can be tested without killing enemies.
- Description rewritten: beta notice removed, features list now covers classes, enemy scaling and the level-up effect.
- `license.md` updated: beta notice replaced by a standard "as is" warranty section.
