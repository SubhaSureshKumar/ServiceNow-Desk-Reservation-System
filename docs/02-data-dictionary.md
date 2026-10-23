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

## Table: Loaner Hardware (x_2221041_hybrid_0_loaner_hardware)

Status: Built

| Field Name | Type      | Reference Table                       | Mandatory | Default   | Notes |
|------------|-----------|---------------------------------------|-----------|-----------|-------|
| item_name  | String    | -                                     | Yes       | -         | e.g. Monitor, Dongle |
| reservation| Reference | x_2221041_hybrid_0_desk_reservation   | No        | -         | Linked reservation, if any |
| issued_to  | Reference | sys_user                              | No        | -         | Who currently has it |
| state      | Choice    | -                                     | Yes       | available | Available / Reserved / Issued / Returned / Under Sanitization / Damaged |

Note: Desk Number is set as the display column on Desk Reservation, so reference fields show readable values like D-101 instead of the creation timestamp.
