# 🚕 Call Taxi Booking Application

This is a **low-level design** for a Call Taxi Booking system. It allocates taxis to customers based on proximity, availability, and earnings. The system is scalable to any number of taxis and simulates a basic dispatching service.

---

## ✨ Problem Statement

Design a **Call Taxi Booking** application with the following assumptions:

- There are `n` number of taxis. Initially assume `4`, but it should work for any number.
- The system consists of **6 points** (`A, B, C, D, E, F`), with **15 km** between consecutive points.
- Travel time between two consecutive points is **60 minutes**.
- Pricing:
  - ₹100 for the first 5 km.
  - ₹10 per km thereafter.
- Taxis initially stationed at point `A`.
- Allocation logic:
  - Prefer a free taxi at the pickup point.
  - Otherwise, allocate the nearest available taxi.
  - If multiple taxis are free at the same point, allocate the one with **lower earnings**.
  - Taxis earn only for the trip between pickup and drop-off.
  - If no taxis are free at that time, booking is rejected.

---

## 🧮 Features

✅ **Book a Taxi**  
Input customer details and receive an allocation or rejection.

✅ **Display Taxi Details**  
Show:
- Taxi Number
- Total Earnings
- Trip details (Booking ID, Customer ID, From, To, Pickup Time, Drop Time, Amount)


## 🎯 Example Usage

#### Input 1:
Customer ID: 1
Pickup Point: A
Drop Point: B
Pickup Time: 9
#### Output:
Taxi can be allotted.
Taxi-1 is allotted.
#### Input 2:
Customer ID: 2
Pickup Point: B
Drop Point: D
Pickup Time: 9
#### Output:
Taxi can be allotted.
Taxi-2 is allotted.
#### Input 3:
Customer ID: 3
Pickup Point: B
Drop Point: C
Pickup Time: 12
#### Output:
Taxi can be allotted.
Taxi-1 is allotted.


## 📝 Display Taxi Details:

Taxi-1 Total Earnings: Rs. 400
BookingID CustomerID From To PickupTime DropTime Amount
1 1 A B 9 10 200
3 3 B C 12 13 200

Taxi-2 Total Earnings: Rs. 350
BookingID CustomerID From To PickupTime DropTime Amount
2 2 B D 9 11 350


## 🧠 Assumptions
- Distance between consecutive points = `15 km`
- Travel time per segment = `60 mins`
- Minimum fare up to `5 km` = `Rs. 100`
- Beyond 5 km = `Rs. 10/km`
- Taxis earn only for the trip from pickup to drop-off.


## 🚀 Getting Started

#### 📂 Clone the repository:
```bash
git clone https://github.com/your-username/call-taxi-booking.git
cd call-taxi-booking
💻 Usage:
Implement booking logic in the source file.

Run the program.

Enter customer booking details to allocate a taxi.

🧪 Test Cases
Use the example cases above or add your own.

🧑‍💻 Contributing
Contributions are welcome! Please fork the repo and submit a pull request.

📄 License
This project is licensed under the MIT License.
