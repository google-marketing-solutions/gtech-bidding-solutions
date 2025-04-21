# **BidScript ReadMe**

Disclaimer: This is not an official Google product.

# **Solution Overview**

BidScript is an open-source suite of solutions, including the GA4 Bidder and Bidding IQ, that generate custom bidding scripts to use within Display & Video 360\. These solutions leverage predictive modeling to optimize bidding strategies based on different data sources and objectives for direct activation.

* **GA4 Bidder** leverages Google Analytics 4 data stored in BigQuery to automatically generate predictive models. It creates features, builds multiple models using BigQuery ML, selects the best one, and produces a Custom Bidding script, with the goal to influence conversion values when bidding.
* **Bidding IQ** utilizes a predictive model that identifies the most influential impression quality signals (like viewability, creative size, and device) impacting lower-funnel KPIs. It analyzes historical DV360 data (stored as a CSV or BigQuery) and target variable data to create Custom Bidding scripts weighted by the predictive values of these impression signals.

BidScript aims to enhance bidding performance by allowing advertisers to implement more sophisticated strategies based on data-driven insights, catering to various scenarios like limited online conversion data or driving deeper business goals.

# **Solution Use Cases**

## **GA4 Bidder**

Three main use cases:

1) Limited online conversion data
2) Non-revenue conversion events
3) Driving deeper business goals that aren’t inherent to the platform

## **Bidding IQ**

Two main use cases:

1) Performance advertisers looking to connect upper funnel strategies to final KPI.
2) Video advertisers that need guidance on selecting proper KPIs for comparability across awareness, consideration, and performance tactics.

##

##

# **Requirements**

## **Technical Skills**

These solutions are designed to require little to no coding and input from the user. They have minimal prerequisites, allowing advanced analysts to lead the process with consultation from data scientists before handing off to a media analyst for activation. Familiarity with GA4 and DV360 is necessary for defining use cases and activating the scripts.

In their current form, these solutions are substantial in their modeling approach and design. However, they also offer a foundation for further customization by advertisers and partners to further innovate and integrate into their proprietary tech stacks.

## **Data Requirements**

BidScript requires specific data depending on the chosen solution:

### **GA4 Bidder**

* 6+ months of data, with more being better.
* GA4 data stored in BigQuery.
* Optionally, additional data can be joined with your GA4 data, including holidays, promotional data, etc.
* The final granularity of your dataset should be one row per user with behaviors aggregated across all visits prior to a conversion.

#

### **Bidding IQ**

* 2 years of data (minimum 1 year) broken out by date.
* DV360 data stored in Google Sheets or BigQuery.
* Daily target KPI should be measured within 30 days of influencer impressions.
* Volume should be total volume (total conversions, all sales revenue, leads, etc.) for the time period, not just attributed volume.
* Data needs to be in the same realm of what is being tested (ex: 2 years of video data from DV360).

# **FAQ**

**Can these solutions be used for other platforms, like Google Ads and Search Ads 360?**
In its current form, BidScript solutions are designed specifically to leverage automation for use with DV30 and its custom bidding functionality. However, the underlying principles of using data-driven predictive models to inform bidding strategies can be applied to Google Ads and Search Ads using the model insights and outputs.

**What solution should I use if conversions is my goal?**
Bid towards conversion with [automated bidding](https://support.google.com/displayvideo/answer/2997422?hl=en-IE&sjid=11959840171476089715-NC) (i.e. max conversions), available directly in the DV360 UI.

**What should I use to bid towards revenue?**
In [Goal Builder](https://support.google.com/displayvideo/answer/11118987?hl=en-IE&sjid=11959840171476089715-NC), bid towards a Revenue Floodlight.
