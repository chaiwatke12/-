function sendLineNotify() {

  var token = "xxxxxxxxxxxxxxxxxxxx"; //แก้ไข Token
  var message = "xxxxxxxxxxxxxxxxxxxx"; //แก้ไข ข้อความ
  
  var payload = {"message": message};
  var options = {
    "method": "post",
    "headers": {
      "Authorization": "Bearer " + token
    },
    "payload": payload
  };
  
  UrlFetchApp.fetch("https://notify-api.line.me/api/notify", options);
  
}