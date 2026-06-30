# The 26 Test Cases

These are the test cases published by the site at
https://automationexercise.com/test_cases, reproduced here so your work is
self-contained. **All 26 are in scope** — see `CHALLENGE.md` for what we're looking
for (hint: it's about *how* you build 26 maintainable, reliable tests, not just
that they exist).

The steps below are the site's own happy-path scripts. You are expected to
translate them into well-architected automation — not transcribe them literally.

---

## Test Case 1: Register User
1. Navigate to `http://automationexercise.com`
2. Verify that home page is visible successfully
3. Click on 'Signup / Login' button
4. Verify 'New User Signup!' is visible
5. Enter name and email address
6. Click 'Signup' button
7. Verify that 'ENTER ACCOUNT INFORMATION' is visible
8. Fill details: Title, Name, Email, Password, Date of birth
9. Select checkbox 'Sign up for our newsletter!'
10. Select checkbox 'Receive special offers from our partners!'
11. Fill details: First name, Last name, Company, Address, Address2, Country, State, City, Zipcode, Mobile Number
12. Click 'Create Account' button
13. Verify that 'ACCOUNT CREATED!' is visible
14. Click 'Continue' button
15. Verify that 'Logged in as username' is visible
16. Click 'Delete Account' button
17. Verify that 'ACCOUNT DELETED!' is visible and click 'Continue' button

## Test Case 2: Login User with correct email and password
1. Navigate to the site and verify home page is visible
2. Click on 'Signup / Login' button
3. Verify 'Login to your account' is visible
4. Enter correct email address and password
5. Click 'login' button
6. Verify that 'Logged in as username' is visible
7. Click 'Delete Account' button
8. Verify that 'ACCOUNT DELETED!' is visible

## Test Case 3: Login User with incorrect email and password
1. Navigate to the site and verify home page is visible
2. Click on 'Signup / Login' button
3. Verify 'Login to your account' is visible
4. Enter incorrect email address and password
5. Click 'login' button
6. Verify error 'Your email or password is incorrect!' is visible

## Test Case 4: Logout User
1. Navigate to the site and verify home page is visible
2. Click on 'Signup / Login' button
3. Verify 'Login to your account' is visible
4. Enter correct email address and password, click 'login'
5. Verify that 'Logged in as username' is visible
6. Click 'Logout' button
7. Verify that user is navigated to login page

## Test Case 5: Register User with existing email
1. Navigate to the site and verify home page is visible
2. Click on 'Signup / Login' button
3. Verify 'New User Signup!' is visible
4. Enter name and an already registered email address
5. Click 'Signup' button
6. Verify error 'Email Address already exist!' is visible

## Test Case 6: Contact Us Form
1. Navigate to the site and verify home page is visible
2. Click on 'Contact Us' button
3. Verify 'GET IN TOUCH' is visible
4. Enter name, email, subject and message
5. Upload a file
6. Click 'Submit' button
7. Click OK on the confirmation dialog
8. Verify success message 'Success! Your details have been submitted successfully.'
9. Click 'Home' button and verify landing on the home page

## Test Case 7: Verify Test Cases Page
1. Navigate to the site and verify home page is visible
2. Click on 'Test Cases' button
3. Verify user is navigated to the test cases page successfully

## Test Case 8: Verify All Products and product detail page
1. Navigate to the site and verify home page is visible
2. Click on 'Products' button
3. Verify user is navigated to ALL PRODUCTS page successfully
4. Verify the products list is visible
5. Click on 'View Product' of the first product
6. Verify the user lands on the product detail page
7. Verify product detail is visible: name, category, price, availability, condition, brand

## Test Case 9: Search Product
1. Navigate to the site and verify home page is visible
2. Click on 'Products' button
3. Verify user is navigated to ALL PRODUCTS page successfully
4. Enter a product name in the search input and click search
5. Verify 'SEARCHED PRODUCTS' is visible
6. Verify all the products related to the search are visible

