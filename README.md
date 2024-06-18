Write a program to book train tickets as per the details given below.
o
Train starts from station 'A and reaches station 'E
Assume the station order as A →> B →> C -> D -> E
Tickets can be booked from any place, le (A to 'E) or (C' to 'E) or (B' to 'D) etc...
A single ticket can be booked for multiple passengers. For example, if four people are travelling as a group, then it will be one ticket which will have the seating information for four people.
The train has only one coach with eight seats.
There can be a maximum of 2 Waiting list seats in addition to 8 confirmed seats.
Each ticket is uniquely identified by a sequentially generated number called PNR (both for confirmed and waiting list booking)
• If a passenger is allocated a seat for a ticket booked between D - E, then same seat should not be allotted for other tickets booked for A-›E, where as it can be allocated for any booking between stations A -> D
• Book tickets only when all the requested number of seats are available in a booking (either Confirmed or WL seat ) . For eg if 4 seats are requested, book only when all four are avallable but should not book when only 3 or less seats are available.
• Each ticket once booked / cancelled should have the source, destination, no. of seats, and the status (booked / cancelled) printed.
• A ticket should be cancelled using the PNR. Once a ticket has been cancelled, the PNR should not be reused again.
• Partial cancellation should be supported. i.e If a PNR has 4 seats booked, then it should be possible to cancel 2 seats alone.
When a ticket is cancelled, the passengers in the waiting list should be moved up provided following conditions are met Assume WL1 is from A →> D and WL2 is from D -> E. If a cancellation happens from C - E, in such case, the WL1 cannot be accommodated since it is from A -> D. So, here the WL2 should be moved to confirmed list
You can hard code the input in the below format in your program.
Booking format (<book> ‹Source station> <Destination station» ‹No of tickets») book,C,D,2
Cancel format (<cancel> <PNR Number> <Number of tickets>)
cancel,2,2
To print the booking summary & chart chart

Sample Data with explanation given below. Use the same data input in your program when showing
Sample Summary print for the above sample data
PNR 1, A to E, Seat Nos: 1, 2, 3, 4, 5, 6, 7, 8
PNR 2, A to E, Seat Nos: WL1, WL2
PNR 1, A to E, Seat Nos: 6, 7, 8 Canceled Seats: 1, 2,3, 4, 5
PNR 2, A to E, Seat Nos: 1,2
PNR 1, A to E, Seat Nos: - Canceled Seats: 1, 2, 3, 4, 5, 6, 7, 8
PNR 2, A to E, Seat Nos: - Canceled Seats: 1,2
PNR 3, A to C, Seat Nos: 1, 2, 3, 4, 5, 6, 7,8
PNR 4, C to E, Seat Nos: 1, 2, 3, 4, 5, 6, 7, 8
PNR 5, A to E, Seat Nos: WL.1, WL2
No seats available
PNR 3, A to C, Seat Nos: - Canceled Seats: 1, 2, 3, 4, 5, 6, 7,8
PNR 4, C to E, Seat Nos: - Canceled Seats: 1, 2, 3, 4, 5, 6, 7, 8
PNR 5, A to E, Seat Nos: 1,2
Data Input

bookAE.8
Notes for your understanding slone
bookAE,2
PNR 1 booked
cancel, 1,5 B
PNR 2 booked with 2 WL tickets
chart
tickets from PNR-1 will be cancelled, WLl & W.2 wil be confimed
cancel,1,3
prints booking, summary & chart
3 tickets from PNR-1 will be cancelied
cancel,2,2
2 tickets from PNR.2 will be cancelled. All the seats are free
book.A,C,8
PNR-3 will be booked
book.C,E,8
PNR-4 will be booked
book, A,E.2.
PNR-5 will be booked with 2 WL tickets
chart
prints booking summary & chart. All seats are occupied between all stations
book,C,D,2

cancel,3,8
due to ticket unavailability between stations, this booking should fail 8 tickets from PNR-3 will be cancelled
chart
prints booking summary & chart. You can see that all seats are occupied between C-»0 stations
cancel,4,8
8 tickets from PNR 4 will be cancelled and 2 WL tickets from PNR-5 will get confirmed
chart
prints booking summary &/chart. You can see that seats 1,2 will be occupied for stations A->D
book,C,E,3
PNR-6 will be booked
