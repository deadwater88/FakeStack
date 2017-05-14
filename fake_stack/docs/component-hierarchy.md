{
  currentUser: {
    id: 1,
    email: "david.wong.cal@gmail.com"
    image_url: "example.com/image123"
  },
  forms: {
    signUp: {errors: []},
    logIn: {errors: []},
    createNote: {errors: ["body can't be blank"]}
  },

  Posts: {
    1:{
      id: 1
      author: "david"
      tagged_users: [2, 4, 5]
      content: "This requires a lot of planning"
    }
    2:{
      id: 2
      author: "Sam"
      tagged_users: [1,3,6]
      content: "This wasn't too hard"
    }
  }

  Comments: {
    1:{
      id: 1
      author_id: 2
      post_id: 1
      content: "It wasn't too bad"
    }
    2:{
      id: 2
      author_id: 1
      post_id: 1
    }
  }

  Friends: {
    1:{
      id: 1,
      firstName: "David"
      lastName: "Wong"
      image_url: "example.com/image123"
    }
    2:{
      id: 2
      firstName: "Rick"
      lastName: "Sanchez"
      image_url: "example.com/image413"
    }
    123:{
      id: 123
      firstName: "Gerry"
      lastName: "Goodwin"
      image_url: "example.com/image123124"
    }
  }

  viewedUser: {
    id: 4,
    firstName: "Kate"
    lastName: "Winslet"
    profile: {
      
    }


  }
}
