flowchart TD
  subgraph User
    Withdraw((Withdraw Money))
    Deposit((Deposit Money))
    CheckBalance((Check Account Balance))
    PayService((Pay Service Bills))
    LogOut((Log Out))
  end
  
  subgraph ATM System
    Authenticate((Authenticate Card))
    VerifyCash((Verify Cash Availability))
    PerformTransaction((Perform Transaction))
    RecordTransaction((Record Transaction))
    DispenseCash((Dispense Cash))
    DisplayMessage((Display Message))
  end
  
  User --> Withdraw
  User --> Deposit
  User --> CheckBalance
  User --> PayService
  User --> LogOut
  
  Withdraw --> Authenticate
  Authenticate --> VerifyCash
  VerifyCash --> PerformTransaction
  PerformTransaction --> RecordTransaction
  RecordTransaction --> DispenseCash
  DispenseCash --> DisplayMessage
  
  Deposit --> Authenticate
  Authenticate --> VerifyCash
  VerifyCash --> PerformTransaction
  PerformTransaction --> RecordTransaction
  RecordTransaction --> DisplayMessage
  
  CheckBalance --> Authenticate
  Authenticate --> PerformTransaction
  PerformTransaction --> DisplayMessage
  
  PayService --> Authenticate
  Authenticate --> VerifyCash
  VerifyCash --> PerformTransaction
  PerformTransaction --> RecordTransaction
  RecordTransaction --> DisplayMessage