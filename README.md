# Logic (handler.py):
Implemented logic to count footfall for a given video clip.

## Simple Logic:
- Check for track ID of an object and increment whenever the object crosses the designated area (green area) **FROM ABOVE** (Ensure only movement towards the area from top to bottom is considered)
- Making use of a dictionary to store the state of the tracked object (inside)

## Cases Handled:
- People entering
- People re-entering (same individual have similar track_id)
