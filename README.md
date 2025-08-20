# TO-DO-list
a simple TO-DO list project using HTML ,CSS and JAVA Script
<!DOCTYPE html>
<html>
<head>
    <title>To Do List</title>
    <style>
        body{
            font-family: sans-serif;
            background: #eee;
            text-align: center;
            padding: 20px;
        }
        h2{
            margin-bottom: 15px;
        }
        #inp{
            padding: 8px;
            width: 220px;
        }
        button{
            padding: 8px 12px;
            background: green;
            color: white;
            border: none;
            cursor: pointer;
        }
        ul{
            list-style: none;
            padding: 0;
            margin-top: 15px;
        }
        li{
            background: #fff;
            margin: 5px;
            padding: 8px;
            border-radius: 4px;
            text-align: left;
        }
    </style>
</head>
<body>
    <h2>To Do List</h2>
    <input type="text" id="inp" placeholder="write task...">
    <button onclick="addItem()">Add</button>
    <ul id="list"></ul>

    <script>
        function addItem(){
            let inp = document.getElementById("inp");
            let txt = inp.value.trim();

            if(txt.length == 0){
                // agar empty h to kuch add mat karo
                return;
            }

            let li = document.createElement("li");
            li.innerText = txt;

            // click karne se delete hoga
            li.onclick = function(){
                li.remove();
            }

            document.getElementById("list").appendChild(li);
            inp.value = "";
        }
    </script>
</body>
</html>
