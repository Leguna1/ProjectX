# ProjectX
This is my examination project, the goal with this project was to learn as much as possible about how to make open world arpg game with BluePrint only.
I wanted to have one reasonably small map where monsters could roam around and player's objective would be to farm and get stronger as preperation for the boss fights. I wanted the player be able to work with at least 7 skills get stat points as he levels up and be able to choose where to put his points to deal more damage or take less damage. 
I focused on creating smart AIs and damage system component first 3 weeks of the project, the goal was to have melee, ranged and mage enemies with smart combat behaviors pursuing the player, hiding from the player, self-healing and team combat.

Both AIs and Player uses same damage and stats components to take damage from each other and respond to damage but they have different attacks component because I wanted to keep player's abilities for itself.

Path to Damage system: Content/Developers/KalE/Systems/DamageSystem   (The player blueprint can be found here too)
Path to Stats system: Content/Developers/KalE/Systems/Stats
Path to AIs: Content/Developers/KalE/Systems/AI
Path to Projectiles: Content/Developers/KalE/Systems/AoE & Projectiles
Path to AI Attacks component: Content/Developers/KalE/Systems/Abilities (BPC_Attacks)
Path to Player abilities: Content/Developers/KalE/Systems/Abilities/AbilityBase (BPC_RogueAbility)

Path to UI Widgets: Content/Developers/KalE/Systems/Widget

Both player and AIs can wield any weapon from Content/Arsenal but the weapons are purely visual, the damage is dealt with ray tracing and targeting only. 

The level has only melee type enemies and only few of them because of my laziness but project holds all core needs to populate the level with ranged and mage enemies too by creating new childs from BP_EnemyRangedChild & BP_EnemyMageChild and assigning animation montages, sounds and effects in the details panel.

Player ability types:
Basic single target attack, AoE attack, stun attack, sleep attack, and damage is determined by player's attack power and enemy's defence power.
Player has 4 directional flip-move to dodge attacks. (Press Shift while moving) to execute.
