# Documenting Performance Metrics

When completing user research about performance reporting and the use of business intelligence within the Food Standards Agency, one recurring theme discovered was that users consistently find it challenging to locate an authoritative definition or reach a shared understanding of the metrics used to measure performance.

Looking around for well-established methods by which metrics should be templated TO communicate their function to users, I found very little. A considerable amount has been written about designing metrics, evaluating their effectiveness, and deep dives into some of the most common performance metrics (particularly metrics about digital services) but almost nothing about communicating them to users. Whilst one of the strengths of a good performance metric is that it is somewhat self-evident, as processes and services become more complex, so does understanding them using only a handful of basic performance metrics.

This document has been written to try to help solve that problem by providing a template by which existing and new performance metrics can be documented. By laying out the key characteristics of a performance metric in a consistent way it is hoped that users will gain a better understanding of individual metrics, how metrics relate to each other, and the relative strengths and weaknesses of using any given metric. In addition, by creating a consistent view, it may be easier for users to understand that they are looking at a metric definition and pull out the pertinent information they need more quickly. This is really about the metadata of metrics, with a splash of style guide particularly for users within The Agency, other users may already have established style guides for documenting metrics.

### Publishing Performance Metrics

The most important consideration for performance metric documentation is version control. The user must always be confident that what they are looking at is the most up to date version. We're pretty agnostic about how you do that, but as you can probably tell we're definite fans of GitHub as markdown is easy to get to grips with, but you could use a wiki or an intranet. Just please, please, don't use a fixed file, and not a PDF, you'll be laughed out of town I expect.

## Metric Name

Rather obviously, the metric definition should start with the name. When naming metrics, you should consider the following;
 
 - Is there already an established name used widely throughout the sector for this metric? If there is, use that.
 - Use plain language, and avoid the use of acronyms within metric names, all you will achieve is to make unfamiliar users look up a second thing.
 - In the context of the domain, does the shortest possible name have an obvious meaning? i.e. "value for money" is a quite generic name, but when considered within the domain in which it sits, does it become obvious? If not, you probably need a more specific name.
 - Try to avoid referring to specific dimensions directly in the metric name, unless they are always cut by that specific interval. For example, "widgets per hour" is not a good metric name if users can also cut the measure by other time intervals (i.e. widgets per month), but is useful if even when you do, you still see the same value. i.e. Running the widgets per hour report grouped by month and the value is still widgets per hour, broken down by month.
 - Be mindful that metrics frequently appear on charts or dashboards, where screen estate is at a premium, so brevity in metric names is preferable. Longer names frequently end up abbreviated into incomprehensible acronyms, which then themselves become embedded into the language of an organisation, and acronyms make unfamiliar users look up a second thing.
 - Avoid using numbers in metric names, i.e. "quarter-hour" rather than "15 minutes".
 
When documenting existing metrics consideration should be given to changing the metric name if it fails to meet one or more of the style criteria, but only if the timing is appropriate. For example, as part of a wider review of performance within a specific domain or the redevelopment of a business process or service. When documenting well established metrics for the first time, the original names should be used to meet users' existing expectations.
 
### Key Performance Indicator
 
