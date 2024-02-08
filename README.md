## README

---

In this repository, you will find a sample YAML file that demonstrates various data types and structures in YAML format. Below, you will find a description of individual keys and values in the YAML file:

### Scalars
- `name`: easybytes
- `language`: Java
- `area`: Online
- `major-version`: 2
- `minor-version`: 0.5
- `hex`: 0x12d6 (expected value: 4822)
- `octal`: 024432 (expected value: 10522)
- `goodDay`: true
- `badDay`: false
- `niceweekend`: Yes
- `boringweekend`: No
- `positive-infinity`: .inf (expected value: infinity)
- `negative-infinity`: -.Inf (expected value: negative infinity)
- `invalidNumber`: .NAN (expected value: not a number)
- `null-value`: null
- `null-value1`: ~
- `organization`: eazybank
- `about`: EasyBank is a Bank-based application.
- `history`: EasyBank established in 1989.
- `products`: "[Account] & {Cards} - <Loans>" (for special characters, use double quotes in String)
- `hasMobileApp`: "Yes"

### Sequences
- `applications`:
  - Cards
  - Loans
  - Accounts
- `departments`:
  - Marketing
  - Insurance
  - Security
- `locations`: [Hyderabad, NewYork, Berlin, "Paris"]
- `products2`:
  - Accounts:
      - Savings Account
      - Current Account
  - Loans:
      - Home Loan
      - Car Loan
      - Personal Loan
  - Cards:
      - Credit Card
      - Debit Card

### Dictionaries
- `applications2`:
  - cards:
      - name: EasyCards
      - technology: Python
      - team-size: 12
  - accounts:
      - name: EasyAccounts
      - technology: Java
      - team-size: 50
  - loans:
      - name: EasyLoans
      - technology: Ruby
      - team-size: 8

### Complex Keys
- `This is a key that has multiple lines`: and this is its value
- `Dev, Test, PROD`:
  - https://dev
  - https://test
  - https://prod

### Anchors (Definitions) and Aliases
- `definitions`:
  - days:
    - weekday: &working
        wakeup: 6.00 AM
        activities:
          - workout
          - meetings
          - work
          - sleep
        sleeptime: 10:00 PM
    - weekend: &holiday
        wakeup: 08:00 AM
        activities:
          - workout
          - playing
          - movies
          - friends
          - sleep
        sleeptime: 12:00 AM
- `schedules`:
  - days:
    - weekdays:
      - monday: *working
      - tuesday: *working
      - wednesday: *working
      - thursday: *working
      - friday:
          <<: *working # exception for anchor
          sleeptime: 11:00 PM
    - weekends:
      - saturday: *holiday
      - sunday: *holiday

---

This YAML file contains various data structures that may be useful in different project scenarios. It was created to demonstrate the capabilities of the YAML format based on training from the Udemy platform. You are free to modify and customize it according to your needs.
