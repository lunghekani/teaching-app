# teaching-app
// The Book class should have properties for title, author, and ISBN, as well as methods for getting and setting these properties.
// It should also have a method for checking whether the book is available (i.e., whether the number of copies available is greater than zero).

// The FictionBook class should inherit from Book and also have a property for the genre of the book 
//(e.g., "mystery", "romance", "science fiction", etc.).

// The NonFictionBook class should also inherit from Book and have a property for the subject of the book
//(e.g., "history", "biography", "self-help", etc.).

// Your task is to write a method that allows a user to check out a book from the library.
// The method should take as input the title of the book and the number of copies the user wants to check out. 
//It should update the database to reflect the fact that the specified number of copies are no longer available. 
//If the book is not available, the method should throw an exception.




 // CREATING VARIABLES TO CREATE THE CONNECTION STRING
            // THIS IS ON MY SERVER SO IT CAN RUN WITHOUT AN ISSUE
            MySqlConnection connection;
            string server;
            string database;
            string uid;
            string password;

            // MY SERVER DETAILS, YOU CAN STEAL THESE KINDA
            server = "164.160.91.44"; // SERVER IP ADDRESS
            database = "vxworkfl_DSWBooks"; // DB NAME
            uid = "vxworkfl_DSW3A"; // USERNAME
            password = "LuuIsAwesome@23"; // PASSWORD AND YES I AM AWESOME


            string connectionString;
            // BUILDING THE CONNECTION STRING
            connectionString = "SERVER=" + server + ";" + "DATABASE=" + database + ";" + "UID=" + uid + ";" + "PASSWORD=" + password + ";";

            // CREATING A MYSQL CONNECTION TO CONDUCT OPERATIONS
            connection = new MySqlConnection(connectionString);

            try
            {
                connection.Open();
                Console.WriteLine("Connection is open");

            }
            catch (Exception)
            {
                Console.WriteLine("Contact Lunghi The Server Could be Down or you have no internet");// NO REALLY CALL HIM :)
            }