## Test Case 10: Verify Subscription in home page
1. Navigate to the site and verify home page is visible
2. Scroll down to the footer
3. Verify text 'SUBSCRIPTION'
4. Enter an email address and click the arrow button
5. Verify success message 'You have been successfully subscribed!'

## Test Case 11: Verify Subscription in Cart page
1. Navigate to the site and verify home page is visible
2. Click 'Cart' button
3. Scroll down to the footer
4. Verify text 'SUBSCRIPTION'
5. Enter an email address and click the arrow button
6. Verify success message 'You have been successfully subscribed!'

## Test Case 12: Add Products in Cart
1. Navigate to the site and verify home page is visible
2. Click 'Products' button
3. Hover over the first product and click 'Add to cart'
4. Click 'Continue Shopping' button
5. Hover over the second product and click 'Add to cart'
6. Click 'View Cart' button
7. Verify both products are added to the cart
8. Verify their prices, quantity and total price

## Test Case 13: Verify Product quantity in Cart
1. Navigate to the site and verify home page is visible
2. Click 'View Product' for any product on the home page
3. Verify product detail is opened
4. Increase quantity to 4
5. Click 'Add to cart' button
6. Click 'View Cart' button
7. Verify the product is displayed in the cart with the exact quantity (4)

## Test Case 14: Place Order: Register while Checkout
1. Navigate to the site and verify home page is visible
2. Add products to cart
3. Click 'Cart' button and verify the cart page is displayed
4. Click 'Proceed To Checkout'
5. Click 'Register / Login' button
6. Fill all details in Signup and create account
7. Verify 'ACCOUNT CREATED!' and click 'Continue'
8. Verify 'Logged in as username' at the top
9. Click 'Cart' button, then 'Proceed To Checkout'
10. Verify Address Details and Review Your Order
11. Enter a description in the comment text area and click 'Place Order'
12. Enter payment details: Name on Card, Card Number, CVC, Expiration date
13. Click 'Pay and Confirm Order' button
14. Verify success message 'Your order has been placed successfully!'
15. Click 'Delete Account' button, verify 'ACCOUNT DELETED!' and click 'Continue'

## Test Case 15: Place Order: Register before Checkout
1. Navigate to the site and verify home page is visible
2. Click 'Signup / Login' button
3. Fill all details in Signup and create account
4. Verify 'ACCOUNT CREATED!' and click 'Continue'
5. Verify 'Logged in as username' at the top
6. Add products to cart
7. Click 'Cart' button and verify the cart page is displayed
8. Click 'Proceed To Checkout'
9. Verify Address Details and Review Your Order
10. Enter a description in the comment text area and click 'Place Order'
11. Enter payment details: Name on Card, Card Number, CVC, Expiration date
12. Click 'Pay and Confirm Order' button
13. Verify success message 'Your order has been placed successfully!'
14. Click 'Delete Account' button, verify 'ACCOUNT DELETED!' and click 'Continue'

## Test Case 16: Place Order: Login before Checkout
1. Navigate to the site and verify home page is visible
2. Click 'Signup / Login' button
3. Fill email, password and click 'Login'
4. Verify 'Logged in as username' at the top
5. Add products to cart
6. Click 'Cart' button and verify the cart page is displayed
7. Click 'Proceed To Checkout'
8. Verify Address Details and Review Your Order
9. Enter a description in the comment text area and click 'Place Order'
10. Enter payment details: Name on Card, Card Number, CVC, Expiration date
11. Click 'Pay and Confirm Order' button
12. Verify success message 'Your order has been placed successfully!'
13. Click 'Delete Account' button, verify 'ACCOUNT DELETED!' and click 'Continue'

## Test Case 17: Remove Products From Cart
1. Navigate to the site and verify home page is visible
2. Add products to cart
3. Click 'Cart' button and verify the cart page is displayed
4. Click the 'X' button corresponding to a particular product
5. Verify that the product is removed from the cart

