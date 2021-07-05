```startuml
@startuml

entity "顧客マスタ" as customer <m_customers>{
+ customer_code[PK]
--
pass
name
address
tel
mail
del_flag
reg_date
}

@enduml
```
