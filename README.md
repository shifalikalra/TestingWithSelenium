# TestingWithSelenium
Selenium Test Project - Trusted Shops Rating Page
This README contains the step by step explanation of the testing code and the further development of concepts!

This project demonstrates how to automate tests for the Trusted Shops rating page using Selenium WebDriver and Java. The tests verify various aspects of the page, such as the page title, grade value, additional information window, review filtering, and star percentage calculation.

Prerequisites:
Java JDK 8 or higher
Selenium WebDriver
ChromeDriver (compatible with your Chrome browser version)

Step By Step Explanation:
The project starts by setting up the necessary dependencies and drivers, including the ChromeDriver.

The TestClass main method initializes the ChromeDriver and navigates to the Trusted Shops rating page.

The code waits for the cookie pop-up to appear and accepts it by clicking the accept button.

The page title is retrieved using the getTitle() method and checked for existence. The result is printed to the console.

The grade value is extracted from the page using the class name "ctgork". It is then parsed as a double and checked if it is above zero. The grade value and its existence are printed to the console.

The code clicks on the "Wie berechnet sich die Note?" link to open the window with additional information.

It switches to the new window and waits for the "info-content" element to be present. The text of the element is retrieved and checked for existence. The additional information is printed to the console.

The code switches back to the default content (main page).

It locates and clicks on the "2 Stars" filter to display only reviews with two stars.

The code verifies that all the filtered reviews have a star rating of two stars. It iterates over each review element, retrieves the star rating text, and compares it with "2 Stars". The result is printed to the console.

The star percentage values displayed on the page are retrieved from the "jEoVFS" element.

The code splits the percentage values using a regular expression to separate them.

It then iterates over each percentage value, removes the percentage sign, and checks if the cleaned percentage is not empty.

If the cleaned percentage is not empty, it is parsed as a double and added to the sum of star percentages if adding it does not exceed 100.

The sum of star percentages is calculated and printed to the console.

Finally, the browser is closed using the quit() method.

Concept for Further Development: 
1. What kind of checks would you add to current test?
Check the visibility and correctness of other important elements on the page, such as the company name, address, contact information, etc.
Validate the presence and functionality of any interactive elements on the page, such as buttons, dropdowns, or input fields.
Verify that the reviews are sorted correctly based on their rating or date.
Check if pagination or infinite scrolling is implemented correctly and validate the navigation between different pages of reviews.
Validate that the page is responsive and works well on different screen sizes and devices.

2. What are the next tests you would recommend implementing?
Perform negative tests by intentionally providing invalid input or trying to access restricted functionality, and ensure appropriate error handling and validation messages are displayed.
Implement end-to-end tests that cover the entire user journey, starting from landing on the website to submitting a review or performing any other important actions.
Test the website's search functionality by entering different keywords and verifying that the search results are accurate and relevant.
Test the website's performance by measuring page load times, response times, and resource utilization under various traffic conditions.
Implement tests to validate the website's security, such as checking for proper handling of sensitive data, preventing XSS (cross-site scripting) attacks, and ensuring secure communication over HTTPS.

3. Does the profile page have non-functional properties? How would you test these properties?
Non-functional properties of the profile page may include performance, usability, accessibility, security, and compatibility.
To test these properties, specific test scenarios can be designed:
Performance: Measure the page load time, response time, and server resource utilization under different user loads using tools like JMeter or Selenium Grid.
Usability: Conduct usability testing with real users to evaluate the ease of navigation, intuitiveness, and overall user experience of the profile page.
Compatibility: Test the profile page on different browsers, devices, and operating systems to ensure it renders correctly and functions properly across various combinations.
Overall, the goal is to ensure that the profile page not only meets functional requirements but also satisfies non-functional aspects, providing a secure, performant, usable, and accessible user experience.
