
# 6. Review of the AI-generated analysis

| # | Where (ID or diagram) | Why it is wrong | Correction |
|---|---|---|---|
| 1 | FR-01 (Functional requirements) | It combines several different functions (register, log in, book and cancel) in a single requirement. A requirement should describe one function only. | Split it into separate requirements: user registration, login, booking and cancellation. |
| 2 | FR-02 (Functional requirements) | Not all bookings last one hour. Padel lasts 90 minutes, while tennis and futsal last 60 minutes. | Specify the correct duration for each sport: 90 minutes for padel and 60 minutes for tennis and futsal. |
| 3 | FR-03 (Functional requirements) | "Fast and easy to use" describes quality, not a function. It is also vague and cannot be tested as written. | Reclassify it as a non-functional requirement and define measurable criteria for performance and usability. |
| 4 | FR-04 (Functional requirements) | The identifier FR-04 is used twice, so the requirements do not have unique identifiers. | Assign a different identifier to each requirement, for example FR-04 and FR-05. |
| 5 | Forgotten password requirement | Sending the user's password by email is a security risk. Passwords should not be sent or stored in plain text. | Provide a secure password-reset process using a temporary link or token. |
| 6 | FR-05 (Functional requirements) | Rating courts and writing comments were never requested by the client. This feature has been invented. | Remove this requirement unless the town council explicitly approves the feature. |
| 7 | NFR-01 (Non-functional requirements) | PostgreSQL and the council's servers are technical infrastructure requirements, not quality requirements. | Move this requirement to the System Requirements section (SR). |
| 8 | NFR-02 (Non-functional requirements) | Java 25, Spring Boot and React were not specified by the client. The AI has invented the technology stack. | Remove the specific technologies. The technical solution should be decided by the development team and the client. |
| 9 | NFR-03 (Non-functional requirements) | Publishing the application in Google Play and the App Store contradicts Pedro's requirement for a responsive website because the IT department cannot maintain native applications. | Specify a responsive website that works on mobile phones and computers. |
| 10 | Use case diagram: Cancel booking -> Refund money | The refund is included automatically, but Variant B does not specify a refund policy. We cannot assume that cancelled bookings are refunded. | Remove the automatic refund use case until the town council confirms its refund policy. |
| 11 | Use case diagram: Book court and Log in | The extend relationship is incorrect. Logging in is not an optional extension of booking a court. | Treat login as a precondition for booking, or use an include relationship if login is modelled as a mandatory use case. |
| 12 | Class diagram: Booking and Court multiplicities | The multiplicities are reversed or incorrect. A booking must correspond to exactly one court, while a court can have many bookings over time. | Use the relationship: Court "1" -- "0..*" Booking. |
