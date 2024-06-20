# Hotel Reservation System 🏨

Welcome to the **Hotel Reservation System**! This project is a console-based application designed to manage hotel reservations using Java and MySQL. 

## Features ✨

- **Reserve a Room:** Easily reserve a room by providing guest details and room information.
- **View Reservations:** Display all current reservations in a tabular format.
- **Get Room Number:** Retrieve the room number based on reservation ID and guest name.
- **Update Reservations:** Update existing reservations with new guest details, room number, or contact information.
- **Delete Reservations:** Delete a reservation using its reservation ID.
- **User-Friendly Exit:** Smoothly exit the system with a countdown.

## Technologies Used 🛠️

- **Java**: The core programming language used to build the application.
- **MySQL**: Database used for storing reservation data.
- **JDBC**: Java Database Connectivity for connecting Java application to the MySQL database.

## Prerequisites 📋

- Java Development Kit (JDK) installed
- MySQL Server installed and running
- MySQL Connector/J library (download from [MySQL official site](https://dev.mysql.com/downloads/connector/j/))

## Setup Instructions 🚀

1. **Clone the Repository:**

   ```sh
   git clone https://github.com/your-username/HotelReservationSystem.git
   cd HotelReservationSystem
   
2. **Set Up the Database:**

Create a MySQL database named hotel_db and a reservations table by running the following SQL commands:
CREATE DATABASE hotel_db;

USE hotel_db;

CREATE TABLE reservations (
    reservation_id INT AUTO_INCREMENT PRIMARY KEY,
    guest_name VARCHAR(100) NOT NULL,
    room_number INT NOT NULL,
    contact_number VARCHAR(15) NOT NULL,
    reservation_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

3. **Modify Database Credentials:**

Update the database credentials in HotelReservationSystem.java to match your MySQL setup:
private static final String url = "jdbc:mysql://localhost:3306/hotel_db";
private static final String username = "your_mysql_username";
private static final String password = "your_mysql_password";

4. **Compile the Project:**
   javac -cp .:/path/to/mysql-connector-j-8.4.0.jar HotelReservationSystem.java

5. **Run the Application:**
   java -cp .:/path/to/mysql-connector-j-8.4.0.jar HotelReservationSystem


**How to Use 📝**

1. **Reserve a Room:**

Select option 1.
Enter guest name, room number, and contact number.
The system will confirm if the reservation was successful.

2. **View Reservations:**

Select option 2.
All current reservations will be displayed in a table format.

3. **Get Room Number:**

Select option 3.
Enter reservation ID and guest name to retrieve the room number.

4. **Update Reservation:**

Select option 4.
Enter reservation ID and new details to update the reservation.

5. **Delete Reservation:**

Select option 5.
Enter reservation ID to delete the reservation.

6. **Exit:**

Select option 0 to exit the system gracefully.


**Contributing 🤝**
Contributions are welcome! Please fork this repository and submit pull requests for any improvements.
