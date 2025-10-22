<h1>📱 Flipkart Mobile Data Scraper</h1>

<p><strong>Flipkart Mobile Data Scraper</strong> is a Python-based data extraction tool that scrapes the latest <strong>mobile phone listings from Flipkart</strong>.  
It automatically collects information such as prices, ratings, offers, and specifications — and stores them in both a <strong>CSV file</strong> and a <strong>MongoDB database</strong>.</p>

<hr>

<h2>📌 Features</h2>
<ul>
  <li>✅ Extracts real-time mobile phone data from Flipkart</li>
  <li>✅ Collects detailed product information:
    <ul>
      <li>Product Name</li>
      <li>Rating & Review</li>
      <li>Number of Ratings</li>
      <li>Actual Price</li>
      <li>Selling Price</li>
      <li>Offer</li>
      <li>Memory</li>
      <li>Display</li>
      <li>Camera</li>
      <li>Battery</li>
    </ul>
  </li>
  <li>✅ Saves extracted data into <strong>Flipkart_Data.csv</strong></li>
  <li>✅ Inserts data into <strong>MongoDB</strong> for long-term storage</li>
  <li>✅ Structured and clean data format using <strong>Pandas</strong></li>
</ul>

<h2>🛠 Tech Stack</h2>
<ul>
  <li><strong>Language:</strong> Python 3.8+</li>
  <li><strong>Libraries:</strong> BeautifulSoup, Requests, Pandas, PyMongo, lxml</li>
  <li><strong>Database:</strong> MongoDB (local instance)</li>
</ul>

<hr>


<h2>🚀 Installation</h2>

<p><strong>Prerequisites:</strong> Python 3.8+ and MongoDB installed locally.</p>

<pre>
# 1️⃣ Clone the repository
git clone https://github.com/your-username/flip_scraper_csv.git

# 2️⃣ Create and activate a virtual environment
python -m venv env
source env/bin/activate     # On Windows: env\Scripts\activate

# 3️⃣ Install dependencies
pip install requests beautifulsoup4 pandas pymongo lxml

</pre>

<h2>🖥 Output Example</h2>

<p>After running the script, a file named <code>Flipkart_Data.csv</code> will be created, and all records will be stored inside MongoDB.</p>

<table>
  <tr>
    <th>Product Name</th>
    <th>Rating & Review</th>
    <th>Rating No</th>
    <th>Actual Price</th>
    <th>Selling Price</th>
    <th>Offer</th>
    <th>Memory</th>
    <th>Display</th>
    <th>Camera</th>
    <th>Battery</th>
  </tr>
  <tr>
    <td>Realme P1 5G</td>
    <td>4.3 ★</td>
    <td>12,345</td>
    <td>₹18,999</td>
    <td>₹14,999</td>
    <td>21% off</td>
    <td>8 GB RAM</td>
    <td>6.67-inch</td>
    <td>64MP + 16MP</td>
    <td>5000 mAh</td>
  </tr>
</table>

<h2>🧠 How It Works</h2>
<ul>
  <li><strong>Step 1:</strong> Sends an HTTP request to Flipkart’s mobile search results page.</li>
  <li><strong>Step 2:</strong> Parses the HTML response using <strong>BeautifulSoup</strong>.</li>
  <li><strong>Step 3:</strong> Extracts product data from HTML tags and stores it in a Python dictionary.</li>
  <li><strong>Step 4:</strong> Converts the dictionary into a <strong>Pandas DataFrame</strong>.</li>
  <li><strong>Step 5:</strong> Saves the data to <code>Flipkart_Data.csv</code>.</li>
  <li><strong>Step 6:</strong> Inserts all records into a <strong>MongoDB collection</strong> for databas
