```uml
@startuml
start

:weather = 天気情報;

split(0)
   :A;
split again(1)
   :B;
split again(2)
   :C;
split again(None)
   :a;
end split

end
@enduml
```
