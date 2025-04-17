# Meeting Minutes

## WES 207 Weekly Meeting

**Date:** Tuesday, April 16th, 2025  
**Time:** 7:00 PM - 7:47 PM Pacific Daylight Time  
**Location:** Zoom

---

### Attendees
- Ricardo L.
- Connors J.
- Tyler F.
- William G.

---

### Agenda
1. Parts Order Update
2. Project Overview and Timeline Review


---

### Discussion

#### Parts Order Update
- **Key Discussion Points:**
  - Tyler asked for an update on the parts order.
  - Connors confirmed that the parts have not yet arrived. He mentioned that he pinged Professor Kastner, who indicated the parts were sent to WES lead.
  - It was noted that further follow-up may be required.
- **Decisions Made:**
  - The team agreed to re-ping Professor Kastner and confirm the shipment status of the ordered parts.
- **Action Items:**
  - Re-confirm parts shipment status by contacting Professor Kastner. — *Assigned to:* Connors. J — *Due:* ASAP


#### Project Overview and Timeline Review
- **Key Discussion Points:**
  - Tyler reviewed the project overview and timeline document (project repo) shared on Slack.
  - Overall, the document was approved with only minor comments and clarifications:
    - There was a suggestion to simulate TCP connections as an optional test method to avoid dependence on hardware.
    - The team discussed the benefits of using Protobuff for defining and packaging data packets to simplify serial communication.
    - Detailed dialogue was held regarding the method to monitor battery state-of-charge (using a voltage divider) and the challenges of converting digital readings to analog values.
    - Discussion covered transmission scheduling so that commands and data (e.g., tracker ID, timestamp, GPS coordinates) are sent without interference; Connors mentioned staggering transmissions (e.g., every 15 seconds) across towers.
    - The functionality of a command-line interface (CLI) versus a graphical user interface (GUI) was also debated. While a CLI is acceptable for testing purposes, a GUI might be developed later for more polished demonstrations.
  - Minor clarifications were made regarding comms packet structure based on prior implementations.
- **Decisions Made:**
  - The project overview and timeline document is accepted with minor modifications:
    - Confirm that a CLI interface is acceptable for testing; development of a GUI is optional.
    - Further analysis of the battery monitoring system (voltage divider approach) will be pursued.
- **Action Items:**
  - Look into hardware needed to provide an operational voltage level to ADC — *Assigned to:* Tyler F. — *Due:* ASAP

---

### Additional Notes
- N/A

---

### Next Meetings

**Meeting:** 207 Weekly Meeting  
**Date:** Tuesday, April 22nd, 2025  
**Time:** 7 PM Pacific Daylight Time  
**Location:** Zoom