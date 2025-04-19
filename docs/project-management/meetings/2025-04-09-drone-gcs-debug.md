# Meeting Minutes

## Drone GCS Debug

**Date:** Wednesday, April 9th, 2025  
**Time:**  3:55 PM - 4:32 PM Pacific Daylight Time  
**Location:** Zoom

---

### Attendees
- Tyler F.
- Kiruthika M.

---

### Agenda
1. Troubleshooting Map Data Population from Saved Frequency Data

---

### Discussion

#### Troubleshooting Map Data Population from Saved Frequency Data
- **Key Discussion Points:**
  - Save/load functions work, but saved frequency data does not display on the map.
  - Current map visibility is linked to backend-emitted signals for live sessions.
  - Merging saved and live data causes conflicts.
  - Tyler recommended creating a separate system for loading/displaying saved data.
  - Discussed UI options to distinguish saved sessions on the map (e.g., color, shape, or session ID labels).
  - No need for a new database table for visibility — only handled on the frontend.
- **Decisions Made:**
  - Develop independent backend/frontend handlers for saved frequency data.
  - Keep saved and live session data separate.
  - Use visual cues to differentiate saved data on the map.
- **Action Items:**
  - Create new display logic for saved frequency data — *Assigned to:* Kiruthika M. — *Due:* N/A
  - Design map distinction for saved sessions (e.g., color or label) — *Assigned to:* Kiruthika M. — *Due:* N/A

---

### Additional Notes
- Future enhancement: support multiple tracking sessions displayed together.
- Tooltip or color-based tracking session indicators suggested.

---

### Next Meeting
N/A
