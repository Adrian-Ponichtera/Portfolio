## Grocery Store Prices - Adrian Ponichtera

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Grocery Store Prices in Union County</title>
  <style>
    body {
      margin: 0;
      font-family: "Inter", Arial, sans-serif;
      line-height: 1.6;
      background: #f9fafb;
      color: #1a1a1a;
    }
    header {
      background: #0ea5e9;
      color: #fff;
      padding: 1.5rem;
      text-align: center;
    }
    main {
      margin: 0 auto;
      padding: 2rem 1rem;
    }
    section {
      margin-bottom: 2.5rem;
    }
    .grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 1.5rem;
    }
    @media (min-width: 900px) {
      .grid {
        grid-template-columns: 1fr 1fr;
      }
    }
    figure {
      margin: 0;
      background: #fff;
      border: 1px solid #e5e7eb;
      border-radius: 8px;
      overflow: hidden;
      box-shadow: 0 4px 12px rgba(0,0,0,0.05);
    }
    figcaption {
      padding: 0.75rem 1rem;
      font-size: 0.9rem;
      color: #6b7280;
      border-top: 1px solid #e5e7eb;
    }
    .map-card {
      background: #fff;
      border: 1px solid #e5e7eb;
      border-radius: 8px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.05);
      overflow: hidden;
    }
    }
    .map-wrapper {
      width: 120%;
      height: 1000px;    
    }
    .map-card-header {
      padding: 1rem;
      border-bottom: 1px solid #e5e7eb;
      font-weight: 600;
    }
    .content {
      background: #fff;
      border: 1px solid #e5e7eb;
      border-radius: 8px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.05);
      padding: 1.5rem;
    }
    footer {
      text-align: center;
      padding: 1.5rem;
      border-top: 1px solid #e5e7eb;
      color: #6b7280;
    }
  </style>
</head>
<body>
  <header>
    <h1>Grocery Store Prices in Union County</h1>
    <p>By: Adrian Ponichtera</p>
  </header>
  <main>
      <h2>Static Maps</h2>
      <div>
          <iframe src="Static Map 2.PNG" height="800" width="130%"></iframe>
          <figcaption>Spatial distribution of grocery stores with noted prices mapped against Income by Census tract.</figcaption>
          <iframe src="Static Map 1.PNG" height="750" width="130%"></iframe>
          <figcaption>Catchement areas of the two cheapest grocery stores.</figcaption>
      </div>
    <section>
      <div class="map-card">
        <div class="map-card-header"><a href="Interactive_Map_Final.html">Interactive Map</a></div>
        <iframe src="Interactive_Map_Final.html" height="500" width="95%"></iframe>
      </div>
    </section>
    <section>
      <div class="content">
        <h3>Analysis and Interpretation</h3>
        <p>
          I was inspired by the blog <a href="https://www.marketreportblog.com/"> The Market Report</a> which performed an online survey of grocery store prices in the United States northeast for 30 different stores using a set basket of 30 items. I edited the list down to 23 items that were most commonplace, easy to locate, and most used by consumers. This list included: 
<ul>
  <li>Broccoli crown 2 lb</li>
  <li>Gala apples 3 lb</li>
  <li>Bananas 3 lb</li>
  <li>Baking/russet potatoes 5 lb bag</li>
  <li>Organic spring mix, 5 oz</li>
  <li>Green seedless grapes, 3 lb</li>
  <li>Boneless skinless chicken breast, 3 lb</li>
  <li>Ground beef 80/20, 2 lb</li>
  <li>Pork loin roast or tenderloin, boneless, 4 lb</li>
  <li>Peeled deveined raw shrimp, 31-40 ct, 2 lb</li>
  <li>Deli cheddar, sliced, 1 lb</li>
  <li>Deli turkey, sliced, 1 lb</li>
  <li>4 muffins, assorted</li>
  <li>Penne Pasta, 1 lb</li>
  <li>Extra virgin olive oil, 16.9 fl oz</li>
  <li>All purpose flour, 5 lb</li>
  <li>Powdered sugar, 2 lb</li>
  <li>Toilet paper, 1 ply, 12 rolls x 1000 sheet (Scott or equivalent)</li>
  <li>Paper towels, 2 rolls</li>
  <li>Gallon 1% milk</li>
  <li>Large brown eggs, dozen</li>
  <li>Block Monterrey or pepper jack cheese, 8 oz</li>
  <li>Half and half, quart</li>
