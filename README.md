# MIT-APP-Assignment-1.
class library:
    def __init__(self):
        self.lib_ID=[]
        self.lib_book=[519,753,698]
    def add_book(self,book_ID):
        self.book_ID=book_ID
        self.lib_book.append(book_ID)
        print(f"Book with book ID:{self.book_ID} has been added")
        print(self.lib_book)
    def delete(self,book_ID):
        if book_ID in self.lib_book:
            print(f"Book with book ID:{self.book_ID} has been removed")
            self.lib_book.remove(self.book_ID)
            print(self.lib_book)
        else:
            print("There is no book with this book id!!") 
    def return_book(self,book_ID,lib_ID):
        print(f"Book with book ID:{book_ID} has been return by lib ID:{lib_ID}")        
        self.lib_book.append(book_ID)
        print(self.lib_book)
    def issueing_book(self,book_ID,lib_ID):
        if book_ID in self.lib_book:
            print(f"Book with book ID:{book_ID} has been issued for lib ID:{lib_ID}")        
            self.lib_book.remove(book_ID)
            print(self.lib_book)
        else:
            print("There is no book with this id!!")
a=library()
i=True
while(i==True):
    x=int(input("select from bottom \n1.Add Book\n2.Remove Book\n3.Issue Book\n4.Return Book\n"))
    if(x==1):
        b=int(input("enter book id: "))
        a.add_book(b)
    if(x==2):
        b=(input("enter book id: "))
        a.delete(b)   
    if(x==3):
        b=int(input("enter book id: "))
        c=int(input("enter lib id: "))
        a.issueing_book(b,c)
    if(x==4):
        b=int(input("enter book id: "))
        c=int(input("enter lib id: "))
        a.return_book(b,c)
    d=int(input("do you want to use this again? \n1.Yes(1)\n2.No(2)\n "))
    if(d==1):
        i=True
    else:
        i=False