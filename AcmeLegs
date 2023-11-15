using Terraria;
using Terraria.ID;
using Terraria.Localization;
using Terraria.ModLoader;

namespace ExampleMod.Content.Items.Armor
{
    [AutoloadEquip(EquipType.Legs)]
    public class AcmeGrieves : ModItem
    {

        public override void SetDefaults() {
            Item.width = 20;
            Item.height = 12;
            Item.value = Item.sellPrice(gold: 42);
            Item.rare = ItemRarityID.Purple;
            Item.defense = 24;
        }

        public override void UpdateEquip(Player player) 
        {
            player.moveSpeed += 0.15f;
             
            player.GetAttackSpeed(DamageClass.Melee) += 0.10f;
        }

            public override void AddRecipes() 
            {
                recipe.AddIngredient<DirtBlock>;
				recipe.AddTile<WorkBench>
                recipe.Register;
                
            }
        }
    }
