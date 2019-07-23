<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <script src="../jquery/jquery-3.4.1.js"></script>
</head>
<body>  
        <script>
                function runSlots() {
                var slotOne;
                var slotTwo;
                var slotThree;
                
                var images = ["https://www.w3cschool.cn/statics/codecamp/images/9H17QFk.png", "https://www.w3cschool.cn/statics/codecamp/images/9RmpXTy.png", "https://www.w3cschool.cn/statics/codecamp/images/VJnmtt5.png"];
                
                slotOne = Math.floor(Math.random() * (3 - 1 + 1)) + 1;
                slotTwo = Math.floor(Math.random() * (3 - 1 + 1)) + 1;
                slotThree = Math.floor(Math.random() * (3 - 1 + 1)) + 1;
                
                
                
                $($('.slot')[0]).html('<img src = "' + images[slotOne-1] + '">');
                $($('.slot')[1]).html('<img src = "' + images[slotTwo-1] + '">');
                $($('.slot')[2]).html('<img src = "' + images[slotThree-1] + '">');
                
               
                
                if (slotOne === slotTwo && slotTwo === slotThree) {
                $('.logger').html("Win");
                return null;
                }
                
                if (slotOne !== undefined && slotTwo !== undefined && slotThree !== undefined){
                $(".logger").html(slotOne + " " + slotTwo + " " + slotThree);
                }
                
                $('.logger').html(" Not A Win");
                
                return [slotOne, slotTwo, slotThree];
                }
                
                $(document).ready(function() {
                 $('.go').click(function() {
                 runSlots();
                 });
                 });
                </script>
                 
                <div>
                 <div class = 'container inset'>
                 <div class = 'header inset'>
                 <h2>@HaoZai</h2>
                 </div>
                 <div class = 'slots inset'>
                 <div class = 'slot inset'>
                 
                 </div>
                 <div class = 'slot inset'>
                 
                 </div>
                 <div class = 'slot inset'>
                 
                 </div>
                 </div>
                 <br/>
                 <div class = 'outset'>
                 <button class = 'go inset'>
                 Go
                 </button>
                 </div>
                 <br/>
                 <div class = 'foot inset'>
                 <span class = 'logger'></span>
                 </div>
                 </div>
                </div>
                
                <style>
                 .slot > img {
                margin: 0!important;
                height: 71px;
                width: 50px;
                 }
                 body{
                     background-color: #482A0F;
                 }
                 .container {
                 background-color: #4a2b0f;
                 height: 400px;
                 width: 260px;
                 margin: 50px auto;
                 border-radius: 4px;
                 }
                 .header {
                 border: 2px solid #fff;
                 border-radius: 4px;
                 height: 55px;
                 margin: 14px auto;
                 background-color: #457f86
                 }
                 .header h2 {
                 height: 60px;
                 margin: auto;
                 text-align: center;
                 line-height: 60px;
                 
                 }
                 .header h2 {
                 font-size: 14px;
                 margin: 0 0;
                 padding: 0;
                 color: #fff;
                 text-align: center;
                 }
                 .slots{
                 display: flex;
                 background-color: #457f86;
                 border-radius: 6px;
                 border: 2px solid #fff;
                 }
                 .slot{
                 flex: 1 0 auto;
                 background: white;
                 height: 75px;
                 width: 50px;
                 margin: 8px;
                 border: 2px solid #215f1e;
                 border-radius: 4px;
                 text-align: center;
                 }
                 .go {
                 width: 100%;
                 color: #fff;
                 background-color: #457f86;
                 border: 2px solid #fff;
                 border-radius: 2px;
                 box-sizing: none;
                 outline: none!important;
                 }
                 .foot {
                 height: 150px;
                 background-color: 457f86;
                 border: 2px solid #fff;
                 }
                 
                 .logger {
                 color: white;
                 margin: 10px;
                 }
                 
                 .outset {
                 -webkit-box-shadow: 0px 0px 15px -2px rgba(0,0,0,0.75);
                 -moz-box-shadow: 0px 0px 15px -2px rgba(0,0,0,0.75);
                 box-shadow: 0px 0px 15px -2px rgba(0,0,0,0.75);
                 }
                 
                 .inset {
                 -webkit-box-shadow: inset 0px 0px 15px -2px rgba(0,0,0,0.75);
                 -moz-box-shadow: inset 0px 0px 15px -2px rgba(0,0,0,0.75);
                 box-shadow: inset 0px 0px 15px -2px rgba(0,0,0,0.75);
                 }
                </style>
</body>
</html>
