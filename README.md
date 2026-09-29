# List View
- API Endpoint: ords/teochewthunder/borrowing/`year`/`month`
- Example: https://oracleapex.com/ords/teochewthunder/borrowing/2026/3

## HTML/CSS
- Header and rows are styled using the same template grid format, for consistency.
- Header labels are actually buttons that have been disguised as labels. They also have a direction indicator to show if they are being used to sort, and in what direction.

## Properties
- `records`: An array of records that have been returned from the API endpoint. This is the dataset that will be worked with.
- `sort`: An array of objects. Each object will have these properties
  - `col`: the name of the sorted column.
  - `dir`: value "asc" or "desc".
- `pageNo`: current page being viewed in the dataset.
- `pageSize`: number of records in a page.
- `search`: value to filter columns by.

## Data Change
- User selects from Year/Month dropdown list
- Result: `records` is updated based on data returned.

## Data Search
- User enters term into search bar
- Result: `records` is filtered based on `title`, `author`, `category` or `name` matching the search term in `search`.

## Data Paging
- User clicks "Next", "Prev", "Last" or "First" buttons.
- `pageNo` changes. 
OR User selects page size from dropdown list.
- Result: `records` is filtered according to `pageSize` and `pageNo`.

## Data Sorting
- User clicks on any of the header buttons.
  - if column is not already in `sort`, push it to `sort` with direction "asc".
  - if column is already being sorted with directon "asc", change it to "desc".
  - if column is already being sorted with directon "desc", remove it from `sort`.
- Result: `records` is sorted by all elements in `sort` before being displayed.