</ul> 
</p>
<p>
I created all datasets, other than this list of basket items. First, I created a database of grocery stores in Union County. I searched for some datasets online but I could not find ones that were up to date or complete so I built this myself. This consisted of me searching for grocery stores on google maps and noting the name, address, and municipality of each store. I excluded stores like Costco and Sam’s Club based on the fact that you need a membership to get into and I excluded Walmart and Target based on the limited scope of this project that had to be completed at the end of the semester.
</p>
<p>
After this process I had a dataset of about 40 grocery stores. Unfortunately, due to the limited time for data collection for this project I only tracked prices at 25 stores. Grocery stores were selected based on convenient routing availability. An effort was made to sample grocery stores of the same brand and to represent multiple municipalities. All grocery stores were full service except for Lidl and Aldi which contained pre-cut deli meats and cheeses as they do not have a delicatessen stand within the store itself. This could have skewed the Deli Cheddar and Deli Turkey items for these two chains because the quality of freshly cut cheeses and meats probably differs from those done days prior.
</p>
<p>
When noting the prices at grocery stores I chose the cheapest item of each category, which was usually the store brand, as long as the quality was not substantially different from items chosen in other stores. For items that had a weight, the price was taken from a package that contained a similar weight as the one in the spreadsheet since there are often discounts for larger packages. For example, I recorded the 2.83 lb package at $3.69 per pound rather than the 1.01 lb package at $3.99 per pound for the Boneless Skinless Chicken Breast, 3 lb. If items were on sale, then the sale price was listed. Some grocery stores have high prices but rely on constant sales to attract customers so it would be unfair to exclude sales. The sale price was recorded even if a membership was required to access the sale as long as the membership could be obtained at no cost.
</p>
<p>
This was all done in an excel spreadsheet. To make them mappable I had to geocode the addresses that I had noted and then attached the prices to that supermarket. Some minor issues came up with geocoding where an address was displayed in the wrong area which was caused by the abbreviation of a cardinal direction. Some addresses do not represent the building location of the supermarket, instead they represent the entrance to the strip mall that they are located. This had no impact on the analysis because this represented a very minor change in walk or drive shed analyses and made no difference to point locations when zoomed out to the entirety of Union County. No point locations were close enough to confuse them with other grocery stores. The interactive map takes the elements from the first static map so that they can be explored in more detail. The census tracts display detailed information when they are hovered over and when the grocery store circle markers are hovered over, they display the store name and the total basket price. When they are clicked, they compare the total basket price of that store with the average basket price of the data. The Shoprite 10 minute driveshed is also shown to illustrate the most common supermarket chain in the county. 
        </p>
        <p>
