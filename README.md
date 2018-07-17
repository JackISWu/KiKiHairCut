# TonyAndKevin
hair cut reservation platform

## Functions
Make Appointment operation:
 - choose barber shop(required frist), list all barber in specified order
 - choose barber, show hair style the barber can handle, available time, and branch the barber works
 - choose hair style, show barbers ho can handle it
 - choose time (set by each barber), show barbers who are available in that time
 - choose which branch (sorted by distance from user)(only valid when barber shop is decided)

Cancel appointment
 - rules (1hour before 100% deposit return, 30hour before 50% deposit return)

Comment (once created, cannot modify or delete)
 - comment on barber shop environment, barber
 - able to attach a photo
 - give a star (5 stars)

## DB Schemas
 - barber shop info
   shop_id, name
 - barber shop branch info
   branch_id, address, phone, is_main, shop_id
 - barber info
   barber_id, name, available_time_start, available_time_end, branch_id
 - customer info
   customer_id, name, birth_date
   
 - comment info
   comment_id, barber_id, customer_id, star, content, created_time
 - appointment_info
   appointment_id, customer_id, barber_id, created_time, canceled_time
 
 
## Tech stack
 - backend -> Spring Boot
 - frontend -> Angular 2
 - database -> MySQL
