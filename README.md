# TripSync by KDT

> A mobile-first travel planning prototype that helps groups turn different travel needs into one clear and considerate itinerary.

**Team:** KDT — CodeNection 2026 Participant Team   


---

## Overview

Planning a group trip can be stressful. Ideas are often scattered across group chats, Google Maps, notes, and spreadsheets. Friends may have different budgets, interests, food requirements, travel pace, and walking comfort. In many cases, one organiser has to make decisions without clearly knowing what works for everyone.

TripSync is a collaborative, mobile-first travel planning prototype. It helps travellers collect their preferences first, identify shared interests and important constraints, then produce a group-friendly itinerary.

> Most travel planners organise places. TripSync organises people’s needs before organising places.

## The Problem

Group travel planning becomes difficult when members have different needs:

- Different spending limits
- Different interests, such as food, culture, nature, shopping, or nightlife
- Dietary requirements, including vegetarian or halal options
- Different travel pace and walking comfort
- Sudden changes such as rain, attraction closures, or schedule changes

Existing tools can help people save locations or build an itinerary, but important personal constraints can still be missed until the group has already made a decision.

## Our Solution

TripSync creates a simple planning flow:

```text
Create or join a trip
        ↓
Complete a Travel Profile
        ↓
Collect profiles from group members
        ↓
Generate a Group Match
        ↓
Review a shared itinerary
        ↓
Adjust the plan when conditions change
```

Each traveller completes a **Travel Profile** with:

- Budget limit
- Travel pace
- Interests
- Food requirements
- Walking comfort

The **Group Match** feature then shows:

- A group compatibility score
- Shared interests
- The lowest group budget limit
- The preferred group pace
- Important planning considerations, such as dietary needs or low walking comfort

## Key Features

### 1. Trip creation and invitation

A user can create a trip by entering the trip name, destination, travel dates, and group budget target. The system creates a Trip Code that can be shared with other travellers.

### 2. Travel Profile

Each member adds their own preferences instead of relying on the organiser to guess them. The profile includes budget, pace, interests, dietary requirements, and walking comfort.

### 3. Group Match

TripSync combines the group’s submitted preferences and highlights where members agree or where the itinerary needs extra care.

For example, the app can remind the group to:

- Keep spending close to the lowest member budget
- Include vegetarian or halal-friendly meal options
- Avoid long walking distances for a member with low walking comfort

### 4. Considerate shared itinerary

The prototype provides a three-day itinerary with activity tags such as:

- Dietary-friendly
- Low walking
- Indoor
- Culture
- Photography
- Relaxed pace

This makes it easier for the group to understand why an activity was included.

### 5. Rainy Day Adjustment

When plans change, TripSync provides a clear alternative. For example, an outdoor activity can be replaced with an indoor activity while explaining the effect on walking distance, interests, and estimated cost.

## What Makes TripSync Different

TripSync is not only an itinerary builder. It acts as a lightweight planning mediator for a group.

| Standard travel planners | TripSync |
|---|---|
| Focus on places, routes, and schedules | Starts with each traveller’s needs and constraints |
| The organiser manually collects opinions | Every member completes a Travel Profile |
| Budget or dietary conflicts may appear late | Important constraints are highlighted before the itinerary is confirmed |
| A plan changes without clear reasoning | Alternatives explain what changed and why |
| Focuses mainly on location and timing | Also considers budget, food needs, pace, and walking comfort |

## Prototype Scope

This project focuses on validating the core preference-to-itinerary flow.

### Included

- Trip creation
- Trip Code invitation flow
- Travel Profile submission
- Group Match calculation
- Constraint and preference summary
- Shared itinerary display
- Rainy Day Adjustment scenario
- Mobile-first UI prototype

### Not included in this prototype

- Real-time cross-device collaboration
- User accounts and authentication
- Live Google Maps, weather, or route data
- Hotel, flight, ticket, or restaurant booking
- Payment and expense-splitting services
- AI-generated itineraries

TripSync Beta currently stores prototype data locally in the browser. In a future version, a shared database would allow every traveller to complete their profile from their own device and update the Group Match in real time.

## Design Prototype

The high-fidelity UI prototype was designed in Figma with a mobile-first layout.

[Open the Figma prototype](https://www.figma.com/design/QliyFeoKCuab7ycvQ7hj96/TripSync?node-id=0-1)

## User Flow

```text
Home
 ├─ Create a Trip
 │   └─ Enter trip details
 │       └─ Receive Trip Code
 │           └─ Add Travel Profiles
 └─ Join with Code
     └─ Enter Trip Code
         └─ Add Travel Profile

Travel Profiles
 └─ Group Match
     └─ Shared Itinerary
         └─ Rainy Day Adjustment
```

## Ideas Considered

| Idea | Decision | Reason |
|---|---|---|
| Constraint-based Group Match Engine | Kept | It directly addresses conflict around budget, dietary needs, accessibility, and travel pace. |
| Trip Code invitation system | Kept | It reduces friction and makes joining a group feel quick and simple. |
| In-app group chat | Dropped | Groups already use WhatsApp or Telegram. A chat feature would add scope without improving the core planning problem. |
| Flight and hotel booking integrations | Dropped | Booking APIs are too complex for the prototype. We focused on planning and preference matching first. |
| AI itinerary generator | Dropped | The core value is transparent group decision-making, not generating a generic list of places. |

## Technical Feasibility

### Prototype implementation

- **Frontend:** HTML, CSS, and JavaScript
- **Data storage:** Browser local storage for prototype data
- **Design:** Figma
- **Deployment:** GitHub Pages

### Future implementation

- **Frontend:** React or Next.js for a scalable mobile-first web application
- **Backend and database:** Firebase Firestore or Supabase for shared trip data and real-time updates
- **Authentication:** Secure sign-in and trip-level access control
- **External services:** Maps, weather, and place data APIs

## Privacy Note

TripSync Beta is an early-stage prototype. It does not process payments, bookings, passwords, precise location data, or sensitive personal information. Users should not enter sensitive information while testing the prototype.

## Team

TripSync is developed by **KDT**, a student team participating in CodeNection 2026.

| Role | Contribution |
|---|---|
| Product & Development | Product flow, prototype implementation, and deployment |
| Design & Research | UI/UX design, user research, and ideation |
| Documentation & Presentation | Project documentation, slides, and video presentation |

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
