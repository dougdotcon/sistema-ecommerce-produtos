# EcommerceScraperHub

A comprehensive solution for scraping product data from e-commerce platforms like Kabum and Pichau, storing it efficiently, and displaying it through a modern, responsive web interface built with Ant Design.

## Features

- **Data Extraction**: Automated scraping of product details from Kabum and Pichau.
- **Data Storage**: Stores extracted data in a structured JSON format.
- **Image Management**: Downloads product images and provides fallback assets for missing images.
- **Modern Web Interface**: A responsive and interactive UI built with Ant Design.
- **Advanced Filtering**: Filter products by category, price range, and source.
- **Search Functionality**: Full-text search across all product attributes.
- **Product Details**: Dedicated view for individual product specifications and details.
- **UX Enhancements**: Smooth animations, hover effects, and responsive layout for all devices.

## Tech Stack

- **Backend**: Python 3.x (Requests, BeautifulSoup, Faker)
- **Frontend**: HTML5, CSS3, JavaScript (React via Ant Design CDN)
- **Data Storage**: JSON file (`db.json`)

## Prerequisites

- Python 3.6+
- Modern Web Browser (Chrome, Firefox, Edge)

## Installation & Setup

### 1. Clone the Repository
bash
git clone https://github.com/your-username/ecommerce-scraper-hub.git
cd ecommerce-scraper-hub


### 2. Install Python Dependencies
bash
pip install -r requirements.txt


### 3. Run the Data Collection Scripts

**Step 3a: Scrape Product Data**
Run the main scraper to fetch products from the configured websites.
bash
python scraper.py


**Step 3b: Generate Fallback Images**
Create placeholder images for products that do not have images available.
bash
python gerar_imagem_fallback.py


*Note: This will generate a `db.json` file and a `images/` directory containing product assets.*

### 4. Launch the Web Interface

Simply open the `index.html` file in your browser or serve it via a local web server (recommended for CORS policies).
bash
# Using Python's built-in HTTP server
python -m http.server 8000
# Then navigate to http://localhost:8000


## Project Structure


ecommerce-scraper-hub/
├── scraper.py              # Main script for data extraction
├── gerar_imagem_fallback.py # Script to generate placeholder images
├── requirements.txt        # Python dependencies
├── db.json                # JSON database with product data
├── index.html             # Main entry point for the web app
├── screenshots/           # Visual comparisons of UI versions
├── images/                # Downloaded product images
└── README.md              # Project documentation


## How It Works

1.  **Scraping**: The `scraper.py` script uses Python libraries to send HTTP requests to e-commerce sites, parse the HTML responses, and extract relevant product information (name, price, category, source, image URL).
2.  **Data Processing**: The extracted data is standardized and saved into `db.json`. Simultaneously, images are downloaded and saved locally.
3.  **Fallback Images**: If a product lacks an image, `gerar_imagem_fallback.py` ensures a placeholder exists.
4.  **Frontend Rendering**: The `index.html` file loads the `db.json` data. It uses the Ant Design library (via CDN) to render a dynamic, filterable grid of products.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request