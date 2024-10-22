``` mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    CUSTOMER {
        nchar(5) CustomerID PK
        nvarchar(40) CompanyName
        nvarchar(30) ContactName
        nvarchar(30) ContactTitle
        nvarchar(60) Address
        nvarchar(15) City
        nvarchar(15) Region
        nvarchar(10) PostalCode
        nvarchar(15) Country
        nvarchar(24) Phone
        nvarchar(24) Fax

    }
    ORDER
    ORDER {
        int orderID
        nchar(5) CustomerID
        int EmployeeID
        datetime OrderDate
        datetime RequiredDate
        datetime ShippedDate
        int ShipVia
        money Freight
        nvarchar(40) ShipName
        nvarchar(60) ShipAddress
        nvarchar(15) ShipCity
        nvarchar(15) ShipRegion
        nvarchar(10) ShipPostalCode
        nvarchar(15) ShipCountry
    }