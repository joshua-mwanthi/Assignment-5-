class Book:
    def __init__(self, title, author, pages, genre):
        self.title = title
        self.author = author
        self.pages = pages
        self.genre = genre

    def display_info(self):
        print(f"Title: {self.title}")
        print(f"Author: {self.author}")
        print(f"Pages: {self.pages}")
        print(f"Genre: {self.genre}")

    def read(self, pages_read):
        print(f"You have read {pages_read} pages of {self.title}.")
        remaining_pages = self.pages - pages_read
        print(f"{remaining_pages} pages remaining.")

class EBook(Book):
    def __init__(self, title, author, pages, genre, file_size, format):
        super().__init__(title, author, pages, genre)
        self.file_size = file_size
        self.format = format

    def display_info(self):
        super().display_info()
        print(f"File Size: {self.file_size} MB")
        print(f"Format: {self.format}")

    def download(self):
        print(f"Downloading {self.title} in {self.format} format...")

# Create an instance of Book
book1 = Book("1984", "George Orwell", 328, "Dystopian")
book1.display_info()
book1.read(50)

print()  # Just for better separation of output

# Create an instance of EBook
ebook1 = EBook("Digital Fortress", "Dan Brown", 356, "Thriller", 1.5, "PDF")
ebook1.display_info()
ebook1.read(100)
ebook1.download() 

Part b
class Vehicle:
    def move(self):
        raise NotImplementedError("Subclasses must implement this method.")

class Car(Vehicle):
    def move(self):
        print("Driving 🚗")

class Plane(Vehicle):
    def move(self):
        print("Flying ✈️")

class Boat(Vehicle):
    def move(self):
        print("Sailing 🚤")

# Create instances of each vehicle
car = Car()
plane = Plane()
boat = Boat()

# Call the move method on each instance
car.move()    # Output: Driving 🚗
plane.move()  # Output: Flying ✈️
boat.move()   # Output: Sailing 🚤

 
