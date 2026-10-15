# Online Bargaining System (Spring Boot)

Features: buyer/seller registration and login, BCrypt password hashing, session-based login, product listing, seller product creation, buyer offers, seller accept/reject actions, responsive Thymeleaf pages, and file-backed H2 database.

## Requirements
- JDK 21 or newer
- Maven 3.9+
- VS Code (Java Extension Pack recommended)

## Run
Open this folder in VS Code. In the terminal, run:

```bash
mvn spring-boot:run
```

Then open http://localhost:8080/ . Keep the terminal running while demonstrating the site. Press Control+C to stop it.

## Demo flow
1. Register a Seller at `/register`.
2. Log in as Seller at `/login` and add a product from the Seller Dashboard.
3. Open a private/incognito browser window (or log out), register a Buyer, and log in as Buyer.
4. Buyer Dashboard: submit an offer for the product.
5. Log back in as Seller and accept/reject the offer.

## Database
H2 file database is stored under `./data/` so records remain after normal app restarts. H2 console: http://localhost:8080/h2-console (JDBC URL `jdbc:h2:file:./data/bargainingdb`, user `sa`, blank password).

## Notes
This is a college demonstration project, not a production-ready commerce service. It uses session attributes and basic validation; before production, add Spring Security protections, CSRF protection, ownership checks for seller offers, and more complete validation.
