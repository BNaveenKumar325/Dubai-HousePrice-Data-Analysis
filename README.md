Data Preparation & Modeling :
I used Power BI’s Power Query Editor to clean and transform the
dataset. The original file contained fields such as location, price,
number of bedrooms and bathrooms, size in square feet, property type,
and other optional fields like year built .
The first task was to ensure data quality. I handled missing values
for example, removing rows where price or size was null, as these were
critical for downstream calculations. I also checked for duplicates and
removed any redundant entries.
• Next, I converted data types appropriately: price and size to
numeric, and categorical fields such as location and property type
to text.
• To enrich the data and make it more analytically useful, I created
several calculated columns:

• Price Per Square Foot : This was derived as price / size and gives
a normalized view of property pricing across various sizes.

• Property Age : For listings that included the year built, I created
a column calculating age using the formula 2025 - year_built.

• Listing Category : One of the more advanced steps: I created a
dynamic classification of properties into ‘Budget’, ‘Mid-Range’,
and ‘High-End’ segments based on the 33rd and 66th percentiles
of the price distribution. This segmentation helps stakeholders
instantly grasp the distribution of listings by affordability.

These transformations allowed me to build a structured semantic model
that supports slicing and dicing across multiple dimensions - location,
price range, furnishing status, developer, and more.

KPI Cards :
I used Card Visuals for four key indicators:
• Total Listings: This shows the count of all available properties
in the dataset.
• Average Price: A basic but important measure for benchmarking.
• Average Size (sqft): Useful for comparing average apartment or
villa sizes.
• Highest Priced Property: This gives agents and investors a
sense of the luxury ceiling.
I grouped these cards visually within a rectangle shape. I formatted the
shape with a soft gray background and a border to clearly delineate this
section as ‘Key Metrics’. I also sent the shape to the back layer so that
the cards are prominently visible on top.
This layout makes it easier for any user , whether a novice agent or a
senior policymaker to get an at-a-glance market snapshot.

Pie Chart :
I implemented a Pie Chart to represent the proportion of properties in
each listing category : Budget, Mid-Range, and High-End.
This visual is highly effective for summarizing market
segmentation. For instance, if Budget listings dominate the share, it
could indicate either low market affordability or oversupply of
economy-grade housing. Conversely, if High-End properties dominate,
it might be a signal of luxury-focused development.

I added data labels and percentage annotations for each slice to enhance
readability. From the pie chart, we can visually deduce how the market
skews , whether it’s investment-friendly, balanced, or tilted toward a
luxury audience.

Stacked Area Chart :
I created a Stacked Area Chart showing the growth of listings
over time by category.
Since our dataset may not have explicit time data like listing date, I
used the year_built field as a proxy to simulate a time dimension. I
plotted the number of properties over time, stacked by listing category.
This chart reveals development trends: for example, if High-End
property listings surged after 2015, or if Budget housing has stagnated,
this tells investors what’s been in focus over the years.
The stacked format also helps identify overlaps and market shifts,
whether Mid-Range properties are gaining share, or if Budget
properties are declining.

Stacked Column Chart :
Next, I used a Stacked Column Chart to show the distribution of listings
by bedroom count, further broken down by property type.
Here, each column represents a specific number of bedrooms —
say 2BHK, 3BHK, 4BHK — and the color-coded segments within each
column indicate whether the properties are apartments, villas,
townhouses, etc.

This visual is particularly valuable for real estate agents. It helps
identify demand and supply gaps. For instance, if 4-bedroom
apartments dominate the dataset, it could mean high buyer interest or
an oversupply in that segment.

Line and Clustered Column Chart :
I integrated a Line and Clustered Column Chart, which overlays
two different types of measures on a shared axis.
The columns represent the count of listings per year (or another
grouping), while the line overlays average price trends over the same
timeline.
This dual-axis visual helps policymakers and analysts correlate
supply with pricing. For example, a sudden spike in property count
followed by a plateau or decline in price might suggest oversaturation.
Conversely, rising prices amidst stable inventory may point to strong
demand.
I synchronized the axis labels, added tooltips, and used color coding to
make the chart intuitive and data-rich.

Scatter Plot :
I used a Scatter Plot to map Size (sqft) on the X-axis against Price
on the Y-axis, colored by listing_category.
This visual is powerful for identifying outliers and pricing
anomalies. For instance, a tiny property priced unusually high might
indicate a prime location or ultra-luxury build. Meanwhile, large but
inexpensive properties could be in less desirable areas.

Scatter plots also help investors spot value pocket - that is, properties
that offer large size for below-average price.

Through these visuals and filters, the dashboard becomes a powerful
storytelling tool.

• For investors, it identifies undervalued locations and segments
with high ROI potential.
• For agents, it highlights which types of listings are most common
and what configurations are in demand.
• For policymakers, the trends by year, price range, and furnishing
status can inform housing policy and urban planning.
Additionally, tooltips were added across visuals to enhance
interactivity. For instance, when hovering over a pie slice or scatter
point, you’ll see detailed price and size information.
This Power BI dashboard leverages clean data, calculated insights, and
thoughtfully designed visuals to provide real-time, interactive analytics
on Dubai’s housing market.
