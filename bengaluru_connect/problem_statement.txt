The Vision: "Bengaluru Connect" aims to be the ultimate platform for everything happening in the city. It will have two main features:
Event Ticketing: Users can book tickets for a limited number of seats at exclusive events, from a pottery workshop in Koramangala with 20 seats to a stand-up comedy show in Indiranagar with 100 seats.
Local News Feed: A highly active, real-time feed where users can post news, photos, and updates about their neighbourhood (e.g., "Road closure near MG Road," "New cafe opening in Jayanagar").
The Challenge:
As the architect, you must decide on the foundational database strategy for the entire platform. Write a brief, clear recommendation.

Here are the critical business requirements you must consider:

Requirement A (Ticket Sales): We absolutely cannot sell the same seat twice for any event. A transaction must be 100% reliable. If a user's booking fails halfway through, the seat must immediately be available for others.
Requirement B (News Feed): The news feed must be extremely fast and always available. We anticipate millions of users reading and posting concurrently. It's okay if a new post takes a few seconds to appear for everyone across the city, but the feed can never go down.
Requirement C (User Profiles): User profiles will be flexible. Some users might add a bio, others might link their social media, and others might have a portfolio of their photos posted on the feed. The profile structure will evolve over time.
Your Assignment: Write a recommendation memo (1-2 pages) that addresses the following:

Your Final Decision: State clearly which database type you recommend:
A Relational (SQL) Database for the entire platform.
A NoSQL Database for the entire platform.
A Hybrid Approach (using both for different parts of the platform).
Justification & Trade-offs: This is the most important part. Justify why you made your choice. Specifically explain briefly how your chosen approach will handle all three requirements (A, B, and C).

The Biggest Risk: Identify the single biggest technical risk of the approach you have chosen and briefly explain how you plan to manage it.

Note:
Your goal is not to find the one "right" answer, but to demonstrate that you can think through a complex problem, weigh the pros and cons, and defend your decision.
