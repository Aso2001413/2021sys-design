```uml
@startuml
start

:weather = 天気情報;

if(wather)then(0)
:快晴です;
(0以外)elseif(wather)then(1)
:曇りです;
(1以外)elseif(wather)then(2)
:雨です;
else(その他)
:不明です;
endif

end
@enduml
```
