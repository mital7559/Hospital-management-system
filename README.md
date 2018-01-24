# Hospital-management-system

A patient can query for open slots for a particular day. In response, they receive a list of slots that're open on that day. If no slots are available on the requested date, they get an appropriate response.

Given a slot id, a patient can book an appointment or if previously booked, cancel an appointment. If a successful appointment is booked, the client receives a link to it along with a link to cancel the appointment. If for some reason the appointment booking failed, they get an appropriate response.

<b>Note</b>: 
- To book an appointment, a client must already be registered with the hospital.
- Per Slot only one appointment can be booked


# REST API urls :

1) <b>GET /slots</b>
	- Returns list of all slots for current date.
	
2) <b>GET /slots?date=20180101</b>
	- Returns list of all slots for requested date.

3) <b>GET /slots/1</b>
	- Returns slot which has Id 1
	
4) <b>PUT /slots/1?reserve=true</b>
	- Doctor will mark slot 1 as reserved
	
5) <b>PUT /slots/1?reserve=false</b>
	- Doctor will mark slot 1 as available/not reserved
	
6) <b>GET /slots/1/appointment</b>
	- Returns appointment details for slot id 1
	
7) <b>POST /slots/1/appointment?patientId=1234</b>
	- Book an appointment for slot id 1
	
8) <b>DELETE /slots/1/appointment?patientId=1234</b>
	- Cancel an appointment for the slot id 1
	
