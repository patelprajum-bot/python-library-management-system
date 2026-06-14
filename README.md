class Library:
    def __init__(self):
        self.books=["\nmath","physics","chemistery","English"]

    def display_book(self):
        for book in self.books:
            print(book)

    def borrow_book(self):
        user_book=input(" select book ")
        if user_book not in self.books:
            print(" book not find ")
        else:
            self.books.remove(user_book)
            print(f" {user_book} issued succesfully ")

    def return_book(self):
        return_book=input(" return book ")
        if return_book in self.books:
            print("\n This book is already exits")
        else:
            self.books.append(return_book)
            print(" book returned succesfully")

    def add_book(self):
        add_books=input(" add book.")
        if add_books in self.books:
            print(" this book is already exits")
        else:
            self.books.append(add_books)
            print("book addeed succesfully")

a=Library()

while True:
    print("Menu-system\n1.Show all books\n2.Borrow book\n3.Return book\n4.Add new book\n0.for quit")

    choice=input("select the choice--")

    if choice=="1":
        a.display_book()
    elif choice=="2":
        a.borrow_book()
    elif choice=="3":
        a.return_book()
    elif choice=="4":
        a.add_book()
    elif choice=="0":
        break

