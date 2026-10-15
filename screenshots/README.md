# Discount Percentage verification

Captured from the running local frontend at http://localhost:5173/ on 2026-10-15.
The submission section was not supplied, so these captures cover the requested
Add Item, Home, and related update behavior.

- `01-add-item.jpg`: populated Add Item form with 12.5% discount before saving.
- `02-home-saved.jpg`: Home page displaying the saved 12.5% discount.
- `03-edit-item.jpg`: Edit Item form changing the discount to 20%.
- `04-home-updated.jpg`: Home page displaying the updated 20% discount.

The sample Wireless Headphones item remains available in the running application.

Verification completed:

- Frontend production build passes.
- UI creation saves 12.5%, Edit loads that value, and updating to 20% remains
  visible after reloading Home.
- API create, detail read, list read, and update preserve numeric discounts.
- Updates accept 0, 100, and decimal percentages.
- Create and update reject negative values, values above 100, nonnumeric text,
  and null.
- Creating without a discount defaults to 0; unrelated updates preserve it.
- Temporary API verification items were removed after the checks.
