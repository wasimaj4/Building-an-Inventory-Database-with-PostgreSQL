Project Description: Building an Inventory Database with PostgreSQL
Overview
This project involves designing a PostgreSQL database schema to manage and track mechanical parts inventory. The database will store crucial information about each part, including its description, manufacturer details, category, current location in the storeroom, available quantities, and associated reordering options. The goal is to create a robust structure that ensures data integrity and supports efficient inventory management operations.

Key Components and Constraints
Parts Table:

Central table storing information about each mechanical part.
Constraints include ensuring uniqueness and non-emptiness of the code column.
All parts must have a description, enforced by a NOT NULL constraint.
Reorder Options Table:

Tracks reordering details such as quantity and price per unit.
Constraints ensure both price_usd and quantity are NOT NULL and positive.
Additional constraint limits the price per unit within a specified range.
Locations Table:

Manages the physical locations of parts in the storeroom.
Ensures each location has a positive quantity of parts.
Implements a uniqueness constraint to prevent duplicate entries for the same part and location combination.
Manufacturer Table:

Stores information about part manufacturers.
Ensures all parts listed in the parts table reference a valid manufacturer.
Supports updates, such as merging manufacturers, to maintain data integrity across related tables.
Data Quality and Integrity
The schema includes various constraints to enforce data quality, such as NOT NULL checks and range limitations on price.
Relationships between tables ensure that only valid data entries are accepted, reducing errors and inconsistencies.
Updates and merges are managed carefully to maintain referential integrity and accuracy in tracking part manufacturers and locations.
Application and Use
Designed for integration with an inventory management application that interacts with the database.
Supports queries and updates from multiple users while maintaining the integrity of stored data.
Provides a structured approach to managing inventory, enabling efficient tracking, reordering, and location management of mechanical parts.
