

#Delete a Book
mutation {
  delete_book: deleteBook(id:7){
    book {
      id
    }
  }
}

#Update a Book
mutation {
  update_book: updateBook(input: {title:"Imagine this updated",author: "Shola", pages: 12, price: 1200, quantity: 4, description:"a brief description", status: "True"}
  ,id:5){
    book {
      id,
      title,
      author,
      pages,
      price,
      quantity,
      description,
      status
    }
  }
}

#Create a Book
mutation {
  update_book: createBook(input: {title:"Imagine this updated 1",author: "Shola", pages: 12, price: 1200, quantity: 4, description:"a brief description", status: "True"}){
    book {
      id,
      title,
      author,
      pages,
      price,
      quantity,
      description,
      status
    }
  }
}

#Create Category
mutation {
 create_category:createCategory(title :"Plastic") {
  category {
   id,
   title,
  }
 }
}



#Get all books list witth details
{
  books{
      id
      title
      author
      isbn
      pages 
      price
      quantity
      description
      status
    }
}
