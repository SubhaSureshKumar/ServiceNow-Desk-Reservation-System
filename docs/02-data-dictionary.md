# Data Dictionary

## Table: Desk Reservation (x_2221041_hybrid_0_desk_reservation)

Status: Built

| Field Name   | Type      | Reference Table | Mandatory | Default   | Notes |
|--------------|-----------|-----------------|-----------|-----------|-------|
| employee     | Reference | sys_user        | Yes       | -         | Who booked the desk |
| desk_number  | String    | -               | Yes       | -         | Desk identifier, e.g. D-101 |
| start_time   | Date/Time | -               | Yes       | -         | Reservation start |
| end_time     | Date/Time | -               | Yes       | -         | Reservation end |
| state        | Choice    | -               | Yes       | requested | Requested / Confirmed / Checked-In / Checked-Out / Overdue / Cancelled |


## Table: loaner_hardware

| Field Name       | Type      | Reference Table       | Mandatory | Notes |
|-------------------|-----------|------------------------|-----------|-------|
| item_name       | String    | -                      | Yes       | e.g. Monitor, Dongle |
| reservation     | Reference | u_desk_reservation     | No        | Linked reservation, if any |
| issued_to       | Reference | sys_user               | No        | Who currently has it |
| state           | Choice    | -                      | Yes       | Available / Reserved / Issued / Returned / Under Sanitization / Damaged |
