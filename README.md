<Html>
    <Head>
        <style>
            #txt{border: 0;
            font-size: larger;
        ;
    border-width: 1px;

        </style>
    </Head>
    
        
    
    <script>
        
        var c=0;
        
        var t;
        
        var timer_is_on=0;
        
        function timedCount(){
        
            document.getElementById('txt').value=c;
        
            c=c+1;
        
            t=setTimeout(function(){timedCount()},1000);
        
        }
        
        function doTimer(){
        
            if (!timer_is_on){
        
                timer_is_on=1;
        
                timedCount();
        
            }
        
        }
        
        function stopCount(){
        
            clearTimeout(t);
        
            timer_is_on=0;
        
        }
        
        </script>
        
        </head>
        
        <body>
        
            
        
        <form>
        
        <input type="button" value="开始计数!" onclick="doTimer()" /><br>
        
       <p>time:    <input type="text" id="txt" /></p>   
        
        <input type="button" value="停止计数!" onclick="stopCount()" />
        
        </form>
        
        
        </body>
        
        </html>
