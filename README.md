# List View (TBC)
API Endpoint: https://oracleapex.com/ords/teochewthunder/borrowing/`year`/`month`
Example: https://oracleapex.com/ords/teochewthunder/borrowing/2026/3

## HTML/CSS
Header and rows are styled using the same template grid format, for consistency.

## Properties
- `records`: An array of records that have been returned from the API endpoint. This is the dataset that will be worked with.
- `sort`: An array of objects. Each object will have these properties
  - `col`: the name of the sorted column.
  - `dir`: value "asc" or "desc".

## Data Change
- User selects from Year/Month dropdown list
- `records` is updated based on data returned.

## Data Search
- User enters term into search bar
- `records` is filtered based on `title`, `author`, `category` or `name` matching the search term.

## Data Paging

## Data Sorting
