# Answer-Qwiik-Test

Feature: Login functionality on SauceDemo website

  Scenario: Successful login with valid credentials
    Given I am on the SauceDemo login page
    When I enter valid username and password
    And I click on the login button
    Then I should be redirected to the home page
    And I should see the products displayed
  
  Scenario: Unsuccessful login with invalid credentials
    Given I am on the SauceDemo login page
    When I enter invalid username and/or password
    And I click on the login button
    Then I should see an error message indicating login failure
    And I should remain on the login page
  
  Scenario: Reset password functionality
    Given I am on the SauceDemo login page
    When I click on the 'Forgot Password' link
    Then I should be redirected to the password reset page
    And I should see a form to enter my email address
    When I enter my email address
    And I click on the 'Reset Password' button
    Then I should see a confirmation message indicating that an email has been sent
  
  Scenario: Logout functionality
    Given I am logged in to the SauceDemo website
    When I click on the logout button
    Then I should be redirected to the login page
    And I should see the login form
