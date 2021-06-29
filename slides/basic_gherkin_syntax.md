---
layout: image-left
image: https://source.unsplash.com/Gej8FOFLlHg/1600x900
---

# Basic syntax

```gherkin
Feature: Access privacy information
  The website needs to provide privacy information
  for any user accessing the google search page

  Scenario: Request main page
    When a user request "www.google.com"
    Then the response include a link to "Privacy"

  Scenario: Request Privacy
    Given the user is at "www.google.com"
    When the user clicks "Privacy"
    Then the response includes "Google Privacy Policy"

  Scenario: Get effective date
    Given the user is at "policies.google.com/privacy"
    Then "Effective" exists on the page 
```