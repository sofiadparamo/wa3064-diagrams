| graph TD
  subgraph ATM
    atm((ATM))
  end
  
  subgraph ATM Controller
    controller((ATM Controller))
  end
  
  subgraph Bank Interface
    bank((Bank Interface))
  end
  
  subgraph Cash Dispenser
    dispenser((Cash Dispenser))
  end
  
  subgraph Card Reader
    reader((Card Reader))
  end
  
  subgraph Keypad
    keypad((Keypad))
  end
  
  subgraph Display
    display((Display))
  end
  
  atm --> controller
  controller --> bank
  controller --> dispenser
  controller --> reader
  controller --> keypad
  controller --> display