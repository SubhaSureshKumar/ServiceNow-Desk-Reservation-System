# Data Dictionary

## Table: u_desk_reservation

| Field Name       | Type      | Reference Table | Mandatory | Notes |
|-------------------|-----------|------------------|-----------|-------|
| u_employee        | Reference | sys_user         | Yes       | Who booked the desk |
| u_desk_number     | String    | -                | Yes       | Desk identifier |
| u_start_time      | Date/Time | -                | Yes       | Reservation start |
| u_end_time        | Date/Time | -                | Yes       | Reservation end |
| u_state           | Choice    | -                | Yes       | Requested / Confirmed / Checked-In / Checked-Out / Overdue / Cancelled |

## Table: u_loaner_hardware

| Field Name       | Type      | Reference Table       | Mandatory | Notes |
|-------------------|-----------|------------------------|-----------|-------|
| u_item_name       | String    | -                      | Yes       | e.g. Monitor, Dongle |
| u_reservation     | Reference | u_desk_reservation     | No        | Linked reservation, if any |
| u_issued_to       | Reference | sys_user               | No        | Who currently has it |
| u_state           | Choice    | -                      | Yes       | Available / Reserved / Issued / Returned / Under Sanitization / Damaged |
