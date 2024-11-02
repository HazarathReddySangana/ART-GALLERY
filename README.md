# ART-GALLERY


Here's a summary of the SQL code with key points for each section:

### 1. **Database Creation and Selection**
   - **Creates the Database**: `CREATE DATABASE artgallery;`
   - **Selects the Database**: `USE artgallery;`

### 2. **`artist` Table**
   - **Defines Artist Details**:
     - `artist_id`: Unique identifier, auto-incremented (Primary Key).
     - `name`: Artist's name, required.
     - `birthplace`: Artist’s birthplace, optional.
     - `age`: Artist’s age.
     - `style`: Artistic style (e.g., "Cubism," "Impressionism").

### 3. **`artwork` Table**
   - **Defines Artwork Information**:
     - `artwork_id`: Unique identifier, auto-incremented (Primary Key).
     - `title`: Artwork title, required.
     - `year_created`: Year the artwork was created, modified to `SMALLINT` for flexibility.
     - `price`: Artwork price.
     - `artist_id`: Foreign key linking to `artist_id` in the `artist` table.

### 4. **`gallery` Table**
   - **Defines Gallery Details**:
     - `gallery_id`: Unique identifier, auto-incremented (Primary Key).
     - `name`: Gallery name, required.
     - `location`: Gallery location.

### 5. **`artwork_gallery` Table**
   - **Creates a Many-to-Many Relationship** between `artwork` and `gallery`.
     - `artwork_id`: Foreign key referencing `artwork(artwork_id)`.
     - `gallery_id`: Foreign key referencing `gallery(gallery_id)`.
   - **Primary Key**: Composite key on `(artwork_id, gallery_id)`.

### 6. **Insert Statements for Sample Data**
   - **`artist` Table**: Inserts three sample artists with various art styles and birthplaces.
   - **`artwork` Table**: Adds three artworks, each associated with an artist.
   - **`gallery` Table**: Inserts three galleries with names and locations.
   - **`artwork_gallery` Table**: Establishes which artworks are displayed in which galleries.

### 7. **Queries to Retrieve Data**
   - **Retrieve All Artists**: Lists all records in the `artist` table.
   - **Retrieve Artworks by Specific Artist**: Filters artworks by artist (e.g., `artist_id = 1`).
   - **Retrieve Artworks in a Specific Gallery**: Lists artworks displayed in a given gallery (`gallery_id = 1`).
   - **Retrieve Galleries Showing a Specific Artwork**: Lists galleries displaying a specific artwork (`artwork_id = 1`).
   - **Calculate Total Value of Artworks in a Gallery**: Calculates the combined value of all artworks in a given gallery (`gallery_id = 2`).
   - **Retrieve Detailed Information**: Joins tables to show artwork title, artist name, and gallery name for each artwork.


![Screenshot 2024-10-29 141456](https://github.com/user-attachments/assets/e51da745-2554-41a4-8f1e-5787787d3aa7)
![Screenshot 2024-10-29 141536](https://github.com/user-attachments/assets/b9f02d00-4e4f-47f4-82c1-ba3752d1887c)
![Screenshot 2024-10-29 141609](https://github.com/user-attachments/assets/cd1dac0a-c45e-481e-828c-5f52f11e08ac)
![Screenshot 2024-10-29 141635](https://github.com/user-attachments/assets/27204b73-fc85-4adc-bd4d-e5c3d217dee7)
![Screenshot 2024-10-29 141701](https://github.com/user-attachments/assets/5b723264-5afb-401f-b7fa-ac05c993a12b)
![Screenshot 2024-10-29 141740](https://github.com/user-attachments/assets/cc33d06a-357b-4d2f-8094-e36ea1ad88df)
