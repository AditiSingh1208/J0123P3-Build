# J0123P3-Build

## npm init
## npm i nodemon --save-dev
## 

MVC Arch => Controllers
  >> M: Model (It depicts the structure of aMongoDb Collections)
  >> V: View (wrt to frontend (reactJs))
  >> C: Controllers (Brain or logical part of a route)
        >> books.controllers.js
        >> users.controllers.js



Schema >>
  id: String
  name: String
  age: Number
  gender: char || varchar(15)

model >>
  id: 123
  name: DevTown
  age: 23
  gender: 'M'


Redmi Note 8 pro
amazon: 18k
flipkart: 10k


Foreing Key:
>> Referential Integrity

Users Table                           Books Table
issuedBook: 3(Foreing Key here)       issuedbook: 2 (Primary Key)




<!--

router.get("/issued/by-user", (req, res) => {
  const usersWithTheIssuedBook = users.filter((each) => {
    if (each.issuedBook) return each;
  });
  const issuedBooks = [];

  usersWithTheIssuedBook.forEach((each) => {
    const book = books.find((book) => book.id === each.issuedBook);

    book.issuedBy = each.name;
    book.issuedDate = each.issuedDate;
    book.returnDate = each.returnDate;

    issuedBooks.push(book);
  });
  if (issuedBooks.length === 0) {
    return res.status(404).json({
      success: false,
      message: "No Book Have Been Issued Yet..",
    });
  }
  return res.status(200).json({
    success: true,
    message: "Users With The Issued Books...",
    data: issuedBooks,
  });
});

  -->