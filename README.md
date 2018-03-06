Templating Metrics
==================

During the course of user research into performance reporting and use business intelligence within the Food Standards Agency, one recurring theme encountered is users consistently find it challenging to locate a authoritative definition or reach a shared understanding of the metrics being used to report on performance.

Looking around for well-established methods by which metrics should be templated in order to communicate their function to users, I found very little. A considerable amount has been written about deisgning metrics, evaluating their effectiveness, and deep dives into some of the most common performance metrics (particularly metrics about digital services) but almost nothing about communicating them to users. Whilst one of the strengths of a good performance metric is that it is somewhat self-evident, as processes and services become more complex, so does understanding them using only a handful of basic performance metrics.

This document has been written to try to help solve that problem by providing a template by which existing and new performance metrics can be documented. By laying out the key characteristics of a performance metric in a consistent way it is hoped that users will gain a better understanding of individual metrics, how metrics relate to each other, and the relative strengths and weaknesses of using any given metric. In addition, by creating a consistent view, it may be easier for users to understand that they are looking at a metric definition and pull out the pertinent information they need more quickly. This is really about the metadata of metrics, with a splash of style guide particularly for users within The Agency, others users may already have established style guides for developing metrics.

## Metric Name

Rather obviously, the metric definition should start with the metric name. But not all metric name are created equal, when naming metrics you should consider the following:
 
 - Is there already an established name for this metric? If there is, use that.
 - Use plain English, and avoid the use of acronyms with metric names, all you will achieve is to make unfamiliar users look up a second thing.
 - In the context of the domain, does the shortest possible name have an obvious meaning? i.e. "value for money" is a quite generic name, but when considered within the domain in which it sits, does it become obvious? If not, you probably need a more specific name.
 - Try to avoid referring to specific dimensions directly in the metric name, unless they are always cut by that specific interval. For example, "widgets per hour" is not a good metric name if users can also cut the measure by other time intervals (i.e widgets per month), but is useful if even when you do, you still see the same value. i.e. Running the widgets per hour report grouped by month and the value is still widgets per hour, broken down by month.
 - Be mindful that metrics frequently appear on charts or dashboards, where screen estate is at a premium, so brevity in metric names is preferable. Longer names frequently end up abbreviated into incomprehensible acronyms, which then themselves become embedded into the language of an organsiation, and acronyms make unfamiliar users look up a second thing.
 - Avoid using numbers in metric names where possible.