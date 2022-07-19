# recommender-systems-capstone
A capstone project for ["Recommender Systems" Coursera specialization by Minnesota university](https://www.coursera.org/specializations/recommender-systems), done in summer 2022.

# Project Objective
Your project should assess and recommend a recommender solution for the following scenario:

You work for a large online retailer (we’ll call it Nile-River.com) as a recommender systems expert on a team focused on direct sales to consumers in the US.

Your market research team has identified “back to school” as a critical time period for office product sales to consumers in the US. They note that the six weeks including and surrounding the month of August are responsible for 31% of yearly office product sales.

They also report that the surge in office product sales is not limited to traditional school products (such as notebooks, pencils, and erasers). Rather, it appears that once people are buying school products, they also buy other office products (indeed, more document shredders are sold during these six weeks than at any other time of the year, even tax preparation season).

Indeed, most large-dollar office-product purchases include a mix of inexpensive and more expensive products in the same transaction. This data suggests that it may be important to have inexpensive products as an entry point, but more expensive ones that build the transaction size. (For example, I buy paper and pens, and then realize I need several hundred dollars of laser printer toner.) Or alternatively that once someone comes to buy something large, they also fill in smaller items (one I’m buying a new printer, I might as well also buy a calculator and a box of colored paper clips).

They suspect that the surge in office product sales is due to in-person sales and promotion at retail outlets, with two particularly important prompts:

Visits to office products superstores (chain stores such as Staples and Office Depot) peak during this time of year. Once parents are in the store to buy supplies for their children, they see other products of interest.

Special displays are set up at “Big-Box” stores such as Wal-mart and Target with both school supplies and other office products.

Unfortunately, your site (Nile-River.com) does not experience as large a surge in office product sales during the back-to-school period. You do experience a surge (about double typical sales, or about 23% of annual consumer sales), but it is far below that of your offline competitors.

These figures include the results of existing promotions such as back-to-school banners and a free next-day shipping promotion for products sold during the two weeks when schools most commonly start classes (late August and early September).

Your challenge, therefore, is to develop a recommender system to increase sales of office products during this important time period. To maximize business value, you also have a set of key goals and constraints.

Given that your site already has a very effective product-association recommender system, you’ve been asked to focus on recommending products based on customer’s overall profiles, not their current browsing or basket.

Your product recommendations will be displayed in two places on the site:

Five products displayed on the “office products” landing page where customers will land if they click on banner ads (back to school shopping!) or select the office products category (from various menus or navigation aids).

Five products displayed as part of “other suggestions” that will be displayed as part of the shopping cart display and near the bottom of product pages (primarily will be placed on product pages from the same category, but also related products such as textbooks, school bags, and backpacks).

Research shows that additional sales at this time of year are divided fairly broadly among categories of office products (school supplies, consumable supplies, durable office equipment). Your recommender should respond to this research appropriately.

Your recommender should also address the finding above about having both cheaper and more expensive products available to attract customers.

Finally, Nile-River.com prides itself on having a much deeper product catalog than the typical big-box store. One of the key drivers of repeat business is customer discovery of new products they likely couldn’t buy at a local store. Your recommender should respond to this information appropriately.

# Data Description

The following 7 datasets were given:

**Items**

A data set derived from Amazon.com with product metadata and ratings data on office products. The data set is provided thanks to Julian McAuley at UCSD, and involves actual data from the period May 1996-July 2014. To make your computation more tractable, we’ve used a dense subset of the data (called the 5-core subset) that only includes items and users with at least five ratings. [Note that the original datasets are available at http://jmcauley.ucsd.edu/data/amazon/, though these should not be used for this capstone.

For each item, your meta-data includes:
* An item number
* Amazon’s ITEM number (“asin”)
* The item’s brand name
* The item title
* The item category (both leaf category and full path)
* A price in dollars

An availability score between 0 and 1 that reflects how widespread the product is in retail stores; higher scores reflect broad availability; lower scores indicate products not found in most big box store. Note that the availability score is synthetic (we created it), but for purposes of this capstone, treat it as if it were real data.

**Ratings**

A ratings matrix with a row for each item and columns representing each user (ratings are on a 1-5 star scale). Your ratings matrix includes all the ratings data you will receive (we have not separated out test and training data -- that’s your responsibility)

**CBF**

Predicted ratings output from a TFIDF content-based recommender.

**Item-Item**

Predicted ratings output from an item-item collaborative filtering recommender.

**MF**

Predicted ratings output from a matrix factorization (gradient descent) recommender.

**User-User**

Predicted ratings output from a user-user collaborative filtering recommender.

**PersBias**

Predicted ratings output from a baseline recommender that uses product and customer ratings distributions to provide personally-scaled average predictions.

