using Terraria; 
using Terraria.ID;
using Terraria.Localization;
using Terraria.ModLoader;

namespace AcmeArmour.Items.Armor
    {
    public class AcmeBreastplate.ModItem
        {
            
            public override void SetDefaults()
               {
                  Item.defense = 28;
                  Item.width = 42;
                    Item.height = 30;
                    Item.value = Item.sellPrice(gold: 42);
                    Item.rare = ItemRarityID.Purple;
                }

            public static readonly int MaxMinionIncrease = 4;
            public static readonly int MaxSummonDamageIncrease = 15;
            public static readonly int MaxMeleeAttackSpeedIncrease = 30;
            public static readonly int MaxMeleeDamageIncrease = 30;
            public static readonly int ArmorPenetrationIncrease = 12;
            public static readonly int MaxLifeIncrease = 100;
            public static readonly int CritChanceIncrease = 15;

            public override LocalizedText Tooltip => base.Tooltip.WithFormatArgs(MaxMinionIncrease, MaxSummonDamageIncrease, MaxMeleeAttackSpeedIncrease, MaxMeleeDamageIncrease, GenericArmorPenetration);

            public override void UpdateEquip(Player player) 
            {
                player.maxMinions += MaxMinionIncrease;
                player.statLifeMax2 += MaxLifeIncrease;
                player.GetDamage(DamageClass.Melee) += MaxMeleeDamageIncrease / 100;
                player.GetArmorPenetration(DamageClass.Summon) += ArmorPenetrationIncrease;
                player.GetDamage(DamageClass.Summon) += MaxSummonDamageIncrease / 100;
                player.GetAttackSpeed(DamageClass.Melee) += MaxMeleeAttackSpeedIncrease;
                player.GetCritChance(DamageClass.Melee) += CritChanceIncrease / 100;
                player.GetCritChance(DamageClass.Summon) += CritChanceIncrease / 100;
            }

            public override void AddRecipes()
            {
                CreateRecipe().AddIngredient<DirtBlock>;
                AddTile<WorkBench>.Register;
                
            }
        }
    }
