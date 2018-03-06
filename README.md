# Documenting Performance Metrics

During the course of user research into performance reporting and use business intelligence within the Food Standards Agency, one recurring theme encountered is users consistently find it challenging to locate a authoritative definition or reach a shared understanding of the metrics being used to report on performance.

Looking around for well-established methods by which metrics should be templated in order to communicate their function to users, I found very little. A considerable amount has been written about deisgning metrics, evaluating their effectiveness, and deep dives into some of the most common performance metrics (particularly metrics about digital services) but almost nothing about communicating them to users. Whilst one of the strengths of a good performance metric is that it is somewhat self-evident, as processes and services become more complex, so does understanding them using only a handful of basic performance metrics.

This document has been written to try to help solve that problem by providing a template by which existing and new performance metrics can be documented. By laying out the key characteristics of a performance metric in a consistent way it is hoped that users will gain a better understanding of individual metrics, how metrics relate to each other, and the relative strengths and weaknesses of using any given metric. In addition, by creating a consistent view, it may be easier for users to understand that they are looking at a metric definition and pull out the pertinent information they need more quickly. This is really about the metadata of metrics, with a splash of style guide particularly for users within The Agency, others users may already have established style guides for developing metrics.

### Publishing Performance Metrics

The most important consideration for performance metric documentation is version control. The user must always be confident that what they are looking at is the most up to date version. We're pretty agnostic about how you do that, but as you can probably tell we're definite fans of github as markdown is really easy to get to grips with, but you could use a wiki or an intranet. Just please, please, don't use a fixed file, and definitely not PDF.

## Metric Name

Rather obviously, the metric definition should start with the name. But not all metric name are created equal, when naming metrics new metrics you should consider the following:
 
 - Is there already an established name for this metric? If there is, use that.
 - Use plain English, and avoid the use of acronyms with metric names, all you will achieve is to make unfamiliar users look up a second thing.
 - In the context of the domain, does the shortest possible name have an obvious meaning? i.e. "value for money" is a quite generic name, but when considered within the domain in which it sits, does it become obvious? If not, you probably need a more specific name.
 - Try to avoid referring to specific dimensions directly in the metric name, unless they are always cut by that specific interval. For example, "widgets per hour" is not a good metric name if users can also cut the measure by other time intervals (i.e widgets per month), but is useful if even when you do, you still see the same value. i.e. Running the widgets per hour report grouped by month and the value is still widgets per hour, broken down by month.
 - Be mindful that metrics frequently appear on charts or dashboards, where screen estate is at a premium, so brevity in metric names is preferable. Longer names frequently end up abbreviated into incomprehensible acronyms, which then themselves become embedded into the language of an organsiation, and acronyms make unfamiliar users look up a second thing.
 - Avoid using numbers in metric names.
 
 When documenting existing metrics consideration should be given to changing the metric name if it fails to meet one or more of the style criteria, but only if the timing is appropriate. For example, as part of a wider review of performance within a specific domain or the redevelopment of a business process or service. When documenting well established metrics for the first time, the original names should be used to meet users' expectation.
 
 ### Key Performance Indicator
 
 There are many articles, blogs, guides, and even books on identifying, selecting, and developing key performance indicators. We're not looking to cover that here. As far as documenting your KPI's goes, what is imprortant is that they are easily identifiable and that their purpose is clearly tied to strategic objectives and explained as such. Depending on how you choose to communicate your metrics you could do any of the following;
 
 #### Metric Name *(KPI)*
 
 or
 
 #### Metric Name
 ##### _Key Performance Indicator_
 
 Or if you're feeling adventurous why not use a small inline graphic if your chosen publishing platform supports it (this is one of the reasons we like github, and this was a good excuse to draw some chevrons, I really like chevrons. You'll probably want to go smaller.)
 
 ![KPI](https://github.com/adamlocker/Metric_Templating/blob/master/Images/KPI.png "Key Performance Indicator")
 
 ## Metric Purpose
 
 Front and centre of any metric definition should be the purpose of that metric. Most well defined metrics are clear about what is being measured, and what action should or could be taken based on that measurement. For example;
> "Hourly production rate shows the number average number of widgets made per hour during the day. The minimum number of widgets per hour will be set by the planning and performance team, if the rate of production falls below that value, production line managers should contact the planning and performance team and ask them to reprofile production resources."