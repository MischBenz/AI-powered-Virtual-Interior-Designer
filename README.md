# AI-powered-Virtual-Interior-Designer
Create an AI-driven virtual interior design tool that generates personalized room layouts and decor suggestions based on user preferences.
class VirtualInteriorDesigner:
    def __init__(self):
        self.room_types = ["Living Room", "Bedroom", "Kitchen", "Bathroom"]
        self.color_schemes = ["Warm", "Cool", "Neutral"]
        self.styles = ["Modern", "Traditional", "Bohemian", "Scandinavian"]

    def get_user_preferences(self):
        print("Welcome to the AI-powered Virtual Interior Designer!")
        room_type = input(f"Please choose a room type ({', '.join(self.room_types)}): ")
        color_scheme = input(f"Choose your preferred color scheme ({', '.join(self.color_schemes)}): ")
        style = input(f"Choose your style ({', '.join(self.styles)}): ")
        return room_type, color_scheme, style

    def generate_layout(self, room_type):
        # Simplified layout generation logic
        if room_type == "Living Room":
            return "A spacious layout with a sofa set facing a TV unit and a coffee table in the center."
        elif room_type == "Bedroom":
            return "A cozy layout with a king-sized bed, two nightstands, and a dresser."
        elif room_type == "Kitchen":
            return "An L-shaped kitchen with ample counter space and modern appliances."
        elif room_type == "Bathroom":
            return "A functional layout with a walk-in shower, vanity, and mirror."
        else:
            return "Custom room layout."

    def suggest_decor(self, color_scheme, style):
        # Simplified decor suggestion logic
        return f"A {color_scheme.lower()} color palette with {style.lower()} style furniture and decorations."

    def run(self):
        room_type, color_scheme, style = self.get_user_preferences()
        layout = self.generate_layout(room_type)
        decor_suggestion = self.suggest_decor(color_scheme, style)
        print("\nGenerated Room Layout:")
        print(layout)
        print("\nDecor Suggestions:")
        print(decor_suggestion)

if __name__ == "__main__":
    designer = VirtualInteriorDesigner()
    designer.run()
