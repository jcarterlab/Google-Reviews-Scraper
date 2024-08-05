# Google-Reviews-Scraper

This script scapes Google reviews data from a CSV file of Google Maps links.

- It first selects the reviews button and sorts by newest first. It then scrolls to at least the target date (in this case the last 6 months) and calculates relevant metrics.
- It scrolls by selecting an xpath on the reviews and hitting the down key untill it is reached. A div number in the xpath is incremented following each successful scroll untill either the target date is met or the same date is detected x number of times and the program moves on.
- If an xpath isn't found (likely because the div number is out of range) the program tries again with a closer div number untill it can continue. If Google asks the user to sign in the program presses the back button and re-sorts the reviews by newest first so it can continue.
