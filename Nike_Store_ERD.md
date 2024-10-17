```mermaid
erDiagram
    PRODUCT {
        string product_id PK 
        string name 
        string model 
        decimal price 
        string category 
    }
    
    CUSTOMER {
        string customer_id PK 
        string first_name 
        string last_name 
        string email 
        string phone 
    }
    
    SALE {
        string sale_id PK 
        date sale_date 
        string customer_id  
        string product_id  
        int quantity 
        decimal total_price 
    }
    
    INVENTORY {
        string product_id PK 
        int stock_level 
        string warehouse_location 
    }

    PRODUCT ||--|{ SALE : "sold_in"
    CUSTOMER ||--|{ SALE : "makes"
    PRODUCT ||--|{ INVENTORY : "tracked_in"

```

## Documentation
PRODUCT ||--|{ SALE: This means a product can be sold in many sales, but each sale only includes one product. So, lots of people can buy the same cool sneakers.

CUSTOMER ||--|{ SALE: A customer can make many sales, but each sale is tied to one customer. Like, if Alex buys sneakers and a shirt, those are two different sales, but both are by Alex.

PRODUCT ||--|{ INVENTORY: A product can be tracked in the inventory, so you know how many you have and where they are stored