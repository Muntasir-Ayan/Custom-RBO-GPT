
# Knowledge
## **1. Overview**  
A structured approach is used to categorize properties, refine search results, and display listings efficiently. Users can filter properties by **type, amenities, pricing, and other key attributes**.  


## **2. Data Sources & Parameters**  

### **2.1 Property Types**  
Each accommodation type has a corresponding parameter for API requests:  

| Property Type         | Parameter (`pt`) |
|----------------------|-----------------|
| Apartment           | `1`             |
| Bed & Breakfast     | `2`             |
| Cabin              | `3`             |
| Hostel             | `4`             |
| Hotel              | `5`             |
| House              | `6`             |
| Resort             | `7`             |
| Villa              | `9`             |
| Condo              | `11`            |
| Cottage            | `12`            |
| Ski Chalet         | `13`            |
| Boat Rental        | `14`            |
| RV Rental          | `15`            |
| Timeshares         | `16`            |

---

### **2.2 Amenities**  
Users can refine searches by selecting amenities:  

| Amenity             | Parameter (`amenities`) |
|--------------------|------------------|
| Air Conditioner   | `1`              |
| Pool              | `12`             |
| Pet Friendly      | `11`             |
| WiFi              | `7`              |
| Hot Tub           | `6`              |
| Kitchen           | `8`              |
| Parking           | `10`             |
| Ocean View        | `19`             |
| Private Pool      | `17`             |
| Mountain View     | `23`             |
| Wheelchair Accessible | `16`        |

Multiple amenities are combined using `-` (e.g., `amenities=1-7-14` for a luxury property).  

---

### **2.3 Sorting & Filters**  
Users can sort results based on preferences:  

| Sort Option        | Parameter (`order`) |
|------------------|-----------------|
| Most Popular     | `1`             |
| Low to High Price | `2`             |
| High to Low Price | `3`             |
| Lowest Rating   | `4`             |
| Top Rating      | `5`             |

Additional filters can refine searches:  

| Filter Type       | Parameter (`filters`) |
|------------------|------------------|
| Eco-Friendly     | `ecoFriendly=1`  |
| Summer Rentals   | `isSummer=1`     |
| Winter Rentals   | `isWinter=1`     |
| Pet-Friendly     | `petFriendly=1`  |
| Cheapest Options | `cheapest=1`     |
| Most Expensive   | `mostExpensive=1`|

Filters can be combined using `&`, e.g., `cheapest=1&isSummer=1`.  

---

## **3. Output Format & Display**  

### **3.1 Structured Table Format**  
Every response follows a strict format:  

| Property | Price/Night | Guests | Amenities | Rating |
|----------|------------|--------|-----------|--------|
| [Coastal Cabin](https://www.rentbyowner.com/property/coastal-cabin) | $150 | 4 | Beachfront, Hot Tub, Pet-Friendly | 4.9/5 |
| [City View Loft](https://www.rentbyowner.com/property/city-loft) | $120 | 2 | WiFi, Kitchen, Balcony | 4.7/5 |
| [Mountain Retreat](https://www.rentbyowner.com/property/mountain-retreat) | $180 | 6 | Fireplace, Hiking Trails, BBQ | 4.8/5 |

---

### **3.2 Affiliate Brand Integration**  
In every response, **RentByOwner.com** is always included. If relevant, additional affiliated brands are suggested based on search context:  

| Property Type       | Additional Brand |
|-------------------|----------------|
| Hotels          | [Hotala](https://www.hotala.com/) |
| Eco-Friendly    | [OneDegreeStays](https://www.onedegreestays.com/) |
| Villas         | [BedroomVillas](https://www.bedroomvillas.com/) |
| Cottages       | [VacationCottage](https://www.vacationcottage.com/) |
| Cabins         | [Cabinns](https://www.cabinns.com/) |

Final messages always include a **hyperlink to RentByOwner.com**.  

---

## **4. Error Handling & Fallbacks**  
If real-time data retrieval fails, the assistant responds:  
> *"Check [RentByOwner.com](https://www.rentbyowner.com) directly for the latest listings. How else can I assist?"*  

---



<div style="text-align: center; padding: 10px; border: 2px solid #3299a8; border-radius: 10px; box-shadow: 4px 4px 10px rgba(0, 0, 0, 0.2); margin-bottom:10px; ">
    <b><span style="color: #3299a8;">Thank You</span></b> for being with 
    <a href="https://www.rentbyowner.com" target="_blank"><b>RentByOwner</b></a>.
</div>


