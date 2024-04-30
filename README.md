# Nested-Dictionaries


        # Avengers RPG Nested Dictionaries
       # This Python script creates nested dictionaries for an RPG game, featuring two Avengers characters.
          # It includes characters, their inventory, and associated locations with detailed descriptions.
       # Author: Vidhi
       # Date: 20-04-2024

      # Characters dictionary with nested attributes and inventory
characters = {
    "Iron Man": {
        "attributes": {
            "secret_identity": "Tony Stark",
            "super_power": "Genius-level intellect, multitude of Iron Man suits",
            "health_points": 100
        },
        "inventory": ["Iron Man Suit", "Arc Reactor"]
    },
    "Thor": {
        "attributes": {
            "secret_identity": "Thor Odinson",
            "super_power": "Asgardian god, control over thunder",
            "health_points": 150
        },
        "inventory": ["Mjolnir", "Stormbreaker"]
    }
}

       # Inventory dictionary with properties for each item
inventory = {
    "Iron Man Suit": {
        "description": "High-tech suit of armor providing flight and combat capabilities.",
        "damage": 80,
        "protection": 70
    },
    "Arc Reactor": {
        "description": "Power source for the Iron Man suit and Stark's heart.",
        "damage": 0,
        "protection": 50
    },
    "Mjolnir": {
        "description": "Enchanted hammer with the power to summon thunder.",
        "damage": 100,
        "protection": 50
    },
    "Stormbreaker": {
        "description": "A magical axe forged in Nidavellir, capable of summoning the Bifrost.",
        "damage": 120,
        "protection": 50
    }
}

        # Locations dictionary with descriptions
locations = {
    "Stark Tower": {
        "description": "The modern headquarters of Iron Man located in New York City.",
        "threat_level": "Low"
    },
    "Asgard": {
        "description": "The celestial realm of the gods, home to Thor.",
        "threat_level": "High"
    }
}

         # Function to print details of each character, including inventory items
def print_characters(characters, inventory):
    for name, details in characters.items():
        print(f"Character: {name}")
        for attr, value in details["attributes"].items():
            print(f"  {attr.replace('_', ' ').title()}: {value}")
        print("  Inventory:")
        for item in details["inventory"]:
            print(f"    - {item}: {inventory[item]['description']}")
        print()

     # Function to print descriptions of each location
def print_locations(locations):
    for place, loc_details in locations.items():
        print(f"Location: {place}")
        for prop, val in loc_details.items():
            print(f"  {prop.title()}: {val}")
        print()

     # Main execution
if __name__ == "__main__":
    print("Avengers Character Details:\n")
    print_characters(characters, inventory)
    print("Avengers Locations:\n")
    print_locations(locations)

