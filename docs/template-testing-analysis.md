# Testing Issue Templates - Sample Request

This file demonstrates how a teacher would use one of the issue templates and what information the Copilot coding agent would receive.

## Example: Adding a New Activity Using the Template

**Template Used:** 🎯 Add New Activity/Club

### Teacher's Input:
- **Activity Name:** Photography Club
- **Description:** Students will learn digital photography, photo editing techniques, and composition. This club is perfect for students interested in visual arts and digital media.
- **Meeting Days:** Wednesday
- **Start Time:** 15:30 (3:30 PM)
- **End Time:** 17:00 (5:00 PM)
- **Maximum Participants:** 15
- **Supervising Teacher:** Ms. Rodriguez (mrodriguez)
- **Special Requirements:** Requires computer lab access for photo editing software

### Technical Implementation Details Generated:

**Files to Modify:**
- `src/backend/database.py` - Add to initial_activities dictionary

**Code to Add:**
```python
"Photography Club": {
    "description": "Students will learn digital photography, photo editing techniques, and composition. This club is perfect for students interested in visual arts and digital media.",
    "schedule": "Wednesdays, 3:30 PM - 5:00 PM",
    "schedule_details": {
        "days": ["Wednesday"],
        "start_time": "15:30",
        "end_time": "17:00"
    },
    "max_participants": 15,
    "participants": []
}
```

**Acceptance Criteria Provided:**
- ✅ Activity appears in the activities list on the main page
- ✅ Students can register for the activity
- ✅ Activity shows correct schedule information
- ✅ Participant limit is enforced
- ✅ Activity is properly categorized

**Testing Checklist:**
- [ ] Activity appears on homepage
- [ ] Registration modal opens correctly
- [ ] Schedule displays properly in human-readable format
- [ ] Participant counting works correctly
- [ ] Activity filters work with new activity

## Analysis: Why This Template Works for Copilot

### ✅ Clear Requirements
The template provides all necessary technical details:
- Exact activity data structure needed
- Specific file locations to modify
- Precise data format requirements (24-hour time, days array)

### ✅ Complete Context
- Teacher's intent is clear
- Business requirements are specified
- Edge cases are considered (capacity limits, scheduling conflicts)

### ✅ Implementation Guidance
- Specific code changes required
- File paths and data structures
- Testing requirements

### ✅ Acceptance Criteria
- Measurable success metrics
- User experience requirements
- Technical validation steps

## Template Effectiveness Score: 9/10

**Strengths:**
- Comprehensive technical details for implementation
- Clear acceptance criteria
- Structured validation requirements
- User-friendly language for teachers
- Automatic assignment to @copilot

**Minor Improvement Opportunities:**
- Could include screenshot examples for UI changes
- Could reference similar existing activities for context

## Conclusion

These templates provide **more than sufficient detail** for a Copilot coding agent to:
1. Understand the teacher's requirements completely
2. Implement the changes without needing clarification
3. Test the implementation against clear criteria
4. Ensure the solution meets both technical and user requirements

The templates successfully bridge the gap between non-technical teacher requests and technical implementation requirements.