## Test Case 18: View Category Products
1. Navigate to the site and verify categories are visible on the left sidebar
2. Click on the 'Women' category
3. Click on a category link under 'Women' (for example: Dress)
4. Verify the category page is displayed and confirm the category title text
5. On the left sidebar, click a sub-category link of the 'Men' category
6. Verify the user is navigated to that category page

## Test Case 19: View & Cart Brand Products
1. Navigate to the site and click on 'Products'
2. Verify that Brands are visible on the left sidebar
3. Click on any brand name
4. Verify the user is navigated to the brand page and brand products are displayed
5. On the left sidebar, click any other brand link
6. Verify the user is navigated to that brand page and can see the products

## Test Case 20: Search Products and Verify Cart After Login
1. Navigate to the site and click on 'Products'
2. Verify user is navigated to ALL PRODUCTS page successfully
3. Enter a product name in the search input and click search
4. Verify 'SEARCHED PRODUCTS' is visible and related products are shown
5. Add those products to the cart
6. Click 'Cart' button and verify the products are visible in the cart
7. Click 'Signup / Login' and submit login details
8. Go to the Cart page again
9. Verify those products are still visible in the cart after login

## Test Case 21: Add review on product
1. Navigate to the site and click on 'Products'
2. Verify user is navigated to ALL PRODUCTS page successfully
3. Click on a 'View Product' button
4. Verify 'Write Your Review' is visible
5. Enter name, email and review
6. Click 'Submit' button
7. Verify success message 'Thank you for your review.'

## Test Case 22: Add to cart from Recommended items
1. Navigate to the site and scroll to the bottom of the page
2. Verify 'RECOMMENDED ITEMS' are visible
3. Click 'Add To Cart' on a recommended product
4. Click 'View Cart' button
5. Verify that the product is displayed in the cart page

## Test Case 23: Verify address details in checkout page
1. Navigate to the site and verify home page is visible
2. Click 'Signup / Login' and create an account
3. Verify 'ACCOUNT CREATED!' and click 'Continue'
4. Verify 'Logged in as username' at the top
5. Add products to cart, click 'Cart', verify the cart page
6. Click 'Proceed To Checkout'
7. Verify the delivery address matches the address entered at registration
8. Verify the billing address matches the address entered at registration
9. Click 'Delete Account', verify 'ACCOUNT DELETED!' and click 'Continue'

## Test Case 24: Download Invoice after purchase order
1. Navigate to the site and verify home page is visible
2. Add products to cart, click 'Cart', verify the cart page
3. Click 'Proceed To Checkout'
4. Click 'Register / Login' and create an account
5. Verify 'ACCOUNT CREATED!' and click 'Continue'
6. Verify 'Logged in as username', go to Cart, click 'Proceed To Checkout'
7. Verify Address Details and Review Your Order
8. Enter a description and click 'Place Order'
9. Enter payment details and click 'Pay and Confirm Order'
10. Verify success message 'Your order has been placed successfully!'
11. Click 'Download Invoice' and verify the invoice is downloaded successfully
12. Click 'Continue'
13. Click 'Delete Account', verify 'ACCOUNT DELETED!' and click 'Continue'

## Test Case 25: Verify Scroll Up using 'Arrow' button and Scroll Down functionality
1. Navigate to the site and verify home page is visible
2. Scroll down to the bottom of the page
3. Verify 'SUBSCRIPTION' is visible
4. Click the arrow at the bottom-right to move upward
5. Verify the page scrolls up and the 'Full-Fledged practice website for Automation Engineers' text is visible

## Test Case 26: Verify Scroll Up without 'Arrow' button and Scroll Down functionality
1. Navigate to the site and verify home page is visible
2. Scroll down to the bottom of the page
3. Verify 'SUBSCRIPTION' is visible
4. Scroll up to the top of the page
5. Verify the page scrolls up and the 'Full-Fledged practice website for Automation Engineers' text is visible
