```mermaid
graph TD
  subgraph User Interface
    Keypad
    Display
  end
  
  subgraph ATM Control
    CardReader
    ATM
  end
  
  subgraph ATM Peripherals
    CashDispenser
  end
  
  subgraph Bank Interface
    Bank
  end
  
  Keypad -- PIN Entry --> CardReader
  CardReader -- Authentication Request --> ATM
  ATM -- Authentication Request --> Bank
  Bank -- Authentication Response --> ATM
  Keypad -- Transaction Type Selection --> ATM
  ATM -- Transaction Request --> Bank
  Bank -- Transaction Response --> ATM
  ATM -- Cash Availability Check --> CashDispenser
  ATM -- Dispense Cash --> CashDispenser
  ATM -- Message Display Request --> Display
```