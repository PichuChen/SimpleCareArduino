# SimpleCareArduino
Arduino code for Simple Care

這份專案的詳情請洽臉書社團 Simple Care - 開放長照智慧系統
https://www.facebook.com/groups/664434100418340/

這個repo主要是讓大家de完bug之後de完的結果送上來。


送上來的方式請參考這邊：
http://gitbook.tw/chapters/github/pull-request.html

Event Stream的Client Code:
```
var evtSource = new EventSource("//www.tih.tw:8081/2/device/BLE_DATA?event-stream", { withCredentials: true } ); 
data = [];
evtSource.onmessage = function(e) {
  var newElement = document.createElement("li");
  
  newElement.innerHTML = "message: " + e.data;
  console.log(e.data)

 // eventList.appendChild(newElement);
}
```

