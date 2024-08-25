# quartzclass Quartz:
    def __init__(self, color, size, clarity):
        self.color = color
        self.size = size  # in carats
        self.clarity = clarity
        self.is_polished = False

    def display_info(self):
        """Display the quartz details."""
        polished_status = "Polished" if self.is_polished else "Not Polished"
        print(f"Quartz Details:")
        print(f"Color: {self.color}")
        print(f"Size: {self.size} carats")
        print(f"Clarity: {self.clarity}")
        print(f"Status: {polished_status}")

    def polish(self):
        """Mark the quartz as polished."""
        if not self.is_polished:
            self.is_polished = True
            print(f"The quartz has been polished.")
        else:
            print(f"The quartz is already polished.")

    def update_clarity(self, new_clarity):
        """Update the clarity of the quartz."""
        self.clarity = new_clarity
        print(f"Quartz clarity updated to: {self.clarity}")


# Example usage
my_quartz = Quartz("Clear", 5.2, "High")
my_quartz.display_info()     # Display initial info
my_quartz.polish()           # Polish the quartz
my_quartz.display_info()     # Display updated info
my_quartz.update_clarity("Very High")  # Update clarity
my_quartz.display_info()     # Display updated info
