```gherkin

# This is a comment
Feature: Test gerkin highlight # not comment
  # This is a comment
  @commnet
  Scenario: eating # not comment
    Given there are 3.5 cucumbers # not commnet
    # This is a comment
    When I eat 2 cucumbers

  @and @but
  Scenario: Multiple Givens
    Given one thing
    And another thing
    And yet another thing
    When I open my eyes
    Then I should see something
    But I shouldn't see something else

  @outline
  Scenario Outline: eating <tert> 1 vuvu
    Given there are <start> cucumbers
    When I eat <eat> cucumbers
    Then I should have <left> cucumbers

    Examples:
        | start | eat | left |
        |    12 |   5 |    7 |
        |    20 |   5 |   15 |

  @datatable
  Scenario: Data table
    Given the following users exist:
      | name   | email              | twitter         |
      | Aslak  | aslak@cucumber.io  | @aslak_hellesoy |
      | Julien | julien@cucumber.io | @jbpros         |
      | Matt   | matt@cucumber.io   | @mattwynne      |

  @string @docstring
  Scenario: Breaker joins a game
    Given a blog post named "Random" with 'Markdown body'
      """
      Some Title, Eh?
      ===============
      Here is the first paragraph of my blog post. Lorem ipsum dolor sit amet,
      consectetur adipiscing elit.
      """
    Given the Maker has started a game with the word 'silky'
    When the Breaker joins the Maker's game
    Then the Breaker must guess a word with 5 characters

```
