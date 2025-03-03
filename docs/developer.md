# How to Create a Custom ChatGPT on Explore GPTs

## Introduction

OpenAI's **Explore GPTs** feature allows users to create customized ChatGPT versions tailored to specific needs. Whether you want a **personal AI assistant**, a **chatbot for customer support**, or a **creative writing companion**, Explore GPTs makes customization easy—**no coding required!**

In this guide, we’ll walk you through the **step-by-step** process of building your own GPT.

---

## Step 1: Cosmic Fusion Travel API

The Cosmic Fusion Travel API allows users to search for properties based on location, price, and other filters. You can retrieve property details, check availability, and filter properties based on specific criteria such as amenities, price range, and dates.

1. **API Version**:
   - Version: 1.1.0
2. **Base URL**:
   - https://api.cosmicfusion.travelai.com
3. **Authentication**: This API requires an API key for authentication. The key should be passed in the request header as `x-api-key`.

---

### Endpoints

#### 1. Search Properties

    GET /v1/property/search

Search for properties based on a keyword (such as a city name) and apply filters such as price range, property type, and more.

##### Parameters

- keyword (required, string): Search keyword, e.g., city name (e.g., "london").
- limit (required, integer): Number of results to return (default: 10).
- amount (optional, string): Price range in the format min-max (e.g., "100-200").
- startDate (optional, string, date format: YYYY-MM-DD): Check-in date.
- endDate (optional, string, date format: YYYY-MM-DD): Check-out date.
- pt (optional, string): Property type ID (from api-parameter-property-type.json).
- order (optional, string): Sorting order ID (from api-parameter-filter.json).
- filter (optional, string): Additional filters (e.g., ecoFriendly=1).
- amenities (optional, string): Amenities IDs (separated by "-"). Example: 1-7-6.

##### Response

- 200 OK: A successful response with a list of properties matching the search criteria.

#### 2. Get Property Details

    GET /v1/property/details/{propertyId}

Fetch detailed information about a specific property.

##### Parameters

- `propertyId` (required, string): The unique property ID from a search response.

##### Response

- **200 OK**: Detailed information about the property including its location, price, amenities, and policies.

#### 3. Search Properties by Title

    GET /v1/property/search/title/{title}

Search for properties by their title (e.g., hotel name).

##### Parameters

- `title` (required, string): The exact property title or name (e.g., "Sheraton").
- `countryCode` (optional, string): The country code for filtering properties (e.g., "us").
- `location` (optional, string): A specific location to filter properties (e.g., "Panama").

##### Response

- **200 OK**: A successful response with properties matching the given title and filters.

#### 4. Check Property Availability

    GET /v1/property/availability-check

Check the availability of a property for a given date range.

##### Parameters

- checkInDate (required, string, date format: YYYY-MM-DD): The check-in date.
- checkOutDate (required, string, date format: YYYY-MM-DD): The check-out date.
- partnerId (required, string): The partner ID (e.g., 33593320).
- feed (required, integer): The feed ID (e.g., 11).
- clientCountryCode (required, string): The country code of the client (e.g., "us").

##### Response

- **200 OK**: Availability details for the specified dates.

---

## Step 3: Fine-Tuning User Experience

### 1. Set Response Style

- Choose if you want responses to be **short, long, or conversational**.
- Decide if the GPT should **ask follow-up questions**.

### 2. Add API Integrations (Advanced Users)

- If you're a **developer**, you can integrate **external APIs** to make your GPT more powerful.

### 3. Test and Refine

- Use the **chat interface** to test responses.
- Adjust **instructions** based on interactions.

---

## Step 4: Publish and Share

### Save and Publish

- Once satisfied, click **“Publish”**.

### 🔗 Share with Others

- You can share your custom GPT via a **link** or keep it **private** for personal use.

---

## Conclusion

Creating a **custom ChatGPT** with OpenAI’s **Explore GPTs** is an exciting way to **personalize AI interactions**. Whether for **personal, business, or creative projects**, a tailored GPT can enhance **productivity and engagement**. Try building one today and **unleash the potential of AI!**

---

<div style="text-align: center; padding: 10px; border: 2px solid #3299a8; border-radius: 10px; box-shadow: 4px 4px 10px rgba(0, 0, 0, 0.2); margin-bottom:10px; ">
    <b><span style="color: #3299a8;">Thank You</span></b> for being with 
    <a href="https://www.rentbyowner.com" target="_blank"><b>RentByOwner</b></a>.
</div>