There are many articles, blogs, guides, and even books on identifying, selecting, and developing key performance indicators. We're not looking to cover that here. As far as documenting your KPI's goes, what is important is that they are easily identifiable and that their purpose is clearly tied to strategic objectives and explained as such. Depending on how you choose to communicate your metrics you could do any of the following;
 
 > Metric Name **(KPI)**
 
 or
 
 > **Metric Name**  
 > _Key Performance Indicator_  
 
 If you're feeling adventurous, maybe use a small inline graphic if your chosen publishing platform supports it? This is one of the reasons we like GitHub, and this was a good excuse to draw some chevrons, I really like chevrons. (You'll probably want to go smaller.)
 
 ![KPI](https://github.com/adamlocker/Metric_Templating/blob/master/Images/KPI.png "Key Performance Indicator")  

### Domain and Theme
 
In this section you should make it clear the domain(s) to which the metric is applied. These should be listed by strength of association rather than another method of sorting such as alphabetical. You should also categorise the metric by an appropriate theme or themes. Ideally, the available themes should be a centrally controlled vocabulary to limit the overall number of terms and avoid ambiguity, such as "Finance" and "Financial" being used interchangeably.
 
It is important to keep domains and themes distinct. Domains are frequently expressed by business area or functions that the business organises itself by, themes should be able to be used across domains. For example:
 
 > **Domain:** Production  
 > **Themes:** Profitability, Output, Efficiency  
 
## Metric Purpose
 
The most important part of metric definition is communicating the purpose of that metric. Most well-defined metrics are clear about what is being measured, and what action should or could be taken based on that measurement. For example;

> "Hourly production rate shows the number average number of widgets made per hour during the day. The minimum number of widgets per hour will be set by the planning and performance team, if the rate of production falls below that value, production line managers should contact the planning and performance team and ask them to re-profile production resources."

The entire function of this section is to communicate the purpose as succinctly as possible. Keep it brief.

### Calculation

If the metric is calculated in any way, it should be made clear here, preferably in plain language. Some more complex metrics may require mathematical notation, you shouldn't be afraid to use that if necessary. Credit the user with the gumption to understand it, but be prepared to rewrite it if you are asked to make it clearer. For example;
 
 > Total number of widgets made in reporting period / total number of hours in reporting period  
 
or 
 
 ![Equation](https://github.com/adamlocker/Metric_Templating/blob/master/Images/Equation.png "Equation example")
 
 _Note: Calculation is not the same as aggregation or averaging, which is covered later on._
 
## Dimensions
 
A dimension is simply a term for referring to the way in which you can "slice" a metric. A good rule of thumb is that if you could show the measure on a line or column chart, a dimension would be any acceptable way to divide the data along the x-axis. The most common dimensions for a metrics are time and geography, but other dimensions are available. When designing new metrics and thinking about dimensions, bear in mind that it is usually better to record things at an atomic level and aggregate them as needed as you can't unpick them once you start storing the data.
 
Dimensions should be clearly laid out to show the name of the dimension, and all the categories within it. Where a category does not have an immediately obvious definition, you should endeavour to link out to a reference list which defines it. This can be common problem for geographical dimensions, as things like "region" can have multiple meanings. For example, the dimensions for our "Widgets per hour" metric might look like this;
 
 >**Time:** Hour, Day, Week, Month, Quarter, Calendar Year, Financial Year.  
 >**Geographic:** Factory, Area, Region, Country, World. _(Area and Region would be defined somewhere else for this company.)_  
 >**Staff Group:** Employee, Team, Shift.  
 
_Note: Keep the language as plain as possible, it is tempting to use temporal rather than time, but all you're doing is showing off your own vocabulary._
 
## Functions, Aggregations, and Averages
 
Make it clear when a metric can be aggregated or averaged, or when other functions such as "minimum", "maximum", or "count" can be applied to the results returned to the user. If the metric is natively reported as an average, you should make it clear whether that is the mean, median or mode, even if there is only one average used.
 
 >**Functions:** Minimum, Maximum.  
 >**Aggregations:** This metric should not be aggregated.  
 >**Averages:** Mean (default), Median.  
 
## Targets, Thresholds, and Business Logic

This is particularly important for key performance indicators, and any metric that is listed as a KPI must have this section, otherwise it cannot reliably be considered a key performance indicator. Targets are ideally a hard number, something to aim for, but can also be a range where that is important. It is also important to specify the minimum interval over which the target applies, as frequently measuring a KPI on an hourly or even daily basis can become counterproductive and a longer timeframe should be used to mitigate that tendency. Thresholds should be considered advisory and perhaps include in the definition several ranges. Business logic should make it clear when a specific action will happen based on targets or thresholds being missed or exceeded. For example;
 
 > **Target**: Average to exceed 9.4 widgets per hour for this factory (monthly, quarterly or yearly).  
 > **Thresholds:** The lower acceptable limit is 5.8 widgets per hour, there is no upper limit.  
 > **Business Logic:** Falling below the lower threshold in-day will automatically notify the resourcing team. This metric falling below the lower threshold over a week will trigger an early monthly review.  
 
## Strengths and Weaknesses

It is important to be honest with users about the strengths and weaknesses of any given metric, particularly those used to measure performance of an individual or team and against which targets are set. Users will quickly work out ways in which they can manipulate metrics to their advantage (or others' disadvantage) when too much emphasis is placed on meeting (or not missing) a target. Whether you like it or not, any metric with a target will drive the behaviour of those being measured, for good or for bad, so you should be sure to take a holistic view of overall performance rather than relying on only one or two key performance indicators. For example;
 
 > **Strengths:** This metric is easy to understand, and measurable at a very granular level, meaning in-day or even in-hour adjustments can be made, think of it much like the speedometer on your car.  
 > **Weaknesses:** Like all mean average metrics, this can be susceptible to statistical outliers skewing the result. Where possible you should view the metric over the largest possible timeframe to mitigate this.  
 
## Related Metrics

Using the information about the domain and theme of the metric should make this bit easy. It is important to only list other metrics which are closely related to this metric, have a large impact on, or are significantly impacted by changes to it. You should explain the relationships using plain language, but highlight the specific metric names in some way, preferably with a link to the definition for that metric. For example;
 
 > This metric is closely related to **Widgets per Full Time Equivalent**, and can be heavily impacted by the metric **Raw Materials Shortfall Percentage**.
 
_Imagine the bold metric names are links to their definitions, just imagine!_
 
## Data Sources

When documenting metrics you should be clear about where the data comes from, but not in a technical way. You should make it clear if the data is collected by an automated or validated process or by a manual one. If good technical documentation exists (i.e. schema for the one database a metric uses) then you can consider providing a link to it along the lines of "for technical documentation related to this metric please see **URL**. A List of data sources is fine, but for complex processes a diagram can be worthwhile, especially when the point in the process at which the data is captured is important. For example;

 > All the data to calculate this metric comes from our automated production line software, BERTHA. Lovely BERTHA.

## Reference Data

Reference data will most frequently be the data used to dimension the metric such as a reference list which describes the geographic arrangement of an organisation, or even a staff list. When documenting metrics you should never assume that the reference data is obvious. By being explicit about where it has come from makes seeing the links between metrics easier. Where the reference data comes from an internal system, such as a HR system for a list of employees, you should reference that system explicitly. Where the data comes from a publicly available source, such as a register, you should provide a link to that register. For example;

 > This metric uses reference data on factory locations from our **list of production sites, areas, and regions**, country codes from the [GOV.UK Country Register](https://country.register.gov.uk/), and employee data from our HR system, **RAMBO**.

#Complete Example

Putting this all together, our metric documentation for **Hourly Production Rate** might look like this:

----

## Hourly Production Rate
![KPI](https://github.com/adamlocker/Metric_Templating/blob/master/Images/KPISmall.png "Key Performance Indicator")

### Domain and Themes
**Domain:** Production  
**Themes:** Profitability, Output, Efficiency  

### Metric Purpose
Hourly production rate shows the number average number of widgets made per hour during the day. The minimum number of widgets per hour will be set by the planning and performance team, if the rate of production falls below that value, production line managers should contact the planning and performance team and ask them to re-profile production resources.

### Calculation
![Equation](https://github.com/adamlocker/Metric_Templating/blob/master/Images/Equation.png "Equation example")

### Dimensions
**Time:** Hour, Day, Week, Month, Quarter, Calendar Year, Financial Year.  
**Geographic:** Factory, Area, Region, Country, World. _(Area and Region would be defined somewhere else for this company.)_  
**Staff Group:** Employee, Team, Shift.

### Functions, Aggregations, and Averages  
**Functions:** Minimum, Maximum.  
**Aggregations:** This metric should not be aggregated.  
**Averages:** Mean (default), Median.  

### Targets, Thresholds and Business Logic
**Target**: Average to exceed 9.4 widgets per hour for this factory (monthly, quarterly or yearly).  
**Thresholds:** The lower acceptable limit is 5.8 widgets per hour, there is no upper limit.  
**Business Logic:** Falling below the lower threshold in-day will automatically notify the resourcing team. This metric falling below the lower threshold over a week will trigger an early monthly review.  

### Strengths and Weaknesses
**Strengths:** This metric is easy to understand, and measurable at a very granular level, meaning in-day or even in-hour adjustments can be made, think of it much like the speedometer on your car.  
**Weaknesses:** Like all mean average metrics, this can be susceptible to statistical outliers skewing the result. Where possible you should view the metric over the largest possible timeframe to mitigate this.  

### Related Metrics
This metric is closely related to **Widgets per Full Time Equivalent**, and can be heavily impacted by the metric **Raw Materials Shortfall Percentage**.

### Data Sources
All the data to calculate this metric comes from our automated production line software, **BERTHA**. Lovely **BERTHA**.

### Reference Data
This metric uses reference data on factory locations from our **list of production sites, areas, and regions**, country codes from the [GOV.UK Country Register](https://country.register.gov.uk/), and employee data from our HR system, **RAMBO**.

----

You may or may not have found this useful, you may have found it spectacularly useless in fact, that's okay, it was a useful exercise for me. YMMV. :)