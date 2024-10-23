# Doctor Appointment Chatbot

## Overview
This is a simple Python-based chatbot designed to help users book doctor appointments. It guides users through selecting a hospital location, department, and doctor, and then helps them book an appointment by selecting an available time slot. The chatbot also collects personal details of new patients for registration.

## Features
- **Location Selection**: Users can choose from six different cities for their appointment.
- **Department & Doctor Selection**: Users can pick a department or browse a list of available doctors.
- **Appointment Booking**: The bot shows available time slots for each doctor and allows users to book a preferred time.
- **User Registration**: For new users, the bot collects personal information like name, gender, date of birth, phone number, and email.
- **Persistent Data**: The bot stores appointment and patient details within the session.

## Code Structure
The chatbot is implemented using Python classes and functions to ensure modularity and scalability. Here's a breakdown of the key components:

### Class Initialization (`__init__`)
- Defines the hospital locations, departments, doctors, and available time slots.
- Initializes empty lists for storing appointments and patient information.

### Location Selection (`ask_location`)
- Displays a list of available locations and prompts the user to select one.
- Moves to the department selection step after the location is chosen.

### Department & Doctor Selection
- `ask_department`: Allows users to select a department or choose "Not sure" to browse all available doctors.
- `ask_doctor`: Prompts the user to pick a doctor from the selected department.
- `show_doctors_list`: Shows all doctors across all departments if the user is unsure of the department.

### Appointment Booking (`show_available_slots`)
- Displays available time slots for the selected doctor and prompts the user to choose a time.
- Once the time is selected, the appointment is booked.

### Patient Registration
- `ask_registration`: Asks whether the user is already registered. If not, collects the new patient’s information.
- `collect_new_patient_info`: Gathers personal details such as name, gender, date of birth, phone number, and email.

### Confirmation (`confirmation`)
- Confirms the booking and registration details to the user.

## Running the Bot
To start the bot, simply instantiate the `DoctorAppointmentBot` class and call the `run()` method:

```python
bot = DoctorAppointmentBot()
bot.run()
