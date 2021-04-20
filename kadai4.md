```uml
@startuml
start

:weather = 天気情報;
if(wwather)then(0)
:快晴です;
else(1)
:曇りです;
else(2)
:雨です;
endif

end
@enduml
```