The first static map was created by mapping census tracts by income and excluding those with null values. CVs were calculated and high values were shaded. On top of this I plotted supermarket points as circle markers and shaded them based on the total calculated in my grocery store spreadsheet. The border of Union County, NJ was added for reference. The second static map was created by calculating the 10 minute driveshed from Lidl and Aldi grocery store points. Speeds of different road types were varied to represent actual conditions. Then the polygons were joined to the centroid of census blocks to create a block by block map of catchement areas. On top of this I mapped the different brands as unique markers to better show brand dispersion in the county. 
          </p>
        <p>
          Some further research that would enhance this project is to visit every grocery store in Union County, including Walmarts & Targets, and complete the dataset. If there were more time I would also attempt to find a dataset with commercial rental prices to overlay that over grocery store prices. Other than this, there are many ways to analyze this data with a host of variables that could interact with grocery store prices. Finally, a time series of data would be valuable in tracking the change in grocery store prices.
        </p>
        <table>
    <caption>Grocery Store Price Comparison</caption>
    <thead>
      <tr>
        <th>Name</th>
        <th>Total</th>
        <th>Food Total</th>
        <th>Other Total</th>
      </tr>
    </thead>
    <tbody>
      <tr><td>Aldi, Linden, NJ</td><td>$108.26</td><td>$96.08</td><td>$12.18</td></tr>
      <tr><td>Aldi, Roselle, NJ</td><td>$117.21</td><td>$108.41</td><td>$8.80</td></tr>
      <tr><td>Aldi, Union, NJ</td><td>$118.88</td><td>$110.08</td><td>$8.80</td></tr>
      <tr><td>Aldi, Springfield, NJ</td><td>$119.38</td><td>$110.58</td><td>$8.80</td></tr>
      <tr><td>Lidl, Garwood, NJ</td><td>$121.06</td><td>$113.68</td><td>$7.38</td></tr>
      <tr><td>Lidl, Union, NJ</td><td>$140.87</td><td>$127.20</td><td>$13.67</td></tr>
      <tr><td>Shoprite, Union, NJ</td><td>$145.43</td><td>$133.95</td><td>$11.48</td></tr>
      <tr><td>Shoprite, Linden, NJ</td><td>$155.65</td><td>$140.07</td><td>$15.58</td></tr>
      <tr><td>Shoprite, Garwood, NJ</td><td>$159.93</td><td>$145.85</td><td>$14.08</td></tr>
      <tr><td>Shoprite, Elizabeth, NJ</td><td>$161.34</td><td>$147.06</td><td>$14.28</td></tr>
      <tr><td>Trader Joe, Westfield, NJ</td><td>$164.67</td><td>$157.02</td><td>$7.65</td></tr>
      <tr><td>Supremo Food Market, Plainfield, NJ</td><td>$167.60</td><td>$153.96</td><td>$13.64</td></tr>
      <tr><td>Twin City Supermarket, Elizabeth, NJ</td><td>$170.19</td><td>$150.19</td><td>$20.00</td></tr>
      <tr><td>Stop & Shop, Berkely Heights, NJ</td><td>$170.80</td><td>$155.03</td><td>$15.77</td></tr>
      <tr><td>ACME, New Providence, NJ</td><td>$171.64</td><td>$155.66</td><td>$15.98</td></tr>
      <tr><td>Shoprite, Clark, NJ</td><td>$173.20</td><td>$159.22</td><td>$13.98</td></tr>
      <tr><td>SuperFresh, Linden, NJ</td><td>$175.02</td><td>$161.45</td><td>$13.57</td></tr>
      <tr><td>SuperFresh, Roselle, NJ</td><td>$175.39</td><td>$160.32</td><td>$15.07</td></tr>
      <tr><td>Twin City Supermarket, Plainfield, NJ</td><td>$177.99</td><td>$156.02</td><td>$21.97</td></tr>
      <tr><td>Universal Food Market, Rahway, NJ</td><td>$179.42</td><td>$155.32</td><td>$24.10</td></tr>
      <tr><td>Food Bazaar, Elizabeth, NJ</td><td>$179.74</td><td>$156.75</td><td>$22.99</td></tr>
      <tr><td>ACME, Kenilworth, NJ</td><td>$191.39</td><td>$176.42</td><td>$14.97</td></tr>
      <tr><td>Whole Foods, Vauxhall, NJ</td><td>$200.33</td><td>$183.00</td><td>$17.33</td></tr>
      <tr><td>Whole Foods, Clark, NJ</td><td>$206.48</td><td>$195.81</td><td>$10.67</td></tr>
      <tr><td>Kings Food Market, Garwood, NJ</td><td>$221.53</td><td>$202.55</td><td>$18.98</td></tr>
      <tr><td><strong>Average</strong></td><td><strong>$165.21</strong></td><td><strong>$150.65</strong></td><td><strong>$14.56</strong></td></tr>
    </tbody>
  </table>
      </div>
    </section>
  </main>
</body>
</html>
