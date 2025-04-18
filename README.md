# Real Estate Management System

A comprehensive C++ console application for managing real estate properties, including features for property management, broker statistics, and data persistence.

## Features

### Property Management
- Add single or multiple properties
- Display all properties
- Display properties with largest area
- Display sold properties
- Sort properties by price
- Edit property details
- Property status tracking (Sold, Deposited, Free)

### Property Information
Each property includes:
- Reference number
- Broker name
- Property type
- Region
- Description
- Price
- Total area
- Room count
- Floor
- Status

### Advanced Features
- Submenu for specialized queries
- Property editing system
- Comprehensive query system
- Data persistence (Binary and Text file support)

### Query System
- Find highest priced property in a region
- Calculate average property price by region
- Calculate broker sales percentage

## Technical Details

### Data Structure
```cpp
struct Имот {
    char реф_номер[21];
    char име_брокер[51];
    char тип_на_имота[51];
    char район_на_имота[51];
    char изложение[501];
    double цена;
    double обща_площ;
    int брой_стаи;
    int етаж;
    char статус[16];
};
```

### File Operations
- Binary file storage (`info.bin`)
- Text file storage (`info.txt`)
- Automatic data saving on program exit

## Requirements
- C++ compiler (supporting C++11 or later)
- Windows operating system (for console color support)

## Building the Project
1. Ensure you have a C++ compiler installed
2. Compile the source file:
   ```bash
   g++ RealEstateSystem.cpp -o RealEstateSystem
   ```

## Usage
1. Run the compiled executable
2. Choose data loading method (Binary or Text)
3. Use the main menu to:
   - Add properties
   - View properties
   - Edit properties
   - Run queries
   - Save data

### Main Menu Options
1. Enter a residence
2. Enter multiple residences
3. Display the residences
4. Display the residences with the biggest area
5. Display the residences which are sold
6. Order the residences by price
7. Submenu
8. Editing
9. Queries
0. Exit

## Data Persistence
- Data is automatically saved in both binary and text formats
- Binary format: `info.bin`
- Text format: `info.txt`

## Error Handling
- Input validation for all user entries
- Duplicate reference number checking
- File operation error handling
- Status-based editing restrictions

## Notes
- Maximum capacity: 100 properties
- Property status affects editing capabilities
- Sold properties cannot be edited
- Reference numbers must be unique 
