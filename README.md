# MOVIE_BOOKING1
📌 Overview

This is a Java Servlet + JSP based Movie Ticket Booking System. It allows users to register, login, browse movies, select shows, choose seats, and complete bookings. Admins can add movies and manage show details.

The system uses JDBC + MariaDB, follows MVC architecture, and is organized into DAO, Model, and Servlet layers.
⚙️ Technologies Used

Java 8+

JSP + Servlet

MariaDB (via JDBC using mariadb-java-client)

Maven for dependency management

Tomcat (or any Servlet container)

🚀 Features
👥 User Features

Register & Login

View movie list

View available shows

Choose seats

Book tickets

View booking history

🎬 Admin Features

Add Movies

Manage Shows

🗄️ Database Configuration

Update your DB credentials inside:

DBConnection.java

Example:

private static final String URL = "jdbc:mariadb://localhost:3306/movie_booking";
private static final String USER = "root";
private static final String PASSWORD = "password";
Import SQL Schema

Create database:

CREATE DATABASE movie_booking;

Import tables manually (based on your models: user, movie, show, seat, booking).

▶️ How to Run the Project

Install Tomcat or any Java Servlet container

Configure database credentials in DBConnection.java

Build using Maven:

mvn clean package

Deploy the WAR file to Tomcat or run through IDE

Open in browser:

http://localhost:8080/boooking-master/
📌 Servlets Overview
Servlet	Description
AuthServlet	Handles login/register
MovieListServlet	Displays movie list
ShowListServlet	Shows list of shows for a movie
SeatSelectionServlet	Displays seat status
BookingServlet	Confirms booking
AdminMovieServlet	Admin movie operations
🧩 DAO Layer

Handles database operations:

UserDAO → handle user login & registration

MovieDAO → fetch movie list

ShowDAO → fetch shows per movie

SeatDAO → fetch/update seat availability

BookingDAO → save bookings

🌐 JSP Pages
Page	Purpose
index.jsp	Homepage
login.jsp	User login
register.jsp	User registration
movies.jsp	List movies
shows.jsp	Show timings
seats.jsp	Seat selection UI
mybookings.jsp	User booking history
admin_add_movie.jsp	Admin movie addition
📄 web.xml Mapping

Check WEB-INF/web.xml for servlet mappings.

📬 Contact / Contribution

Feel free to improve this project:

Add payment module

Add admin dashboard

Add movie posters

Improve seat UI

🙌 Credits

Built using JSP, Servlets, JDBC, and MariaDB.
